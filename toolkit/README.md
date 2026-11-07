# The Anti-Slop Engineering Toolkit: Rules, Skills, Subagents & Prompts

This directory contains ready-to-use configuration files, skills, subagents, and prompt templates designed to eliminate **in-chat walls of text**, **write-only code bloat (`+81%` clones)**, **silent error masking (`+47%`)**, **10-page design workslop (`1h 56m` tax)**, and **PR review logjams (`+91%` to `+441%`)**.

Every file is plain Markdown or TOML and works out of the box with **Claude Code**, **Cursor**, **OpenAI Codex CLI**, and **Google Gemini CLI**.

---

## 1. What Is Inside This Toolkit

```text
toolkit/
├── README.md                                          This setup and usage guide
├── CLAUDE.md                                          Drop-in instructions for Claude Code (./CLAUDE.md or ~/.claude/CLAUDE.md)
├── AGENTS.md                                          Drop-in instructions for Codex CLI, Cursor, Windsurf, Zed & Amp (./AGENTS.md)
├── GEMINI.md                                          Drop-in instructions for Gemini CLI & Code Assist (./GEMINI.md)
├── codex-config.toml                                  Low-verbosity config for OpenAI Codex CLI (~/.codex/config.toml)
├── cursor-rules/
│   └── anti-slop-and-bluf.mdc                         Always-on Cursor rule (.cursor/rules/anti-slop-and-bluf.mdc)
├── skills/
│   ├── progressive-zoom/
│   │   ├── SKILL.md                                   3-level Progressive Zoom skill (stops 5-paragraph chat dumps)
│   │   └── agents/openai.yaml                         Codex UI & invocation metadata
│   ├── debloat-audit/
│   │   ├── SKILL.md                                   Post-coding De-Bloat & Silent-Failure Audit skill
│   │   └── agents/openai.yaml                         Codex UI & invocation metadata
│   ├── one-page-rfc/
│   │   ├── SKILL.md                                   1-page RFC/ADR & WIP=1 task slicer (stops 10-page doc workslop)
│   │   └── agents/openai.yaml                         Codex UI & invocation metadata
│   └── pre-push-review/
│       ├── SKILL.md                                   Local shift-left PR audit (<150 LOC, clones, silent failures, weak tests)
│       └── agents/openai.yaml                         Codex UI & invocation metadata
├── agents/
│   ├── mental-map-explorer.md                         Isolated subagent that returns a 15-line Mental Map Brief
│   └── debloat-and-silent-failure-auditor.md          Subagent that strips duplicate blocks & silent try/catch wrappers
└── templates/
    └── stage-by-stage-prompts.md                      Copy-paste prompts & CI gates for all 6 stages of the sprint
```

---

## 2. Quick Setup by Coding Assistant (60 Seconds)

### Option A: Claude Code (`claude`)

1. **Turn on built-in Concise output style** (stops conversational preamble and recaps immediately):
   ```bash
   # Inside a Claude Code session:
   /output-style concise
   ```
2. **Install the instruction file, 4 skills, and 2 subagents** (either in your project root or globally in `~/.claude/`):
   ```bash
   # Global User-level (applies to every repo you open):
   mkdir -p ~/.claude/skills ~/.claude/agents
   cp toolkit/CLAUDE.md ~/.claude/CLAUDE.md
   cp -r toolkit/skills/* ~/.claude/skills/
   cp toolkit/agents/*.md ~/.claude/agents/

   # Or Project-level (so your whole team shares the guardrails):
   cp toolkit/CLAUDE.md ./CLAUDE.md
   mkdir -p .claude/skills .claude/agents
   cp -r toolkit/skills/* .claude/skills/
   cp toolkit/agents/*.md .claude/agents/
   ```
3. **Invoke the skills in Claude Code:**
   - `/progressive-zoom` — Explain architecture or bugs in 3 zoom levels (`30-sec map -> state flow -> code`).
   - `/debloat-audit` — Strip duplicate 5+ line blocks, single-use wrappers, and silent `try/catch` fallbacks.
   - `/one-page-rfc` — Draft a 1-page (`<=350-word`) RFC/ADR with a `WIP=1` stacked PR plan.
   - `/pre-push-review` — Run a shift-left audit on `git diff` before pushing.
4. **Recommended Official Claude Code Plugins** (from `anthropics/claude-plugins-official`):
   - **`pr-review-toolkit`:** Includes specialized local pre-PR agents (`code-simplifier`, `silent-failure-hunter`, `pr-test-analyzer`).
   - **`feature-dev`:** Enforces a 7-phase *Discovery -> Codebase Exploration -> Clarifying Questions -> Architecture Options -> Implementation* workflow so agents never jump straight into writing unapproved code.
   - **`hookify`:** Lets you create `.claude/hookify.*.local.md` pre-tool and stop hooks (for example, blocking `stop` if tests were not run).

---

### Option B: Cursor IDE & Cursor CLI

1. **Install the 4 skills globally (`~/.cursor/skills/`) and add the `.mdc` rule to your project:**
   ```bash
   # Global skills (available across all projects in Cursor):
   mkdir -p ~/.cursor/skills
   cp -r toolkit/skills/* ~/.cursor/skills/

   # Project-level always-on rule + AGENTS.md:
   mkdir -p .cursor/rules .cursor/skills
   cp toolkit/cursor-rules/anti-slop-and-bluf.mdc .cursor/rules/
   cp toolkit/AGENTS.md ./AGENTS.md
   cp -r toolkit/skills/* .cursor/skills/
   ```
2. **Use Cursor's built-in visual, planning, and skill commands to protect your mental map:**
   - Type **`/progressive-zoom`**, **`/debloat-audit`**, **`/one-page-rfc`**, or **`/pre-push-review`** in Cursor chat to invoke the installed skills.
   - Press **`Shift+Tab` (Plan Mode)** for any change touching more than 2 files so you approve a short plan before code is generated.
   - Type **`/visualize`** in chat when asking how modules interact so Cursor draws a compact diagram instead of 5 paragraphs of text.

---

### Option C: OpenAI Codex CLI (`codex`)

1. **Install the 4 skills into `~/.codex/skills/` (and `~/.agents/skills/`), copy `AGENTS.md`, and set low verbosity in `~/.codex/config.toml`:**
   ```bash
   mkdir -p ~/.codex/skills ~/.agents/skills
   cp toolkit/AGENTS.md ~/.codex/AGENTS.md
   cp toolkit/AGENTS.md ./AGENTS.md
   cp -r toolkit/skills/* ~/.codex/skills/
   cp -r toolkit/skills/* ~/.agents/skills/

   # If you do not already have a custom ~/.codex/config.toml:
   cp toolkit/codex-config.toml ~/.codex/config.toml
   ```
   *(If you already have an existing `~/.codex/config.toml`, add `personality = "pragmatic"`, `model_verbosity = "low"`, `hide_agent_reasoning = true`, and `model_reasoning_summary = "concise"` at the top level.)*
2. **Invoke the skills in Codex:**
   - Reference `$progressive-zoom`, `$debloat-audit`, `$one-page-rfc`, or `$pre-push-review` in your prompt (or run `/skills` inside `codex`).

---

### Option D: Google Gemini CLI & Gemini Code Assist (`gemini`)

1. **Copy `GEMINI.md` to your repository root (or `~/.gemini/GEMINI.md`):**
   ```bash
   cp toolkit/GEMINI.md ./GEMINI.md
   ```

---

## 3. How Each Tool Maps to the 6 Sprint Stages

| Sprint Stage | The AI Trap (`+35.5 h` Rebound) | Toolkit File / Industry Mitigation |
|---|---|---|
| **All Stages (Chat UI)** | 5-paragraph walls of nitty-gritty detail bury the big picture | `CLAUDE.md` / `AGENTS.md` (BLUF shape rules) + `skills/progressive-zoom/SKILL.md` + `agents/mental-map-explorer.md` |
| **1. Hands-on Coding** | `-70%` refactoring, `+81%` duplicate blocks, `+47%` silent error wrappers | `agents/debloat-and-silent-failure-auditor.md` + `jscpd --baseline-from-ref origin/main --fail-on-new-clones` in CI |
| **2. Debugging & Testing** | No mental map of AI code, false root causes, self-passing unit tests (`<60%` mutation score) | `agents/mental-map-explorer.md` + Prompt 2A/2B + Mutation testing on changed files (`Stryker` / `mutmut`) |
| **3. System Design & RFCs** | `1 hr 56 min` lost per 10-page "workslop" RFC; `+13.8%` task restarts | `skills/one-page-rfc/SKILL.md` (1-page RFC/ADR cap, trade-off table, collapsible `<details>` appendix) |
| **4. Sprint Planning** | Ticket inflation, `+67.4%` parallel PR contexts, `+26%` stalled tasks | `skills/one-page-rfc/SKILL.md` (`WIP = 1` rule + mandatory executable Completion Evidence per task) |
| **5. PR Code Review** | `2×` PRs, `+154%` larger diffs, `5.3×` pickup wait, `<30%`-signal PR bots | `skills/pre-push-review/SKILL.md` (shift review left to IDE) + Stacked PRs (`<150 LOC` via `gh stack` or Graphite) |
| **6. CI/CD & Prod Ops** | `2×` CI queue contention, `31%` unreviewed merges, `+242.7%` prod incidents/PR | Scoped/batched merge queues (Mergify/Trunk) + Blast-radius budgets (feature flags + canary auto-rollback) |
