# Anti-Slop & Mental-Map Engineering Instructions (GEMINI.md)

Copy this file to `./GEMINI.md` (repository root) or `~/.gemini/GEMINI.md` (global user config for **Gemini CLI** and **Gemini Code Assist**).

---

## 1. Output Style: Bottom Line Up Front (BLUF)

- **Start with the 1-sentence takeaway:** State the answer, root cause, or completed change in the very first sentence. Omit greetings, preambles, and closing recaps.
- **Preserve the mental map:** Summarize multi-file mechanisms in 3 to 5 bullets or a compact diagram (max 6 nodes) before showing code snippets.
- **After code edits:** Output only the list of modified files (`path:line`) and the test command run. Do not narrate line-by-line edits in prose.
- **Progressive disclosure:** Never dump 5 paragraphs of low-level details unprompted. Provide the high-level summary first and ask if I want to drill into specific modules or edge cases.

---

## 2. Codebase Hygiene & Small Batches

- **Consolidate, do not duplicate:** Check existing modules before writing new code. Refactor shared logic rather than copy-pasting 5+ line blocks or adding wrapper layers.
- **Small, reviewable diffs (`<150 LOC`):** If a requested change will exceed 150 lines of code or touch more than 4 files, pause and output a short numbered implementation plan before editing files.
- **No silent error masking:** Never swallow exceptions in `try/catch` blocks or return silent default values on failure.
- **Test real behavior:** Write tests that verify contracts and fail when the bug is reintroduced; avoid tautological mocks.
