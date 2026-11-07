---
name: progressive-zoom
description: "Prevents coding assistants from dumping 5-paragraph walls of nitty-gritty detail in chat. Forces explanations, root-cause analyses, and codebase walkthroughs into three explicit zoom levels (Zoom 1: 30-Second Big Picture, Zoom 2: Mechanism & State Flow, Zoom 3: Line-by-Line Code), pausing between levels so you never lose the mental map. Use whenever asking how does this work, explain this module, why is this failing, or reviewing a multi-file change."
---

# Progressive Zoom: Big Picture First, Details on Demand

When explaining code, architecture, bugs, or query plans in chat, **never dump all levels of detail in a single response**. Human working memory saturates when low-level implementation trivia is mixed with high-level system structure.

Always follow this strict three-level **Progressive Disclosure** protocol and **stop after Zoom Level 1** unless the user explicitly asks to zoom in.

---

## Zoom Level 1: The 30-Second Mental Map (Default Response)

Every initial explanation must fit on one screen without scrolling (maximum 12 lines total):

1. **BLUF (Bottom Line Up Front: 1 to 2 sentences):** State what the system/change does, or what caused the bug, in plain engineering terms.
2. **Compact Flow Diagram (max 5 to 6 nodes):** Draw a one-line ASCII chain or compact Mermaid diagram showing only the entry point, core transformation, and storage/external boundary:
   `[Client Request] -> [AuthMiddleware] -> [OrderService] -> [Postgres Lock]`
3. **The 3 Key Boundaries (3 bullets max):** Name the 3 most important `file:line` locations and each component's single responsibility.
4. **Pause & Offer Zoom Controls:** End your message with this exact prompt:
   > **Zoom controls:** Reply **`1`** for Mechanism & State Transitions (locks, failure modes, trade-offs) or **`2`** for Nitty-Gritty Code & Query Details.

---

## Zoom Level 2: Mechanism, State Transitions & Trade-Offs (On Request Only)

Only provide Zoom Level 2 when the user asks to zoom in:

- **Happy-path vs. failure-path sequence:** How state changes step by step, where locks or network calls happen, and what can go wrong under concurrency.
- **Architectural trade-offs:** Why this design was chosen over alternatives, and what invariants callers must respect.
- **Pause before code dump:** End with:
  > **Zoom controls:** Reply **`2`** to inspect the exact line-by-line code, SQL queries, or edge-case branches for any step above.

---

## Zoom Level 3: Line-by-Line Nitty-Gritty (On Request Only)

Only provide Zoom Level 3 when the user asks for specific code lines, stack traces, or raw SQL plans:

- Show exact `startLine:endLine:filepath` code blocks.
- Walk through edge cases, error codes, and concrete test assertions.
- If raw logs or `EXPLAIN ANALYZE` outputs exceed 15 lines, wrap them inside a collapsible `<details><summary>Raw output</summary>...</details>` block so the chat remains scannable.
