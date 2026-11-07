---
name: debloat-audit
description: "Strips out AI write-only bloat (+81% duplicate code blocks, single-use wrappers, dead abstractions) and eliminates silent error-masking constructs (+47% broad try/catch blocks, swallowed exceptions, fallback mocks) while preserving exact behavior. Use after generating or modifying code."
---

# Post-Coding De-Bloat & Silent-Failure Audit

Two large-scale 2026 empirical studies (GitClear's analysis of `623M` changed lines and LinearB's benchmark of `8.1M` pull requests) show that AI coding assistants default to **additive, write-only code**: refactoring drops by **-70%**, duplicated 5+ line blocks jump by **+81%**, and silent error-masking wrappers (`try/catch` blocks that swallow exceptions or return mock fallbacks) rise by **+47%**.

Run this pass immediately after generating code and before committing.

---

## Step 1: De-Bloat (Counteract the `-70%` Refactoring & `+81%` Clone Trap)

Inspect the current diff (`git diff`) and neighboring modules:

1. **Collapse Duplicate Blocks (`5+` lines):** Search existing files (`Grep` / `Glob`) for functions that already perform the same validation, transformation, or query. Replace duplicated blocks with calls to shared functions.
2. **Delete Speculative Wrappers:** Remove single-caller interfaces, pass-through helper functions, factory classes, and unused configuration parameters that were not requested.
3. **Flatten Control Flow:** Replace deeply nested ternaries or redundant boolean flags with explicit early returns (`guard clauses`).
4. **Enforce Batch Size (`<150 LOC`):** Verify the net change stays compact and focused.

---

## Step 2: Hunt Silent Failures (Counteract the `+47%` Error-Masking Trap)

Inspect every `try/catch`, `try/except`, `.catch()`, `if err != nil`, `??`, and fallback branch in the touched files:

1. **Forbid Swallowed Exceptions:** Delete or fix empty catch blocks and catch-and-log-only blocks that allow execution to continue with corrupted or `null` state.
2. **Forbid Production Mock Fallbacks:** Remove any fallback branch that returns dummy, mock, or fabricated default data when a database query, API call, or config lookup fails.
3. **Narrow Exception Types:** Replace broad catch-all handlers (`except Exception:`, `catch (e)`) with the specific error types expected at that boundary so unexpected programming bugs fail loudly.

---

## Step 3: Output Summary (Max 8 Lines)

After applying the edits, report only:
- **Consolidated / De-bloated:** `path/to/file.ext:line` (1-line summary of duplicate logic or wrapper removed).
- **Silent Failures Fixed:** `path/to/file.ext:line` (what error was previously masked and how it now fails explicitly).
