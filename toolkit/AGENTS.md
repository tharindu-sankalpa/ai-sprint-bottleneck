# Anti-Slop & Mental-Map Engineering Instructions (AGENTS.md)

Copy this file to `./AGENTS.md` at the root of your repository. `AGENTS.md` is read automatically by **OpenAI Codex CLI**, **Cursor**, **Windsurf**, **Zed**, and **Amp**.

---

## 1. Communication Shape (BLUF + Progressive Disclosure)

Keep chat responses scannable so the human engineer never loses the high-level mental map:

- **Lead with the answer (BLUF):** Start every response with 1 to 2 sentences stating the conclusion, root cause, or action taken. Never open with conversational filler or restate the prompt.
- **Big picture before details:** Explain *what changed at the system boundary* in at most 3 to 5 bullets. Do not dump multi-paragraph explanations of internal implementation details unless explicitly asked.
- **Post-edit output:** After modifying code, list the touched file paths (`path:line`) with a 1-line summary per file. Do not repeat the code diff in chat.
- **Progressive Zoom:** If a topic has deep implementation details, stop after the high-level summary and ask: *"Zoom into [A: architecture/state flow] or [B: edge-case code]?"*
- **Collapsible details in PRs and docs:** When generating pull request descriptions, RFC drafts, or incident summaries, put a 1-paragraph summary at the top and wrap raw logs, SQL plans, and file lists inside `<details><summary>...</summary>...</details>` blocks.

---

## 2. Subagent & Tool Output Hygiene

- Offload broad codebase searches, log triage (`kubectl logs`, CI traces), and schema inspections to subagents or background tasks so raw output does not flood the primary session context.
- Summarize tool findings in 3 to 5 lines with exact `file:line` citations.

---

## 3. Anti-Bloat & Refactoring Standards

- **Reuse before adding:** Always inspect neighboring files and shared modules before writing new functions. Prefer refactoring existing functions over adding parallel helpers.
- **No duplicate blocks:** Never duplicate 5 or more consecutive lines of logic across files.
- **Hard batch cap (`<150 LOC`):** Keep changes focused and under 150 lines per commit/PR. If a task is larger, propose a 3-step stacked plan first.

---

## 4. Error Handling & Testing Guardrails

- **Forbid silent failures:** Never use empty catch blocks, broad exception suppression, or production fallback mocks. Surface errors explicitly with actionable context.
- **Behavioral tests only:** Test public contracts and failure paths. Never write tests that merely mirror the implementation or mock away the system under test.
