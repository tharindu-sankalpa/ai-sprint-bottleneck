# LinkedIn Carousel Brief: Why Full-Stack AI Doesn't Make Teams 10x Faster

A document post on LinkedIn is a PDF that the feed renders as a swipeable carousel. This file is the complete brief for that PDF: how to produce it, the visual style, the rewritten narrative, the companion LinkedIn post copy, and the exact text, tables, diagrams, and numbers of every page. Every fact below comes from published 2025 and 2026 software engineering telemetry and empirical studies (**Faros AI**, **LinearB**, **GitClear**, **Google Cloud DORA**, **Harvard Business Review / Stanford / BetterUp**, **MSR '26 / arXiv**, **Atlassian**, **Microsoft Research**, and **METR**) and the **80-hour (`10 days × 8 hours`) full-lifecycle two-week sprint model**. Nothing in the pages should be changed, shortened, or invented by the design tool.

---

## How to produce it

Give **Claude Design** (or your design tool) this file in full and say:

> *"Read this brief in full and follow it exactly; add nothing that is not in it; run its closing checklist and report each item."*

1. **Verify every page against this brief:** numbers, units, percentages, stage names, and arrow directions. The tool must not add or reword facts.
2. **Export format:** PDF, **12 pages**, **4:5 portrait** (`1080 × 1350 px`, or `2160 × 2700 px` at 2× retina; also compatible with A4 portrait `210 × 297 mm` if exported as a standalone document). Keep 4:5 portrait as the primary feed choice so every slide fills the LinkedIn mobile viewport without letterboxing.
3. **File name:** `why-ai-everywhere-is-still-not-10x-delivery.pdf`. LinkedIn displays the uploaded PDF file name as the document title in the feed.
4. **Posting:** Upload the PDF with the companion LinkedIn post text at the end of this file. Links inside a LinkedIn PDF are not clickable, so study names are written out plainly on the slides and linked in the post text.

---

## What earlier versions got wrong (Do Not Reintroduce)

- **Do not assume engineers only use AI for typing code.** Modern engineers use AI agents (`Cursor`, `Claude Code`, MCP tools) across **all six stages of the sprint**: coding, debugging (`kubectl exec`, pod logs, port-forwarding, SQL queries, CI log triage), system design (RFCs, architecture drafts), sprint planning & meetings (AI meeting notes, slide decks, Jira ticket breakdowns), code review (AI review bots like `CodeRabbit`, `Copilot`, `Qodo`), and CI/CD YAML authoring.
- **Do not ignore the "Slop & Verification Rebound" in every stage.** Every stage gets a real **gross AI speedup** (`-35.5 hours` saved across an 80-hour sprint), AND every stage gets hit by a **verification, cleanup, and workslop tax** (`+35.5 hours` added back) from over-engineered code, `+81%` code duplication, `1 hr 56 min` per workslop design doc/slide deck, noisy review bots (`<30%` signal), and `+98%` more / `+154%` larger PRs.
- **Do not use Amdahl's 1967 IBM processor paper or the Concorde flight analogy.** Use the **Pipeline Bottleneck Rule (Theory of Constraints)** and the **1,000 ms API endpoint / microservice call-chain analogy** on Page 2.
- **Never join sibling pipeline stages with double-headed arrows.** Flow is strictly unidirectional with a single filled arrowhead at the destination card.
- **Every hour in the 2-week sprint must sum to exactly `80.0 hours` (`10 × 8h`)** in both the Pre-AI Baseline (`80.0 h`) and the Real-World Full-Stack AI Sprint (`80.0 h`), and **`44.5 hours`** in the Gross AI Speedup scenario before the slop and verification rebound.

---

## Rewritten Core Narrative (Full-Lifecycle AI Edition)

> **If AI helps with coding, debugging, design, code reviews, AND meeting notes, why isn't your engineering team shipping 10× faster?**
>
> Because of the **Pipeline Bottleneck Rule** (known in systems engineering as the *Theory of Constraints*). When you accelerate *generation* across every stage of a software pipeline, you shift the entire system’s bottleneck to **human verification, context recovery, and cleanup**.
>
> Every backend engineer has seen this in distributed systems. Imagine an API endpoint taking **1,000 ms** (`300 ms` app compute, `700 ms` database queries, serialization, and downstream calls). Suppose you optimize app compute by **10×** and put caching layers in front of the other stages so raw execution drops to **550 ms**. If that faster execution triggers **2× as many parallel requests** with **2.5× larger payloads** and retry storms from noisy cache misses, your database connection pool saturates, serialization overhead balloons, and end-to-end latency climbs right back to **1,000 ms**.
>
> **That is exactly what happens inside a 2-week (`10 × 8h = 80-hour`) AI-assisted sprint.**
>
> Today’s engineers don't just use AI to autocomplete functions. They use coding agents to run `kubectl` against Kubernetes pods, port-forward services, inspect CI/CD failure logs, and run SQL queries to debug. They use AI to draft system design RFCs, generate sprint slide decks, summarize meeting minutes, and run automated PR review bots.
>
> Across an **80-hour sprint**, using AI in all six stages saves a massive **35.5 hours of gross creation and triage time** (shrinking the raw workload from `80.0 hours` to `44.5 hours`, or **1.80× faster** on paper).
>
> **So where do those saved 35.5 hours go? They get eaten by the Verification & Slop Tax (`+35.5 hours`):**
>
> 1. **Coding (`24.0h → 5.0h gross → 8.0h net`):** AI writes code in `5.0h` (`-19.0h` saved), but engineers spend `+3.0h` untangling over-engineered abstractions, dead wrappers, and duplicated blocks ([GitClear’s 2026 study of 623M lines](https://www.gitclear.com/the_ai_code_quality_maintainability_gap) found refactoring collapsed **-70%** while code duplication jumped **+81%** and error-masking constructs rose **+47%**).
> 2. **Debugging, K8s/DB Triage & Testing (`12.0h → 6.5h gross → 14.5h net`):** Agents save `-5.5h` pulling pod logs, running SQL queries, and scaffolding unit tests. But engineers spend `+8.0h` debugging unfamiliar AI-authored logic they didn't write, chasing confident AI root-cause hallucinations ([Microsoft Research 2026](https://arxiv.org/pdf/2604.07830)), and fixing **+54% more bugs per developer** ([Faros AI 2026](https://www.faros.ai/blog/key-takeaways-from-the-dora-report-2025)).
> 3. **System Design & RFCs (`12.0h → 8.5h gross → 14.0h net`):** Prompting generates a 10-page architecture RFC in minutes (`-3.5h` saved). But reading, decoding, and correcting verbose, generic AI design docs adds `+5.5h` ([Stanford & BetterUp’s HBR study](https://hbr.org/2025/09/ai-generated-workslop-is-destroying-productivity) found **40%** of workers receive AI "workslop" costing **1 hour 56 minutes per incident** to decipher and redo, and [Faros AI](https://www.faros.ai/blog/key-takeaways-from-the-dora-report-2025) measured **+13.8% more task restarts** from flawed specs).
> 4. **Meetings, Slides & Sprint Planning (`12.0h → 8.5h gross → 12.0h net`):** AI writes meeting minutes, slide decks, and Jira tickets (`-3.5h` saved), but engineers spend `+3.5h` reading bloated AI summaries, cleaning up hallucinated ticket requirements, and syncing across **+67.4% more parallel PR contexts** per day.
> 5. **PR Code Review (`10.0h → 8.0h gross → 18.5h net`):** AI review bots save `-2.0h` on lint and syntax, yet [empirical MSR ’26 research](https://arxiv.org/html/2604.03196) shows **12 of 13 review bots have `<60%` signal** (and [Cihan et al.](https://arxiv.org/html/2412.18531v2) found review bots increased PR closure time by **+42%**, from `5h 52m` to `8h 20m`). Meanwhile, human reviewers face **+98% more PRs** that are **+154% larger** and wait **5.3× longer** to be picked up ([LinearB 2026](https://assets.linearb.io/image/upload/v1765300694/resources/LinearB_2026_Software_Engineering_Benchmarks_Report.pdf)), adding `+10.5h` of review load.
> 6. **CI/CD & Production Ops (`10.0h → 8.0h gross → 13.0h net`):** AI saves `-2.0h` parsing CI logs and writing Helm/Terraform YAML, but 2× PR volume clogs CI build queues, increases merge conflicts, and drives **+242.7% more production incidents per PR** ([Faros AI 2026](https://www.faros.ai/blog/key-takeaways-from-the-dora-report-2025)), adding `+5.0h` of operational firefighting.
>
> **The takeaway:** AI made *generating* code, docs, tests, and queries cheap. That shifted the bottleneck to **comprehension and verification**. Until teams enforce concise specs, small batch sizes (`<150 LOC`), and strict anti-slop guardrails, using AI everywhere just turns software engineers into full-time auditors of AI-generated noise.

---

## Brief for the Design Tool (12 Pages, 4:5 Portrait)

Design a 12-page document for a LinkedIn document post (PDF carousel). Pages are 4:5 portrait (`1080 × 1350 px`, rendered at 2× retina `2160 × 2700 px`). It is read inside the LinkedIn feed at phone width, so everything is large relative to the page: body text at least `1/36` of the page width (`60 px` on a `2160 px` canvas), captions, code, and table cells at least `1/45` of the page width (`48 px` on a `2160 px` canvas). Each page is one slide of a presentation: one idea, read in twenty to thirty seconds. Use only the text given below; do not add, reword, shorten, or invent any sentence, number, or study citation. If a page does not fit, do not shrink the type below the minimums; report which page overflowed.

### Style Rules

- **Canvas:** `#FAFAFA`. Primary text `#0F172A`, secondary text `#475569`. A thin rule in `#4F46E5` across the top of every page.
- **Three fixed elements per page:**
  1. Small-caps kicker in indigo `#4F46E5` at the top left (letter-spaced, `1/50` of page width).
  2. Bold two-line headline below it (`1/18` of page width) with one highlighted phrase in an accent colour.
  3. Page number `n/12` at the bottom right in secondary text `#475569`.
- **Typeface:** Inter (or clean geometric sans-serif) for headings and body; JetBrains Mono for time budgets, math blocks, and CLI/SQL snippets.
- **Palette (consistent across all slides and diagrams):**
  - Indigo `#4F46E5` (orchestration, primary framing, net math) with pale tint `#EEF2FF`
  - Blue `#2563EB` (hands-on coding & gross AI speedup) with pale tint `#EFF6FF`
  - Amber `#B45309` (PR review gate, workslop & verification tax) with pale tint `#FFFBEB`
  - Violet `#7C3AED` (debugging, K8s/DB agent triage & testing) with pale tint `#F5F3FF`
  - Teal `#0F766E` (system design, RFCs & architecture) with pale tint `#F0FDFA`
  - Slate `#334155` / `#475569` (sprint planning, meetings, CI/CD & ops) with pale tint `#F8FAFC`
  - Red `#B91C1C` (over-engineering, code duplication, bugs & prod incidents) with pale tint `#FFF1F2`
- **Diagram & Table Cards:** White or pale-tint fill, solid `3 px` outline in `#334155`, `12 px` corner radius, `6 px` coloured left accent bar. Arrows are `3 px` with a single filled triangular head at the destination only. Never use double-headed arrows.
- **Cover Illustration (Page 1 only):** One vector diagram in the middle two-fifths of Page 1 showing six sprint stage discs on the left (Coding, Debugging/K8s, Design, Planning/Docs, Review Bots, CI/CD) feeding high-velocity blue streams (`-35.5h Gross AI Speedup`) into a central amber verification funnel (`+35.5h Slop, Over-Engineering & Review Tax`, marked with a person-and-check icon), exiting as a modest `1.21x Net Delivery` arrow on the right over a faint dot grid. No stock photos, robots, or brains.

---

### Page 1 · Cover

Kicker: `FULL-LIFECYCLE AI · THE VERIFICATION BOTTLENECK`

Headline: `We use AI for coding, debugging, design, and docs. Why aren't we 10x faster?` (highlight "Why aren't we 10x faster?" in indigo `#4F46E5`)

Standfirst, one paragraph in secondary text: `Engineers now use AI across every stage of a 2-week sprint, from kubectl debugging and SQL triage to RFCs, meeting notes, and PR review bots. AI saves 35.5 hours of creation time per sprint, and then adds 35.5 hours of verification, cleanup, and "workslop" tax right back.`

Four numbered points, large numerals in indigo `#4F46E5`:

1. **AI is now full-lifecycle, not just autocomplete.** Agents write code, query pods and databases, draft designs, summarize meetings, and comment on PRs.
2. **Gross savings are real: -35.5 hours per 80-hour sprint.** Raw creation and log-triage time drops from 80.0 hours to 44.5 hours (1.80× faster before rework).
3. **The Slop & Verification Rebound eats +35.5 hours.** Over-engineered code (+81% duplication), verbose AI design docs (1h 56m lost per incident), noisy review bots, and 2× PR queues absorb the saved time.
4. **The bottleneck shifted from creation to verification.** You cannot ship faster than humans can understand and trust what AI generated.

Source badges row: `Faros AI (22k Devs)` · `LinearB (8.1M PRs)` · `GitClear (623M LOC)` · `Stanford / HBR` · `DORA`

Footer line in indigo italic: `The 80-hour full-stack AI sprint, stage by stage. Swipe →`

---

### Page 2 · The Systems Engineering Analogy

Kicker: `SYSTEMS THINKING · THE PIPELINE BOTTLENECK RULE`

Headline: `When generation gets 10x cheaper, verification saturates the pipeline` (highlight "verification saturates the pipeline" in amber `#B45309`)

Diagram card with two stacked horizontal microservice request timelines:

- **Timeline 1 · Baseline Request Pipeline (`1,000 ms total`):**
  - Blue `#2563EB` block (`300 ms`): `App Compute · 300 ms`
  - Slate `#475569` block (`700 ms`): `DB Queries + Serialization + Auth Gate · 700 ms`
- **Timeline 2 · 10x Compute + 2x Request Flood + 2.5x Payload Bloat (`1,000 ms total`):**
  - Blue `#2563EB` block (`30 ms`): `Compute · 30 ms`
  - Teal `#0F766E` block (`220 ms`): `Cached Lookups · 220 ms`
  - Red `#B91C1C` & Amber `#B45309` block (`750 ms`): `DB Lock Queue + Deserializing Bloated Payloads + Retry Storms · 750 ms`

Three bullets:

- **Speeding up creation changes downstream traffic.** In distributed systems, if an upstream service emits 2× more requests with 2.5× larger payloads, downstream serialization and database locks saturate.
- **This is the Theory of Constraints in software delivery.** Making every creation step faster (code, RFCs, slide decks, test scaffolds) floods the human comprehension gate.
- **Effort transfers from the sender to the receiver.** Saving 20 minutes by prompting a 2,000-word design doc or a 500-line PR costs your teammates 2 hours to read, verify, and untangle.

Footnote, secondary text: `In systems engineering, optimizing local throughput without bounding payload size increases queue wait time exponentially.`

---

### Page 3 · The 3 Sprint Realities (10 × 8h = 80 Hours)

Kicker: `THE 80-HOUR SPRINT · THREE REALITIES`

Headline: `AI saves 35.5 hours of creation, then adds 35.5 hours of verification` (highlight "saves 35.5 hours" in blue `#2563EB` and "adds 35.5 hours" in amber `#B45309`)

A 7-row comparison table across a 2-week (`10 days × 8 hours = 80.0 hours`) sprint:

| Sprint Stage | 1. Pre-AI (`80h`) | 2. Gross AI Speedup (`44.5h`) | 3. Slop & Review Rebound | 4. Net Real AI Sprint (`80h`) |
|---|---|---|---|---|
| **1. Hands-on coding** | `24.0 h` | `5.0 h` (`-19.0h`) | `+3.0 h` (cleanup) | **`8.0 h`** (`-16.0h`) |
| **2. Debugging, K8s/DB & tests** | `12.0 h` | `6.5 h` (`-5.5h`) | `+8.0 h` (AI bugs) | **`14.5 h`** (`+2.5h`) |
| **3. System design & RFCs** | `12.0 h` | `8.5 h` (`-3.5h`) | `+5.5 h` (doc slop) | **`14.0 h`** (`+2.0h`) |
| **4. Planning, meetings & slides** | `12.0 h` | `8.5 h` (`-3.5h`) | `+3.5 h` (sync/WIP) | **`12.0 h`** (`0.0h`) |
| **5. PR code review & approval** | `10.0 h` | `8.0 h` (`-2.0h`) | `+10.5 h` (2× PRs) | **`18.5 h`** (`+8.5h`) |
| **6. CI/CD, deploy & prod ops** | `10.0 h` | `8.0 h` (`-2.0h`) | `+5.0 h` (incidents) | **`13.0 h`** (`+3.0h`) |
| **Total Sprint / Net Velocity** | **`80.0 h` (1.0x)** | **`44.5 h` (1.80x paper)** | **`+35.5 h` rebound** | **`80.0 h` (~1.21x tasks)** |

Two bullets:

- **Row 2 (`44.5 h`) is what developers feel in the moment.** Every prompt saves time right now: writing a function, querying a pod, drafting a doc, or generating slides.
- **Row 4 (`80.0 h`) is what engineering telemetry actually records.** The `35.5 hours` saved in generation come back as `35.5 hours` of de-bloating code, verifying unfamiliar logic, reading workslop, and clearing PR queues.

Footnote, secondary text: `Net result: +21% to +34% more tasks completed (1.21x to 1.34x), while PR review + debugging jumps from 22.0h (27.5%) to 33.0h (41.3%).`

---

### Page 4 · Stage 1: Hands-On Coding & Over-Engineering

Kicker: `STAGE 1 · HANDS-ON CODING (24.0h → 8.0h)`

Headline: `Coding is 3x faster once you strip out the over-engineered bloat` (highlight "over-engineered bloat" in red `#B91C1C`)

Math & Telemetry Strip inside a dark `#1E293B` card:

```text
Pre-AI Coding:            24.0 h (30% of sprint)
Gross AI Generation:       5.0 h (-19.0 h saved writing boilerplate & endpoints)
De-Slop & Refactor Tax:   +3.0 h (deleting wrappers, dead abstractions & clones)
Net AI Coding Time:        8.0 h (-16.0 h net saved · 3.0x faster, not 10x)
```

Four empirical signals from **GitClear's 2026 study (623 million changed lines of code, 2023 to 2026)**:

- **Refactoring collapsed `-70%`:** Moved/modularized lines fell from `21%` (pre-AI) to `3.8%` in 2026 as developers default to "write-only" generation.
- **Code duplication jumped `+81%`:** Repeated 5+ line blocks hit an all-time high (`+41%` within-commit copy/paste), creating a multi-file propagation tax.
- **Error-masking constructs rose `+47%`:** AI frequently wraps failing logic in defensive `try/catch`, null-guards, and fallback mocks that hide root causes.
- **Legacy maintenance dropped `-74%`:** LinearB (2026) confirms human PRs do **1.5× more refactoring** than AI PRs (`0.37` vs `0.17` refactor rate); AI strongly biases toward adding new layers instead of simplifying existing code.

Footnote, secondary text: `Sources: GitClear Maintainability Gap Report (2026, 623M changed lines); LinearB Software Engineering Benchmarks (2026, 8.1M PRs).`

---

### Page 5 · Stage 2: Debugging, K8s/DB Agents & Testing

Kicker: `STAGE 2 · DEBUGGING, K8S/DB TRIAGE & TESTING (12.0h → 14.5h)`

Headline: `Agents gather pod logs and SQL fast, but AI code creates 54% more bugs` (highlight "54% more bugs" in red `#B91C1C`)

Two-column comparison card:

- **Left Column · Gross AI Triage Speedup (`-5.5 h` saved, blue `#2563EB` bar):**
  - Agents run `kubectl logs`, `kubectl exec`, and port-forward services automatically.
  - Agents connect to Postgres, inspect schemas, and run diagnostic SQL queries.
  - Agents read CI/CD stack traces and scaffold unit/integration test suites (`12.0 h → 6.5 h`).
- **Right Column · Verification & Bug Rebound (`+8.0 h` added, red `#B91C1C` bar):**
  - **Debugging code nobody wrote:** Diagnosing a bug in AI-authored code requires learning the code from scratch during the incident.
  - **Confident false hypotheses:** Microsoft Research (2026) found agents frequently state wrong root causes with high confidence, sending engineers down dead-end debugging paths.
  - **Tautological unit tests:** AI-generated tests often assert the buggy implementation (`mocking the bug`), passing CI while leaking defects (`+54%` bugs/dev in Faros 2026).

Bottom summary bar: `12.0 h baseline - 5.5 h agent triage + 8.0 h debugging AI edge cases = 14.5 h net (+2.5 h increase).`

Footnote, secondary text: `Sources: Microsoft Research & OSU "To Copilot and Beyond" (2026, n=860); Faros AI 2026 Report (22,000 devs); DORA 2025.`

---

### Page 6 · Stage 3: System Design & Architecture RFCs

Kicker: `STAGE 3 · SYSTEM DESIGN & ARCHITECTURE (12.0h → 14.0h)`

Headline: `A 10-page AI design doc takes 5 minutes to prompt and 2 hours to decode` (highlight "2 hours to decode" in amber `#B45309`)

Three stacked evidence cards:

- **Card 1 · The Gross Speedup (`-3.5 h` saved, teal `#0F766E` bar):** Feeding business requirements into an LLM produces a formatted RFC, schema draft, and trade-off table in minutes (`12.0 h → 8.5 h`).
- **Card 2 · The "Workslop" Tax (`+5.5 h` added, amber `#B45309` bar):** Harvard Business Review, Stanford, and BetterUp (2025, `n=1,150`) found **40% of workers** receive AI "workslop": polished, lengthy documents that lack real project context. Recipients spend an average of **1 hour 56 minutes per incident** deciphering, verifying, and rewriting it.
- **Card 3 · Spec Drift & Task Restarts (`+13.8%` restarts, red `#B91C1C` bar):** Microsoft Research (2026) found one-shot AI designs default to generic textbook patterns and silently invent requirements. Faros AI (2026) measured a **`+13.8%` increase in task restarts** (work moving backward to in-progress) when teams build on unverified specs.

Bottom summary bar: `12.0 h baseline - 3.5 h drafting + 5.5 h de-slopping specs & restarts = 14.0 h net (+2.0 h increase).`

Footnote, secondary text: `Sources: Niederhoffer, Hancock et al., Harvard Business Review / Stanford / BetterUp (2025); Microsoft Research (2026); Faros AI (2026).`

---

### Page 7 · Stage 4: Sprint Planning, Meetings & Presentations

Kicker: `STAGE 4 · MEETINGS, SLIDES & PLANNING (12.0h → 12.0h)`

Headline: `AI writes the meeting notes and slides, then parallel WIP eats the savings` (highlight "parallel WIP eats the savings" in amber `#B45309`)

Math & Workflow Breakdown:

- **Where AI saves `-3.5 hours` (`12.0 h → 8.5 h`):**
  - Auto-transcribing meeting minutes and action items.
  - Generating sprint review slide decks and status summaries.
  - Breaking epics into draft Jira tickets and subtasks.
- **Where `+3.5 hours` immediately comes back (`8.5 h → 12.0 h`):**
  - **Document & ticket inflation:** When a 5-bullet update becomes a 3-page AI summary or 15 verbose Jira tickets, teammates spend the saved time reading and pruning noise (`45.9%` of Microsoft devs cited doc drift/slop as a top problem).
  - **`+67.4%` more daily PR contexts:** Faros AI (2026) found engineers orchestrating multiple AI agents juggle **67.4% more PR contexts** and **17.7% more task contexts** every day.
  - **`+26%` more stalled tasks:** Tasks sitting `7+ days` with no progress rose `26%`, requiring extra standup, triage, and re-planning coordination.

Footnote, secondary text: `Net planning & coordination time stays flat at 12.0 hours: fast artifact generation is canceled out by multi-agent coordination overhead.`

---

### Page 8 · Stage 5: PR Code Review & AI Review Bots

Kicker: `STAGE 5 · CODE REVIEW & AI REVIEW BOTS (10.0h → 18.5h)`

Headline: `Why don't AI code review agents solve the PR review bottleneck?` (highlight "solve the PR review bottleneck?" in amber `#B45309`)

Four stat tiles in a 2 × 2 grid from empirical 2025 and 2026 PR review studies:

- Tile 1 (amber `#B45309` accent): **`12 of 13` Bots `<60%` Signal** (MSR ’26 study of 3,109 PRs found 60.2% of closed bot-reviewed PRs had `<30%` actionable comments; noise drove higher PR abandonment).
- Tile 2 (red `#B91C1C` accent): **`+42%` Longer PR Closure** (Industrial study of 1,568 automated PRs found adding an LLM review bot raised average PR closure time from `5h 52m` to `8h 20m` due to false-positive comment resolution).
- Tile 3 (amber `#B45309` accent, person-and-check mark): **`5.3x` Longer Pickup Wait** (LinearB across 8.1M PRs found Agentic AI PRs wait `17.6 hours` at P75 for a human to open them vs `3.2 hours` for manual PRs, and `<60%` get accepted).
- Tile 4 (red `#B91C1C` accent): **`+91% to +441%` Review Time** (Faros AI found high-AI teams merge `+98%` more PRs that are `+154%` larger, doubling review time in 2025 at `+91%` and surging `+441%` in 2026).

Two bullets:

- **AI review bots catch syntax (`-2.0 h`), not architectural intent.** A bot can flag a missing null check, but it cannot verify whether a 400-line diff belongs in the service at all.
- **31% more PRs now merge with zero review.** When review queues overload (`10.0 h → 18.5 h`), reviewers either rubber-stamp or ignore PRs, pushing defects straight to production.

Footnote, secondary text: `Sources: Chowdhury et al. (MSR '26, 3,109 PRs); Cihan et al. (2025, 4,335 PRs); LinearB (2026, 8.1M PRs); Faros AI (2025/2026).`

---

### Page 9 · Stage 6: CI/CD Pipelines, Deployments & Production Ops

Kicker: `STAGE 6 · CI/CD, DEPLOY & PROD OPS (10.0h → 13.0h)`

Headline: `AI writes the Helm chart, and 2x PR volume triples production incident risk` (highlight "triples production incident risk" in red `#B91C1C`)

Three stacked cards:

- **Card 1 · Gross AI Ops Speedup (`-2.0 h` saved, blue `#2563EB` bar):** AI assistants draft GitHub Actions, Dockerfile, Terraform, and Kubernetes manifests, and summarize opaque CI build failure logs (`10.0 h → 8.0 h`).
- **Card 2 · CI Queue & Merge Conflict Contention (`+2.0 h` added, amber `#B45309` bar):** Pushing `+98%` more PRs with `+154%` larger diffs into the same CI/CD pipeline causes build queues, flaky integration test retries, and rebase storms.
- **Card 3 · The Production Incident Whiplash (`+3.0 h` added, red `#B91C1C` bar):** Faros AI's 2026 telemetry across 22,000 developers found **incidents per PR jumped `+242.7%`** (more than 3.4× higher probability of a production incident per merged change) as larger, rubber-stamped diffs hit production.

Bottom summary bar: `10.0 h baseline - 2.0 h YAML/log help + 5.0 h CI contention & incident triage = 13.0 h net (+3.0 h increase).`

Footnote, secondary text: `Sources: Faros AI "The Acceleration Whiplash" (2026, 22,000 developers); DORA 2025 State of AI-Assisted Software Development.`

---

### Page 10 · Why It Still Feels 10x Faster (The Perception Gap)

Kicker: `COGNITIVE BIAS · CREATION VS. VERIFICATION`

Headline: `Generating 500 lines in 10 seconds feels like 10x; auditing it for 2 hours feels invisible` (highlight "feels invisible" in indigo `#4F46E5`)

Comparison block from the **METR Randomized Controlled Trial** (experienced maintainers on mature repos averaging `1M+ LOC` and `22k+ stars`, screen-recorded across 246 real issues):

- **Before starting:** Developers predicted AI would make them **`24% faster`**.
- **After finishing:** Developers believed AI had made them **`20% faster`**.
- **Actual stopwatch telemetry:** Tasks took **`19% longer`** in the 2025 RCT (and only `4% to 18% faster` in the 2026 follow-up).

Three bullets:

- **Creation has high dopamine; verification has high cognitive drag.** Watching an agent generate a feature, a design doc, or a SQL query feels effortless, so our brains anchor on the 5-minute prompt rather than the 90 minutes spent fixing subtle bugs.
- **UC Berkeley eye-tracking study (DORA 2025):** Developers used AI heavily on mechanical boilerplate (`19%` visual attention) but ignored it on complex code interpretation (`<1%` attention) to retain mental control.
- **Bounded Delegation (Microsoft Research 2026):** Across 860 developers, engineers wanted AI to automate *assembly and evidence collection*, never final architectural judgment or production sign-off.

Footnote, secondary text: `Sources: METR RCT (July 2025 & Feb 2026 update); DORA Insights / UC Berkeley Study (2025); Choudhuri et al., Microsoft Research (2026).`

---

### Page 11 · The Playbook: How to Actually Speed Up the Sprint

Kicker: `THE ENGINEERING PLAYBOOK · CUTTING THE SLOP TAX`

Headline: `To keep the 35.5 hours AI saves, engineer strict anti-slop guardrails` (highlight "strict anti-slop guardrails" in indigo `#4F46E5`)

Five actionable rules, each with a coloured left bar and bold lead:

- **1. Ban raw "workslop" in RFCs and tickets (Teal `#0F766E` bar):** Require every author to verify and condense AI-generated designs into a 1-page constraints-and-tradeoffs brief before sharing. Never make teammates read unedited LLM output.
- **2. Enforce hard PR size caps (`<150 LOC`) & DRY gates (Blue `#2563EB` bar):** Configure coding agents (`CLAUDE.md` / `.cursorrules`) to reuse existing modules, forbid speculative wrappers, and split changes into small, stacked PRs.
- **3. Shift AI code review left to the IDE, not the PR queue (Amber `#B45309` bar):** Run AI review and static checks *before* `git push` (DORA 2025). Restrict PR bots to high-signal security and bug rules so human reviewers aren't buried in `<30%`-signal noise.
- **4. Use agents for read-only K8s/DB evidence bundles (Violet `#7C3AED` bar):** Let agents correlate pod logs, traces, and SQL queries into a cited incident brief, but require explicit human verification before applying patches.
- **5. Track Review Wait, Rework Rate, and Incidents/PR (Indigo `#4F46E5` bar):** Stop celebrating PR count or lines generated. Measure end-to-end cycle time and 14-day code churn.

Footnote, secondary text: `Synthesized from DORA 2025 AI Capabilities Model, GitClear 2026 Maintainability Playbook, and Microsoft Research Bounded Delegation.`

---

### Page 12 · Final Summary & Sources

Kicker: `THE TAKEAWAY · FULL-LIFECYCLE REALITY CHECK`

Headline: `AI made creation cheap. Verification is now the engineering job.` (highlight "Verification is now the engineering job." in indigo `#4F46E5`)

Three summary cards stacked:

- Badge `-35.5 h` (blue `#2563EB` bar): **Gross AI Speedup is real across all 6 stages.** Coding (`-19h`), debugging/K8s/SQL triage (`-5.5h`), RFC drafting (`-3.5h`), meetings/slides (`-3.5h`), review bots (`-2h`), and CI/CD (`-2h`) cut raw creation time from `80h` to `44.5h`.
- Badge `+35.5 h` (amber `#B45309` bar): **Undisciplined AI gives every hour back as Slop & Review Tax.** Over-engineered code (`+3h`), AI bug triage (`+8h`), design workslop (`+5.5h`), parallel WIP (`+3.5h`), 2× PR review queues (`+10.5h`), and prod incidents (`+5h`) refill the `80h` sprint.
- Badge `The Fix` (indigo `#4F46E5` bar): **Don't ask "How fast can AI write this?"** Ask: **"How fast can another engineer verify, review, and debug what AI just produced?"**

Primary Research Citations (listed cleanly at bottom):
- `Faros AI (2025 & 2026) · AI Productivity Paradox (10k devs) & Acceleration Whiplash (22k devs)`
- `LinearB (2026) · Software Engineering Benchmarks Report: AI Productivity Edition (8.1M+ PRs)`
- `GitClear (2025 & 2026) · The Maintainability Gap: AI Code Quality (623M changed lines)`
- `Harvard Business Review / Stanford / BetterUp (2025) · AI-Generated "Workslop" Study (n=1,150)`
- `Microsoft Research & OSU (2026) · To Copilot and Beyond (n=860) · MSR '26 CRA Study (3,109 PRs)`
- `Google Cloud DORA Report (2025) · Atlassian State of DevEx (2025) · METR RCT (2025/2026)`

---

## Companion LinkedIn Post Text (Ready to Copy & Paste)

```text
"Wait, we don't just use AI for writing code anymore. We use it to debug Kubernetes pods, run SQL queries, draft design docs, write meeting notes, and review PRs. Shouldn't the whole sprint be 10× faster now?"

It is the best counter-argument in software engineering right now. So I looked at the 2025 and 2026 telemetry across all 6 stages of a 2-week sprint (10 days × 8 hours = 80 hours) to see what actually speeds up and what slows down.

Here is the plot twist:

When you use AI across EVERY stage of an 80-hour sprint, you genuinely save ~35.5 hours of gross creation and triage time (80h → 44.5h).

Then the "Slop & Verification Tax" adds +35.5 hours right back:

1. Hands-on Coding (24h → 5h gross → 8h net):
AI generates endpoints and boilerplate in 5h (-19h saved). But GitClear's 2026 analysis of 623M lines of code found refactoring collapsed -70%, code duplication jumped +81%, and error-masking constructs rose +47%. Engineers spend +3h stripping out over-engineered wrappers and dead abstractions.

2. Debugging, K8s/DB Triage & Testing (12h → 6.5h gross → 14.5h net):
Coding agents save -5.5h running kubectl exec, reading pod/CI logs, port-forwarding, and running SQL queries. However, debugging unfamiliar AI code you didn't write, chasing confident AI root-cause hallucinations (Microsoft Research, 2026), and fixing +54% more bugs/dev (Faros AI, 2026) adds +8h back.

3. System Design & RFCs (12h → 8.5h gross → 14h net):
Prompting drafts a 10-page RFC in minutes (-3.5h saved). Yet Stanford & BetterUp's HBR study found 40% of workers are getting hit with AI "workslop": polished, verbose docs missing real system context that cost recipients 1 hr 56 min per incident to decode and redo (+5.5h added, plus +13.8% task restarts).

4. Meetings, Slides & Sprint Planning (12h → 8.5h gross → 12h net):
AI writes the meeting minutes, slide decks, and Jira subtasks (-3.5h saved). Then engineers spend +3.5h filtering bloated auto-generated tickets and context-switching across +67.4% more parallel PR streams per day.

5. PR Code Review & AI Review Bots (10h → 8h gross → 18.5h net):
What about AI code review bots? An MSR '26 study of 3,109 PRs found 12 of 13 review bots have <60% signal (mostly noisy comments), and an industrial study (Cihan et al.) found PR closure time actually rose +42% (5h52m → 8h20m) after bot adoption. Meanwhile, human reviewers face +98% more PRs that are +154% larger and wait 5.3× longer for pickup (LinearB, 8.1M PRs). Net review load jumps +8.5h.

6. CI/CD & Production Ops (10h → 8h gross → 13h net):
AI saves -2h writing Helm/Terraform YAML and reading CI errors, but 2× PR volume clogs CI queues and drives +242.7% more production incidents per PR (Faros AI, 2026), adding +5h of ops firefighting.

In systems engineering, this is the Pipeline Bottleneck Rule: when generation becomes nearly free across every stage, human verification becomes the bottleneck for the entire system.

Swipe through the 12-page breakdown below for the stage-by-stage 80-hour sprint math, the telemetry citations, and the 5 guardrails high-performing teams use to keep the 35.5 hours AI saves.
```

---

## Closing Checklist for the Design Tool

- [ ] **12 pages total**, 4:5 portrait (`1080 × 1350 px` or `2160 × 2700 px`), numbered `1/12` through `12/12`.
- [ ] **Page 1** includes the 6-into-1 verification funnel vector illustration, 4 numbered points, and 5 source badges.
- [ ] **Page 2** uses the `1,000 ms` distributed microservice pipeline analogy (no Amdahl's 1967 paper, no Concorde flight).
- [ ] **Page 3** table sums match exactly:
  - Pre-AI Baseline: `24.0 + 12.0 + 12.0 + 12.0 + 10.0 + 10.0 = 80.0 h`
  - Gross AI Speedup: `5.0 + 6.5 + 8.5 + 8.5 + 8.0 + 8.0 = 44.5 h` (`-35.5 h` saved)
  - Slop & Verification Rebound: `+3.0 + 8.0 + 5.5 + 3.5 + 10.5 + 5.0 = +35.5 h`
  - Net Real-World AI Sprint: `8.0 + 14.5 + 14.0 + 12.0 + 18.5 + 13.0 = 80.0 h`
- [ ] **Pages 4 to 9** cover each of the 6 sprint stages in order with exact gross savings, rebound hours, and study citations.
- [ ] **No text overflows any card**, and body text is at least `1/36` of page width (`captions/tables >= 1/45`).
