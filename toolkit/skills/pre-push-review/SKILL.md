---
name: pre-push-review
description: "Shifts AI code review left into the author's IDE before git push, replacing noisy low-signal PR review bots with a high-precision local audit. Checks diff size (under 150 LOC), duplicate code blocks (+81% GitClear clone trap), silent error-masking wrappers (+47% try/catch trap), and self-passing unit tests. Use before committing or opening a pull request."
---

# Local Pre-Push Audit (Shift-Left Code Review)

Research from MSR 2026 (`3,109` PRs) and Bilkent University (`4,335` PRs) shows that running general-purpose AI review bots on open pull requests generates `<30%` actionable signal and slows PR merge time by **+42%**. Instead, run this high-precision audit **locally in your IDE before `git push`**.

---

## Audit Checklist (Run Against `git diff origin/main...HEAD`)

### Gate 1: Batch Size & Stack Check (`<150 LOC`)
- Count changed production lines (excluding lockfiles and generated snapshots).
- **If `>150 LOC` or `>4` files across different layers:** Halt and propose how to split the diff into 2 to 3 stacked pull requests (for example, using `gh stack` or Graphite `gt create`).

### Gate 2: Duplicate Block & Write-Only Bloat Check
- Check whether any 5+ line block in the diff duplicates logic that already exists in the repository (or run `npx jscpd . --baseline-from-ref origin/main --fail-on-new-clones` if installed).
- Check whether the diff introduces a redundant wrapper class, helper file, or interface that could be a 10-line change inside an existing module.

### Gate 3: Silent Failure & Error-Masking Hunter
Inspect every `try/catch`, `try/except`, `.catch()`, `??`, and fallback branch in the diff:
- **CRITICAL:** Empty catch blocks, catch-and-log-only blocks that continue execution with corrupted state, or production code falling back to mock/dummy data.
- **HIGH:** Broad exception catching (`except Exception:`) that hides unexpected programming bugs alongside expected network/I/O errors.

### Gate 4: Test Oracle & Mutation Check (No Self-Passing Tests)
For every new or modified test in the diff:
- Verify the test asserts **observable behavior and contracts**, not internal implementation mocks.
- **The Revert Mental Test:** Ask: *"If I comment out the core business-logic line in the production diff, will this test actually fail?"* If a test mocks out the exact database query, permission check, or state transition where bugs live, flag it as a self-passing test.

---

## Output Format (Confidence >= 80 Only)

Report **only high-confidence issues (score >= 80/100)**. Do not report style nitpicks or issues a linter catches:

1. **Verdict Badge:** `READY TO PUSH` or `NEEDS LOCAL FIX (N issues)`
2. **Diff Stats:** `X files changed, Y production LOC (Target: <150 LOC)`
3. **Blocking Findings (if any):** Exact `file:line`, category (`Bloat` | `Silent Failure` | `Weak Test` | `Bug`), and a 2-line fix.
