# Anti-Slop & Mental-Map Engineering Instructions (CLAUDE.md)

Copy this file to `./CLAUDE.md` (repository root, shared with your team) or `~/.claude/CLAUDE.md` (global personal rules for all projects).

---

## 1. Response Shape & Anti-Chat-Slop (BLUF + Progressive Disclosure)

Never bury the key point inside multi-paragraph explanations or file-by-file narration:

- **BLUF (Bottom Line Up Front):** Always open with a 1 to 2 sentence summary stating the root cause, architectural decision, or result. No preamble, no restating my prompt, and no closing "next steps" filler.
- **Max 3 to 5 bullets for the big picture:** Group explanations by system behavior and architecture, never by a line-by-line walkthrough of every file touched.
- **After editing files:** List only the modified file paths (`path/to/file.ext:line`), one per line, with a one-line reason. Do not narrate the diff in prose; I will read the diff in the editor.
- **For yes/no or trade-off questions:** Answer with the recommendation first in one sentence, followed by a compact comparison table.
- **Gate the nitty-gritty (Progressive Zoom):** Stop after giving the high-level mental map (Zoom Level 1). If deeper implementation or query-plan details exist, end with a single prompt: *"Want to zoom into [A: data flow & state transitions] or [B: line-by-line edge cases]?"* Expand only when asked.
- **Visuals over walls of text:** When explaining how 3 or more modules, services, or database tables interact, draw a compact ASCII or Mermaid flow diagram (max 6 nodes) before writing prose.

---

## 2. Subagent Context Isolation (Keep Main Chat Clean)

Do not pollute the main conversation context with raw file searches, long stack traces, or multi-file exploratory reads:

- **Delegate exploration to subagents:** When a task requires searching across more than 3 files, tracing unfamiliar call chains, or inspecting long `kubectl` / CI / SQL logs, spawn an isolated subagent (`Task` / `explore` / `mental-map-explorer`).
- **Strict subagent return contract:** Instruct the subagent to return **only**:
  1. A 3-sentence architectural summary of how the path works.
  2. Up to 5 essential entry-point `file:line` references.
  3. The exact location of the bug or integration boundary.

---

## 3. Code Quality: Refactor Over Write-Only Bloat

Counteract additive "write-only" code generation:

- **Search before creating:** Before adding a new helper, utility, or wrapper class, search existing modules (`Grep` / `Glob`) and reuse or refactor existing functions in place.
- **Zero 5-line clones:** Never copy-paste blocks of 5 or more lines across files. Extract shared domain logic into a single well-named function.
- **No speculative abstractions:** Do not invent interfaces, factory classes, or configuration layers for a single caller. Write explicit, linear code.
- **Small batches (`<150 LOC`):** Keep every logical change under 150 changed lines of code. If a task requires more than 150 lines or touches more than 4 files, stop, enter Plan Mode, and split the work into sequential stacked steps.

---

## 4. Zero Silent Failures & Honest Tests

- **No error-masking wrappers:** Never add broad `try/catch` (or `try/except`) blocks that swallow exceptions, log-and-continue, or return silent fallback/mock values in production code. Every error must either be handled explicitly by type or bubble up with full context.
- **No self-passing unit tests:** Never write unit tests by copying the implementation logic into the test or mocking out the exact database/network boundary where bugs occur. Write behavioral tests that fail when the underlying business logic breaks.
- **Verify before stopping:** Always run the relevant linter and test command for touched files before reporting completion.
