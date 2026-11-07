---
name: one-page-rfc
description: "Prevents AI workslop in system design RFCs, Architecture Decision Records (ADRs), and sprint planning tickets. Forces any design proposal or feature spec into a 1-page human-scannable brief with explicit system boundaries, non-goals, two real alternatives, and executable completion evidence. Use whenever drafting an RFC, ADR, design doc, or breaking an epic into sprint tasks."
---

# One-Page Anti-Workslop RFC & Task Spec

In Stanford University and BetterUp's 2025 study in *Harvard Business Review*, recipients spent **1 hour and 56 minutes per incident** decoding and rewriting verbose, context-free AI documents ("workslop"). In Faros AI's 2026 study, unverified specs drove a **+13.8% increase in task restarts**.

Never generate a multi-page textbook essay when asked for a system design or sprint breakdown. Produce a **strictly bounded 1-page brief** (maximum 350 words in the main body) using the structure below.

---

## Required 1-Page RFC / ADR Structure

### 1. Problem & System Boundary (3 sentences max)
- **What is broken or missing today** (with a concrete metric, latency, or failure mode).
- **Who is affected** (service, API consumers, or tenant tier).
- **Blast-radius boundary:** Which services, tables, or wire formats are touched.

### 2. Explicit Non-Goals (3 bullets max)
- State what this design **intentionally does not solve** so coding agents and reviewers do not overreach or gold-plate adjacent modules.

### 3. Proposed Design vs. Alternatives (Compact Table)
Compare the recommended approach against at least one simpler alternative (e.g., "Do minimal change in existing module"):

| Approach | Files / Tables Touched | What Improves | What Gets Worse (Trade-off) |
|---|---|---|---|
| **Recommended:** ... | `path/to/module` | ... | ... |
| **Alternative:** ... | `path/to/existing` | ... | ... |

### 4. Unverified Assumptions (Must Be Flagged for Human Check)
- List every assumption about traffic volume, database locks, backward compatibility, or third-party behavior that the human author must verify before approving.

### 5. Stacked PR Plan (`<150 LOC` per PR, `WIP = 1`) & Completion Evidence
Break implementation into small, sequentially mergeable PRs. Every step must include an **executable verification command** (not "code looks good"):

1. **PR 1 (`~80 LOC`):** Schema/types + unit tests -> **Verify:** `pytest tests/unit/test_schema.py`
2. **PR 2 (`~120 LOC`):** Service logic behind feature flag -> **Verify:** `pytest tests/integration/test_service.py`
3. **PR 3 (`~60 LOC`):** Canary rollout + cleanup -> **Verify:** `curl -f ...` + canary error rate check

*(If raw schema DDL, payload examples, or benchmark logs are needed, place them at the very bottom inside a collapsed `<details><summary>Appendix: Raw Schemas & Payloads</summary>...</details>` block.)*
