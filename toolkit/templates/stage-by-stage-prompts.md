# Stage-by-Stage Prompt Templates & CI Gates for the 80-Hour AI Sprint

Use these copy-paste prompts and CI gates to prevent the **+35.5-hour cleanup, debugging, and review rebound** across all six stages of the sprint.

---

## Stage 1: Hands-On Coding (Preventing `+81%` Clones & `-70%` Refactoring Drop)

### Prompt 1A: Refactor-First Feature Prompt
```text
Before writing any code for [FEATURE]:
1. Search the codebase (using a subagent) for existing modules, types, and helpers that touch this domain.
2. Show me a 5-line Mental Map of which existing functions we can extend or refactor in place instead of creating new files.
3. Keep the implementation surgical (<150 LOC), with zero duplicated 5+ line blocks and zero silent try/catch fallbacks.
Stop after step 2 and wait for my approval before editing files.
```

### CI Gate 1B: Block New Code Clones with `jscpd`
Add this single step to GitHub Actions or GitLab CI so pull requests fail **only if they introduce new copy-pasted blocks** compared to `main` (see [jscpd CI guide](https://jscpd.dev/guides/ci)):

```bash
# Fails only on newly introduced duplicate blocks in the PR diff
npx jscpd . --baseline-from-ref origin/main --fail-on-new-clones --reporters ai
```

---

## Stage 2: Debugging, K8s/DB Investigation & Testing (Preventing Missing Mental Map & Self-Passing Tests)

### Prompt 2A: Read-Only K8s/SQL Incident Bundle (Build the Mental Map First)
```text
Investigate [BUG / ALERT] in read-only mode. Do NOT edit any files yet.
Use a subagent to inspect the logs/SQL state and return ONLY:
1. Verified Facts: Exact log lines, SQL counts, and file:line locations confirmed so far.
2. Call-Chain Map: A 1-line flow from the entry point to where the state breaks.
3. Top 2 Competing Hypotheses: For each hypothesis, state what single command or test will prove it false.
Wait for me to review the mental map before proposing a fix.
```

### Prompt 2B: Specification-First & Mutation-Guided Test Prompt
(Counteracts the flaw documented in ETH Zurich's 2026 *TestSuiteBench* study, where agent-generated tests pass on buggy code and score `<60%` on mutation testing):
```text
Write behavioral unit tests for [MODULE / FUNCTION] based on its specification, NOT by copying its implementation:
1. Do not mock the core state transition or SQL/validation boundary being tested.
2. For every test, state in 1 line which specific bug or mutant (e.g., off-by-one, null payload, unauthorized tenant, partial failure) would cause this test to fail.
3. Run the tests, then temporarily break the production condition on line [X] to prove the new test fails when the bug is present.
```

---

## Stage 3: System Design & Architecture RFCs (Preventing the `1h 56m` Workslop Tax)

### Prompt 3A: The 1-Page Anti-Workslop RFC Prompt
```text
Draft a 1-page RFC (max 350 words) for [SYSTEM / FEATURE]. No textbook filler or generic intro.
Include only:
1. Problem & Blast Radius (3 sentences max, naming exact services/tables).
2. Explicit Non-Goals (3 bullets of what we will NOT build).
3. Trade-Off Table comparing (A) Minimal change in existing service vs. (B) New abstraction.
4. Unverified Assumptions I must check manually with the team.
5. A 3-PR stacked rollout plan (<150 LOC per PR) with an executable verification command for each PR.
```

---

## Stage 4: Sprint Planning & Meetings (Preventing Ticket Inflation & `+67%` Parallel WIP)

### Prompt 4A: `WIP = 1` Sprint Task Slicer with Completion Evidence
```text
Break [EPIC] into sequential, small-batch tasks (<150 LOC each) designed for WIP = 1 (finish and verify one before starting the next).
For each task, provide a 4-line card:
- Scope Boundary: Exact files allowed to change (and files off-limits).
- Depends On: Prior task ID.
- Completion Evidence: The exact test or curl/SQL command that proves the behavior works end to end.
Do not generate sub-tasks for boilerplate formatting or documentation filler.
```

---

## Stage 5: PR Code Review (Preventing `5.3×` Pickup Wait & `<30%`-Signal Bot Noise)

### Prompt 5A: Split a Large Diff into a Reviewable PR Stack
(Uses GitHub's native `gh stack` or Graphite `gt` workflow):
```text
My current branch diff is [N] lines across [M] files.
Propose a 3-layer Stacked PR breakdown where each layer is <150 LOC, compiles and passes tests independently, and can be reviewed by a teammate in under 10 minutes:
- Stack PR 1: Types, schema, or foundational refactor (no behavior change).
- Stack PR 2: Core business logic + behavioral tests.
- Stack PR 3: API/UI wiring + feature flag guard.
```

---

## Stage 6: CI/CD & Production Ops (Preventing `+242.7%` Production Incidents per PR)

### Prompt 6A: Pre-Merge Blast-Radius & Rollback Check
```text
Before we merge this PR, generate a 5-line Production Safety Check:
1. Risk Class: Low | Standard (needs feature flag / 5% canary) | High (touches DB schema -> requires expand-and-contract migration, never a flag alone).
2. Instant Rollback Path: How do we revert this in <60 seconds without waiting for a full CI rebuild?
3. Canary Guardrail Metric: Which exact error rate or P95 latency metric triggers an automatic rollback?
```
