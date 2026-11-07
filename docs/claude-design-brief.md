# LinkedIn Carousel Brief: Why Full-Stack AI Doesn't Make Teams 10x Faster

A document post on LinkedIn is a PDF that the feed renders as a swipeable carousel. This file is the complete brief for that PDF: how to produce it, the visual style, the core narrative, the companion LinkedIn post copy, and the exact text, tables, diagrams, and numbers of every page. Every fact below comes from published 2025 and 2026 software engineering studies (**Faros AI**, **LinearB**, **GitClear**, **Google Cloud DORA**, **Harvard Business Review / Stanford / BetterUp**, **MSR '26 / arXiv**, **Atlassian**, **Microsoft Research**, and **METR**) mapped onto an **80-hour (`10 days × 8 hours`) two-week engineering sprint**. Nothing in the pages should be changed, shortened, or invented by the design tool.

> **Where the numbers in this brief come from:**
> - **Measured in published studies (real data):** All percentages, PR sizes, wait times, and incident rates (`30% → 10%` coding share, `+81%` duplicate blocks, `1 hr 56 min` per "workslop" doc, `+98%` more PRs at `+154%` size, `+242.7%` incidents per PR) come directly from the published 2025 to 2026 studies cited on each slide.
> - **Illustrative 80-hour sprint math (`-35.5 h` saved, `+35.5 h` added back):** To show all six stages on one timeline, those published percentages are converted into hours across a single hypothetical two-week (`80-hour`) sprint. Both Page 1 (Cover) and Page 3 state this directly on the slide so readers never mistake the hour totals for one team's stopwatch log.

---

## How to produce it

1. **Generate the four `3:4` portrait diagrams** (`1792 × 2400`) from `docs/nano-banana-prompts.md` (Part B) and save them into `docs/diagrams/`:
   - `docs/diagrams/li-01-sprint-tug-of-war.jpg` (optional; **Page 3** now uses the six-stage hours table below instead of this diagram, so it is only needed if you prefer the visual)
   - `docs/diagrams/li-02-bloat-and-mental-map.jpg` (article-only; **Page 5** now uses a native two-sided bar chart instead, see its spec below)
   - `docs/diagrams/li-03-verification-funnel.jpg` (article-only; **Page 11** now uses a native funnel diagram, see its spec below)
   - `docs/diagrams/li-04-chat-zoom-and-stage-gates.jpg` (article-only; **Page 12** now uses a native two-part diagram, see its spec below)
2. Give **Claude Design** (or your design tool) this file in full plus those four portrait diagram images and say:

> *"Read this brief in full and follow it exactly; add nothing that is not in it; build the native diagrams on Pages 5, 11, and 12 exactly as specified; run its closing checklist and report each item."*

3. **Verify every page against this brief:** numbers, units, percentages, stage names, and arrow directions. The tool must not add or reword facts.
4. **Export format:** PDF, **13 pages**, **4:5 portrait** (`1080 × 1350 px`, or `2160 × 2700 px` at 2× retina; also compatible with A4 portrait `210 × 297 mm` if exported as a standalone document). Keep 4:5 portrait as the primary feed choice so every slide fills the LinkedIn mobile viewport without letterboxing.
5. **File name:** `why-ai-everywhere-is-still-not-10x-delivery.pdf`. LinkedIn displays the uploaded PDF file name as the document title in the feed.
6. **Posting:** Upload the PDF with the companion LinkedIn post text at the end of this file. Links inside a LinkedIn PDF are not clickable, so study names are written out plainly on the slides and linked in the post text.

---

## Key Rules for This Brief

- **Show how engineers use AI across all six stages of the sprint:** coding, debugging (`kubectl exec`, pod logs, port-forwarding, SQL queries, CI log checks), system design (RFCs, architecture drafts), sprint planning & meetings (AI meeting notes, slide decks, Jira ticket breakdowns), code review (AI review bots like `CodeRabbit`, `Copilot`, `Qodo`), and CI/CD YAML configuration.
- **Show both the initial AI time savings and the cleanup/review rebound in every stage:** Every stage gets a real **initial AI speedup** (`-35.5 hours` saved across an 80-hour sprint), AND every stage gets hit by a **cleanup, debugging, and review rebound** (`+35.5 hours` added back) from over-engineered code, `+81%` code duplication, `1 hr 56 min` per "workslop" design doc/slide deck, noisy review bots (`<30%` signal), and `+98%` more / `+154%` larger PRs.
- **Use the Pipeline Bottleneck Rule (Theory of Constraints) and the `1,000 ms` API endpoint / microservice pipeline analogy** on Page 2.
- **Always attribute industry numbers to the published research that measured them** (GitClear, LinearB, Faros AI, Stanford/BetterUp, Microsoft Research, DORA, METR) so the reader knows these are published third-party studies.
- **Label the 80-hour sprint hours as an illustrative model, not a measured dataset.** The cover's source row says the `-35.5 h` / `+35.5 h` figures are backed by published research, and Page 3 carries the explicit footnote that the hours are one 80-hour sprint split using stage-share percentages and speed-up / rebound rates extracted from the cited studies' telemetry, not one team's measured hours. Do not drop or soften that footnote.
- **Never join sibling pipeline stages with double-headed arrows.** Flow is strictly unidirectional with a single filled arrowhead at the destination card.
- **Every hour in the 2-week sprint must sum to exactly `80.0 hours` (`10 × 8h`)** in both the Pre-AI Baseline (`80.0 h`) and the Real-World AI Sprint (`80.0 h`), and **`44.5 hours`** in the Initial AI Speedup scenario before cleanup and review.

---

## Core Narrative

> **If AI helps with coding, debugging, design, code reviews, AND meeting notes, why isn't your engineering team shipping 10× faster?**
>
> Because of the **Pipeline Bottleneck Rule** (known in operations research as the *Theory of Constraints*). When you speed up *drafting and generation* across every stage of a software pipeline, you shift the entire system’s bottleneck to **human review, debugging, and cleanup**.
>
> Every backend engineer has seen this in a producer-consumer pipeline. Imagine a backend job taking **1,000 ms**: `300 ms` in a Producer Worker preparing data, and `700 ms` in PostgreSQL acquiring locks, validating, and committing to disk. If you make the Producer Worker **10× faster** (`300 ms → 30 ms`), single-job latency only drops to **730 ms (`1.37×`)**, and pipeline throughput is still capped by the `700 ms` database step. Worse, when the faster producer submits jobs faster than the database can drain them, queues form in two places: jobs wait for a free connection in the saturated pool, and then wait on row locks inside the database. If the producer also emits larger or unvalidated batches, the backlog grows even faster, erasing the `270 ms` savings and pushing latency past **1,000 ms+**.
>
> **That is what happens inside a 2-week (`10 × 8h = 80-hour`) AI-assisted sprint.**
>
> Today’s engineers don't just use AI to autocomplete functions. They use coding agents to run `kubectl` against Kubernetes pods, port-forward services, inspect CI/CD failure logs, and run SQL queries to debug. They use AI to draft system design RFCs, generate sprint slide decks, summarize meeting minutes, and run automated PR review bots.
>
> Across an **80-hour sprint**, using AI in all six stages saves **`35.5 hours` of initial coding, troubleshooting, and drafting time** (cutting the initial work from `80.0 hours` down to `44.5 hours`, or **1.80× faster** on paper).
>
> **So where do those saved 35.5 hours go? They get eaten by the Cleanup, Debugging & Review Tax (`+35.5 hours`):**
>
> 1. **Coding (`24.0h → 5.0h initial → 8.0h net`):** AI writes initial code in `5.0h` (`-19.0h` saved), but engineers spend `+3.0h` cleaning up over-engineered abstractions, dead wrappers, and duplicated blocks ([GitClear’s 2026 study of 623M changed lines](https://www.gitclear.com/the_ai_code_quality_maintainability_gap) found refactoring fell **-70%** while code duplication jumped **+81%** and error-masking wrappers rose **+47%**).
> 2. **Debugging, K8s/DB Investigation & Testing (`12.0h → 6.5h initial → 14.5h net`):** Agents save `-5.5h` pulling pod logs, running SQL queries, and setting up unit tests. But engineers spend `+8.0h` debugging unfamiliar AI-written logic they didn't write by hand, checking confident false root-cause theories ([Microsoft Research 2026](https://arxiv.org/pdf/2604.07830)), and fixing **+54% more bugs per developer** ([Faros AI 2026](https://www.faros.ai/blog/key-takeaways-from-the-dora-report-2025)).
> 3. **System Design & RFCs (`12.0h → 8.5h initial → 14.0h net`):** Prompting generates a 10-page architecture RFC in minutes (`-3.5h` saved). But reading, fact-checking, and rewriting verbose, generic AI design docs adds `+5.5h` ([Stanford & BetterUp’s HBR study](https://hbr.org/2025/09/ai-generated-workslop-is-destroying-productivity) found **40%** of workers receive AI "workslop" costing **1 hour 56 minutes per incident** to read and redo, and [Faros AI](https://www.faros.ai/blog/key-takeaways-from-the-dora-report-2025) measured **+13.8% more task restarts** from flawed specs).
> 4. **Meetings, Slides & Sprint Planning (`12.0h → 8.5h initial → 12.0h net`):** AI writes meeting minutes, slide decks, and Jira tickets (`-3.5h` saved), but engineers spend `+3.5h` reading bloated AI summaries, cleaning up inflated tickets, and context-switching across **+67.4% more parallel PR streams** per day.
> 5. **PR Code Review (`10.0h → 8.0h initial → 18.5h net`):** AI review bots save `-2.0h` on syntax checks, yet [MSR ’26 research](https://arxiv.org/html/2604.03196) shows **12 of 13 review bots have `<60%` signal** (and [Cihan et al.](https://arxiv.org/html/2412.18531v2) found review bots increased PR closure time by **+42%**, from `5h 52m` to `8h 20m`). Meanwhile, human reviewers face **+98% more PRs** that are **+154% larger** and wait **5.3× longer** to be picked up ([LinearB 2026](https://assets.linearb.io/image/upload/v1765300694/resources/LinearB_2026_Software_Engineering_Benchmarks_Report.pdf)), adding `+10.5h` of review load.
> 6. **CI/CD & Production Ops (`10.0h → 8.0h initial → 13.0h net`):** AI saves `-2.0h` reading CI logs and writing Helm/Terraform YAML, but 2× PR volume clogs CI build queues, increases merge conflicts, and drives **+242.7% more production incidents per PR** ([Faros AI 2026](https://www.faros.ai/blog/key-takeaways-from-the-dora-report-2025)), adding `+5.0h` of operational firefighting.
>
> **The takeaway:** AI made *generating* code, docs, tests, and queries cheap. That shifted the bottleneck to **human review, understanding, and cleanup**. Until teams enforce concise specs, small batch sizes (`<150 LOC`), and strict anti-bloat guardrails, using AI everywhere turns software engineers into full-time reviewers of AI-generated noise.

---

## Brief for the Design Tool (13 Pages, 4:5 Portrait)

Design a 13-page document for a LinkedIn document post (PDF carousel). Pages are 4:5 portrait (`1080 × 1350 px`, rendered at 2× retina `2160 × 2700 px`). It is read inside the LinkedIn feed at phone width, so everything is large relative to the page: body text at least `1/36` of the page width (`60 px` on a `2160 px` canvas), captions, code, and table cells at least `1/45` of the page width (`48 px` on a `2160 px` canvas). Each page is one slide of a presentation: one idea, read in twenty to thirty seconds. Use only the text given below; do not add, reword, shorten, or invent any sentence, number, or study citation. If a page does not fit, do not shrink the type below the minimums; report which page overflowed.

### Style Rules

- **Canvas:** `#FAFAFA`. Primary text `#0F172A`, secondary text `#475569`. A thin rule in `#4F46E5` across the top of every page.
- **Three fixed elements per page:**
  1. Small-caps kicker in indigo `#4F46E5` at the top left (letter-spaced, `1/50` of page width).
  2. Bold two-line headline below it (`1/18` of page width) with one highlighted phrase in an accent colour.
  3. Page number `n/13` at the bottom right in secondary text `#475569`.
- **Typeface:** Inter (or clean geometric sans-serif) for headings and body; JetBrains Mono for time budgets, math blocks, and CLI/SQL snippets.
- **Palette (consistent across all slides and diagrams):**
  - Indigo `#4F46E5` (orchestration, primary framing, net math) with pale tint `#EEF2FF`
  - Blue `#2563EB` (hands-on coding & initial AI speedup) with pale tint `#EFF6FF`
  - Amber `#B45309` (PR review gate, workslop & review tax) with pale tint `#FFFBEB`
  - Violet `#7C3AED` (debugging, K8s/DB investigation & testing) with pale tint `#F5F3FF`
  - Teal `#0F766E` (system design, RFCs & architecture) with pale tint `#F0FDFA`
  - Slate `#334155` / `#475569` (sprint planning, meetings, CI/CD & ops) with pale tint `#F8FAFC`
  - Red `#B91C1C` (over-engineering, code duplication, bugs & prod incidents) with pale tint `#FFF1F2`
- **Diagram & Table Cards:** White or pale-tint fill, solid `3 px` outline in `#334155`, `12 px` corner radius, `6 px` coloured left accent bar. Arrows are `3 px` with a single filled triangular head at the destination only. Never use double-headed arrows.
- **Native diagrams (Pages 5, 11, and 12):** Build these in the design tool from the per-page specs below (HTML/SVG, palette colours, Inter + JetBrains Mono) rather than placing the article's Nano Banana JPEGs, whose labels fall below 12 px at slide width. The `docs/diagrams/li-0N` images remain the article's figures only.
- **Cover Illustration (Page 1 only):** One native vector diagram (HTML/SVG, palette colours) in the middle of Page 1 that carries the cover's first three points visually, so the page keeps only one text statement below it. See the Page 1 spec for the exact layout. No stock photos, robots, or brains.

---

### Page 1 · Cover

Kicker: `FULL-LIFECYCLE AI · THE REVIEW & CLEANUP BOTTLENECK`

Headline: `We use AI for coding, debugging, design, and docs. Why aren't we 10x faster?` (highlight "Why aren't we 10x faster?" in indigo `#4F46E5`)

Standfirst, one paragraph in secondary text: `To find a clear answer, I built an illustrative 2-week (80-hour) sprint model from published 2025 to 2026 research telemetry rather than one team's stopwatch. When you apply those studies' percentages across all 6 stages, AI saves 35.5 hours of initial coding, troubleshooting, and drafting time, and then adds 35.5 hours of code cleanup, debugging, and PR review work right back.`

Hero illustration band (native, about 400 px tall, full content width, between the standfirst and the closing statement). It replaces the old numbered points 1 to 3, so every number in them must appear in the band:

- **Row 1, point 1 (indigo panel `1 · AI IS USED IN ALL SIX SPRINT STAGES, NOT JUST CODING`):** six white stage cards in one row, each with a colour dot, the stage name, and what the agent does: `Coding · writes the code`, `Debugging · inspects pods & databases`, `Design · drafts design docs`, `Planning/Docs · summarizes meetings`, `PR review · comments on PRs`, `CI/CD · writes pipeline YAML`.
- **Connector:** a short indigo downward arrow with the italic caption `Apply the studies' stage percentages to one 80 h sprint`.
- **Row 2, left, point 2 (blue panel `2 · INITIAL SAVINGS ARE REAL`):** three labelled hour bars on one 80 h scale: `Before AI` solid slate `80.0 h`; `AI drafting` blue `44.5 h` plus a dashed ghost segment `-35.5 h saved`; `After cleanup, debugging & review` blue `44.5 h` + amber `+35.5 h` `= 80.0 h`. Footer: `Code, troubleshooting & docs: 80.0 h → 44.5 h, 1.80× faster on paper, before cleanup.`
- **Amber arrow `+35.5h back`** into **row 2, middle, point 3 (amber panel `3 · THE REBOUND`):** three white chips with mono numbers: `+81% · duplicated code to clean up`, `1h 56m · lost per 10-page AI design doc`, `2× PRs · twice as many, twice as large`. Footer: `Cleanup, debugging & review add +35.5 h back.`
- **Indigo arrow `net per 80h`** into the solid indigo result block `1.21× net delivery, not 10×`.

Single filled arrowheads only; flow runs top to bottom, then left to right. Every panel must fit under both Inter and the PDF fallback font with no wrapped bar labels.

One closing statement below the band, with an 8 px indigo left bar instead of a numeral (the former point 4):

**The bottleneck moved from writing to reviewing.** A team cannot ship faster than humans can understand, review, and trust what AI generated.

Published research cited row: `Illustrative 80h model built from published 2025 to 2026 research telemetry (not one team's stopwatch): GitClear · LinearB · Faros AI · Stanford / HBR · Microsoft Research · Google DORA`

Footer line in indigo italic: `The 80-hour AI sprint broken down stage by stage. Swipe →`

---

### Page 2 · The Systems Engineering Analogy

Kicker: `SYSTEMS THINKING · THE PIPELINE BOTTLENECK RULE`

Headline: `When fast producers outrun a fixed database, queues eat the speedup` (highlight "queues eat the speedup" in amber `#B45309`)

Diagram card with three stacked horizontal producer-to-database pipeline bars:

- **Bar 1 · Baseline Single Job (`1,000 ms total`):**
  - Blue `#2563EB` block (`300 ms`): `Producer Worker · 300 ms`
  - Slate `#475569` block (`700 ms`): `Database Locks, Validation & Commit · 700 ms`
- **Bar 2 · 10x Faster Producer Alone (`730 ms single job · 1.37x`):**
  - Blue `#2563EB` block (`30 ms`): `Producer · 30 ms (10x faster)`
  - Slate `#475569` block (`700 ms`): `Database Commit · 700 ms (throughput still capped at 1 job / 700 ms)`
- **Bar 3 · Fast Producer Overloading the Database (`1,000 ms+ and rising`):**
  - Blue `#2563EB` block (`30 ms`): `Producer · 30 ms`
  - Red `#B91C1C` & Amber `#B45309` block (`970 ms+`): `Connection Pool Wait + Row Lock Contention + Unbounded Queue Growth · 970 ms+`

Three bullets:

- **More jobs arrive than the bottleneck can drain.** When producers submit `2×` more jobs per minute into a database that was already the constraint, a backlog builds immediately.
- **Queues form in two places, and throughput drops.** Jobs wait for a free connection when the pool saturates, then contend for row locks inside the database. If batches are also larger or fail validation, the overload multiplies.
- **In an AI sprint, AI is the producer and humans are a shrinking database pool.** AI generates far more PRs with larger diffs, duplicated code, and noisy bot comments, while many companies use perceived AI speedups to cut engineering headcount. That is like shrinking your DB connection pool while doubling write traffic: **every claim and layoff figure is backed by published research and exact numbers in the slides ahead.**

Footnote, secondary text: `Worked systems analogy (1,000 ms -> 730 ms -> 1,000 ms+): when arrival rate exceeds service rate at the bottleneck, queue wait time erases upstream speedups and keeps growing.`

---

### Page 3 · The 3 Sprint Realities (10 × 8h = 80 Hours)

Kicker: `THE 80-HOUR SPRINT · THREE REALITIES`

Headline: `AI saves 35.5 hours of initial work, then adds 35.5 hours of cleanup and review` (highlight "saves 35.5 hours" in blue `#2563EB` and "adds 35.5 hours" in amber `#B45309`)

Six-stage hours table (white card, slate border, replacing the earlier tug-of-war diagram). Five columns: `Sprint stage` · `Pre-AI baseline` · `AI saves` (blue `#2563EB`) · `Rebound tax` (amber `#B45309`) · `Net after AI` (red `#B91C1C` where the stage ends slower than pre-AI, teal `#0F766E` where faster, slate where flat). Hours in JetBrains Mono. All four hour figures must be present for every stage:

| Sprint stage | Pre-AI baseline | AI saves | Rebound tax | Net after AI |
|---|---|---|---|---|
| 1 · Hands-on coding | `24.0 h` | `-19.0 h` | `+3.0 h` | `8.0 h` |
| 2 · Debugging, K8s/DB & testing | `12.0 h` | `-5.5 h` | `+8.0 h` | `14.5 h` |
| 3 · System design & RFCs | `12.0 h` | `-3.5 h` | `+5.5 h` | `14.0 h` |
| 4 · Meetings, slides & planning | `12.0 h` | `-3.5 h` | `+3.5 h` | `12.0 h` |
| 5 · PR code review & bots | `10.0 h` | `-2.0 h` | `+10.5 h` | `18.5 h` |
| 6 · CI/CD & prod ops | `10.0 h` | `-2.0 h` | `+5.0 h` | `13.0 h` |
| **Full 10-day sprint** (dark `#1E293B` row) | **`80.0 h`** | **`-35.5 h`** | **`+35.5 h`** | **`80.0 h`** |

Two concise takeaway lines below the table:

- **Pre-AI studies (Sonar 2019, Stripe) measured `~30%` coding (`24h`); 2025 to 2026 studies (Atlassian, Microsoft) show coding shrank to `~10 to 16%` (`8h`):** AI genuinely cut coding time by two-thirds, yet the 80-hour sprint stayed completely full.
- **Where the saved `35.5 hours` went:** Into code cleanup (`+3h`), debugging unfamiliar AI bugs (`+8h`), rewriting bloated docs (`+9h`), and 2× PR review queues (`+10.5h`, or rubber-stamping PRs that then break in production).

Footnote, secondary text: `Net result: +21% to +34% more tasks completed (1.21x to 1.34x), while PR review + debugging jumps from 22.0h (27.5%) to 33.0h (41.3%).`

Second footnote, secondary italic text (required, never drop it): `Illustrative model: one 80-hour (10 × 8 h) sprint split built by applying the published stage-share percentages and AI speedup/rebound rates from the cited studies, not one team's stopwatch log.`

---

### Page 4 · Stage 1: Hands-On Coding & Over-Engineering

Kicker: `STAGE 1 · HANDS-ON CODING (24.0h → 8.0h)`

Headline: `Coding is 3x faster once you strip out the duplicated, over-engineered bloat` (highlight "over-engineered bloat" in red `#B91C1C`)

Math & Breakdown Strip inside a dark `#1E293B` card:

```text
Pre-AI Coding:            24.0 h (30% of sprint)
Initial AI Generation:     5.0 h (-19.0 h saved writing boilerplate & endpoints)
Cleanup & Refactor Tax:   +3.0 h (deleting wrappers, dead abstractions & clones)
Net AI Coding Time:        8.0 h (-16.0 h net saved · 3.0x faster, not 10x)
```

Four findings from **GitClear's 2026 study (which analyzed 623M changed lines of code from 2023 to 2026)** and **LinearB's 2026 report (8.1M PRs)**:

- **Refactoring fell `-70%`:** Moved/consolidated lines dropped from `21%` (pre-AI) to `3.8%` in 2026 as AI defaults to adding new code rather than refactoring existing modules.
- **Code duplication jumped `+81%`:** Repeated 5+ line blocks hit an all-time high (`+41%` within-commit copy/paste), creating multi-file maintenance work.
- **Error-masking wrappers rose `+47%`:** AI frequently wraps failing logic in defensive `try/catch`, null-guards, and fallback mocks that hide root causes.
- **Legacy code maintenance dropped `-74%`:** LinearB's 2026 report confirms human PRs do **1.5× to 2.2× more refactoring** than AI PRs (`0.37` vs `0.17` refactor rate).

Footnote, secondary text: `Published sources: GitClear Maintainability Gap Report (2026); LinearB Software Engineering Benchmarks Report (2026).`

---

### Page 5 · Stage 2: Debugging, K8s/DB Investigation & Testing

Kicker: `STAGE 2 · DEBUGGING, K8S/DB INVESTIGATION & TESTING (12.0h → 14.5h)`

Headline: `Agents gather pod logs and SQL fast, but AI code creates 54% more bugs` (highlight "54% more bugs" in red `#B91C1C`)

Native diagram (built in the design tool, full content width, replaces the earlier `li-02` image whose labels were unreadable at slide size):

- **Upstream cause band** (red `#B91C1C` border, `#FFF1F2` fill), title `UPSTREAM CAUSE · STAGE 1 WRITE-ONLY AI CODE BLOAT`, three stat chips: `+81%` duplicated code blocks · `−70%` refactoring & moved code · `+47%` error-masking guards; small source line `Source: GitClear & LinearB repository telemetry`.
- **Single downward arrow** from the band into the chart, labelled `Unfamiliar, error-masked code reaches staging & production`.
- **Two-sided bar chart** (white card, slate `#334155` border) with a central axis and `1 h` gridlines at 100 px per hour. Header: `AGENT SPEEDUPS −5.5 h` (blue `#2563EB`, left) and `+8.0 h DEBUGGING REBOUND` (amber `#B45309`, right). Three rows, blue bars growing left and amber bars growing right:
  1. `K8s & pod agent` (kubectl logs, exec & port-forward) `−2.5 h` ↔ `Missing-mental-map penalty` (reverse-engineering unfamiliar AI code live) `+3.5 h`
  2. `Postgres SQL agent` (diagnostic SQL & CI log checks) `−1.5 h` ↔ `Confident false theories` (plausible but wrong root-cause stories) `+2.5 h`
  3. `AI test generator` (generates unit test files) `−1.5 h` ↔ `Flawed AI tests` (tests pass on buggy code, `+54%` bugs) `+2.0 h`

Bottom summary bar: `12.0 h baseline - 5.5 h agent troubleshooting & diagnostics + 8.0 h debugging unfamiliar AI bugs = 14.5 h net (+2.5 h increase).`

Footnote, secondary text: `Published sources: Microsoft Research & OSU "To Copilot and Beyond" (2026); Faros AI Report (2026); Google Cloud DORA (2025).`

---

### Page 6 · Stage 3: System Design & Architecture RFCs

Kicker: `STAGE 3 · SYSTEM DESIGN & ARCHITECTURE (12.0h → 14.0h)`

Headline: `A 10-page AI design doc takes 5 minutes to prompt and 2 hours to fact-check` (highlight "2 hours to fact-check" in amber `#B45309`)

Three stacked evidence cards:

- **Card 1 · Initial Drafting Speedup (`-3.5 h` saved, teal `#0F766E` bar):** Feeding business requirements into an LLM produces a formatted RFC, schema draft, and trade-off table in minutes (`12.0 h → 8.5 h`).
- **Card 2 · The "Workslop" Tax (`+5.5 h` added, amber `#B45309` bar):** A 2025 study by Stanford University and BetterUp in *Harvard Business Review* (`n=1,150`) found **40% of workers** receive AI "workslop": polished, lengthy documents that lack real project context. Recipients spend an average of **1 hour 56 minutes per incident** reading, fact-checking, and rewriting it.
- **Card 3 · Spec Drift & Task Restarts (`+13.8%` restarts, red `#B91C1C` bar):** Microsoft Research (2026) found one-shot AI designs default to generic textbook patterns and silently invent requirements. Faros AI (2026) found a **`+13.8%` increase in task restarts** (work moving backward to in-progress) when teams build on unverified specs.

Bottom summary bar: `12.0 h baseline - 3.5 h drafting + 5.5 h rewriting specs & restarts = 14.0 h net (+2.0 h increase).`

Footnote, secondary text: `Published sources: Harvard Business Review / Stanford / BetterUp (2025); Microsoft Research (2026); Faros AI (2026).`

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
  - **Document & ticket inflation:** When a 5-bullet update becomes a 3-page AI summary or 15 verbose Jira tickets, teammates spend the saved time reading and trimming filler (`45.9%` of Microsoft devs surveyed cited doc drift/slop as a major issue).
  - **`+67.4%` more daily PR contexts:** Faros AI's 2026 study found engineers running multiple AI tasks juggle **67.4% more PR contexts** and **17.7% more task contexts** every day.
  - **`+26%` more stalled tasks:** Tasks sitting `7+ days` with no progress rose `26%`, requiring extra standup, blocker triage, and re-planning time.

Footnote, secondary text: `Net planning & coordination time stays flat at 12.0 hours: faster note-taking is canceled out by managing more parallel work-in-progress.`

---

### Page 8 · Stage 5: PR Code Review & AI Review Bots

Kicker: `STAGE 5 · CODE REVIEW & AI REVIEW BOTS (10.0h → 18.5h)`

Headline: `Why don't AI code review agents solve the PR review bottleneck?` (highlight "solve the PR review bottleneck?" in amber `#B45309`)

Four stat tiles in a 2 × 2 grid from published 2025 and 2026 PR review studies:

- Tile 1 (amber `#B45309` accent): **`12 of 13` Bots `<60%` Signal** (MSR ’26 study of 3,109 PRs found 60.2% of closed bot-reviewed PRs had `<30%` actionable comments; noise drove higher PR abandonment).
- Tile 2 (red `#B91C1C` accent): **`+42%` Longer PR Closure** (Bilkent University & Beko study of 4,335 PRs found adding an LLM review bot raised average PR closure time from `5h 52m` to `8h 20m` due to resolving noisy bot comments).
- Tile 3 (amber `#B45309` accent, person-and-check mark): **`5.3x` Longer Pickup Wait** (LinearB's 2026 report found Agentic AI PRs wait `17.6 hours` at P75 for a human to open them vs `3.3 hours` for manual PRs, and `<60%` get accepted).
- Tile 4 (red `#B91C1C` accent): **`+91% to +441%` Review Time** (Faros AI found high-AI teams open `+98%` more PRs that are `+154%` larger, doubling review time in 2025 at `+91%` and jumping `+441%` in 2026).

Two bullets:

- **AI review bots catch syntax (`-2.0 h`), not architectural intent.** A bot can flag a missing null check, but it cannot tell whether a 400-line diff belongs in the service at all.
- **Smaller teams + 2× PR queues = 31% more unreviewed merges.** While AI doubles PR volume, `26%` of surveyed companies have already reduced or combined their engineering teams (LeadDev 2025), and U.S. employers cited AI in `54,836` job cuts in 2025 and over `120,000` job cuts in 2026 (Challenger). Overwhelmed survivors rubber-stamp PRs, pushing bugs straight to production.

Footnote, secondary text: `Published sources: Chowdhury et al. (MSR '26); Cihan et al. (2025); LinearB (2026); Faros AI (2026); LeadDev (2025); Challenger (2026).`

---

### Page 9 · Stage 6: CI/CD Pipelines, Deployments & Production Ops

Kicker: `STAGE 6 · CI/CD, DEPLOY & PROD OPS (10.0h → 13.0h)`

Headline: `AI writes the Helm chart, and 2x PR volume triples production incident risk` (highlight "triples production incident risk" in red `#B91C1C`)

Three stacked cards:

- **Card 1 · Initial AI Ops Speedup (`-2.0 h` saved, blue `#2563EB` bar):** AI assistants draft GitHub Actions, Dockerfile, Terraform, and Kubernetes manifests, and summarize long CI build failure logs (`10.0 h → 8.0 h`).
- **Card 2 · CI Queue & Merge Conflict Contention (`+2.0 h` added, amber `#B45309` bar):** Pushing `+98%` more PRs with `+154%` larger diffs into the same CI/CD pipeline causes build queues, integration test retries, and rebase conflicts.
- **Card 3 · The Production Incident Whiplash (`+3.0 h` added, red `#B91C1C` bar):** Faros AI's 2026 study found **incidents per PR jumped `+242.7%`** (more than 3.4× higher chance of a production incident per merged change) as larger, lightly reviewed PRs reach production.

Bottom summary bar: `10.0 h baseline - 2.0 h YAML/log help + 5.0 h CI contention & incident fixes = 13.0 h net (+3.0 h increase).`

Footnote, secondary text: `Published sources: Faros AI "The Acceleration Whiplash" (2026); Google Cloud DORA Report (2025).`

---

### Page 10 · Why It Still Feels 10x Faster (The Perception Gap)

Kicker: `PERCEPTION VS. STOPWATCH · WHY 1.2x FEELS LIKE 10x`

Headline: `Generating 500 lines in 10 seconds feels like 10x; fixing it for 2 hours feels invisible` (highlight "feels invisible" in indigo `#4F46E5`)

Comparison block from the **METR Randomized Controlled Trial** (16 experienced maintainers on large open-source repos averaging `1M+ LOC` and `22k+ stars`, screen-recorded across 246 real issues):

- **Before starting:** Developers predicted AI would make them **`24% faster`**.
- **After finishing:** Developers believed AI had made them **`20% faster`**.
- **Actual stopwatch time:** Tasks took **`19% longer`** in the 2025 trial (and `4% to 18% faster` in the Feb 2026 follow-up).

Three bullets:

- **Generating feels fast; reviewing and fixing feels invisible.** Watching an agent produce a feature, a design doc, or a SQL query in seconds feels effortless, so our brains remember the 5-minute prompt rather than the 90 minutes spent fixing subtle bugs later.
- **UC Berkeley eye-tracking study (DORA 2025):** Developers used AI heavily on mechanical boilerplate (`19%` visual attention) but ignored it when understanding complex code (`<1%` attention) to stay in control.
- **Bounded Delegation (Microsoft Research 2026):** Across 860 developers surveyed, engineers wanted AI to automate *incident diagnostics and setup work*, never final architectural decisions or production sign-off.

Footnote, secondary text: `Published sources: METR RCT (July 2025 & Feb 2026 update); DORA / UC Berkeley Study (2025); Microsoft Research (2026).`

---

### Page 11 · The Playbook: How to Actually Speed Up the Sprint

Kicker: `THE ENGINEERING PLAYBOOK · KEEPING THE SAVED HOURS`

Headline: `To keep the 35.5 hours AI saves, put strict guardrails on chat, code, and PRs` (highlight "strict guardrails" in indigo `#4F46E5`)

Native funnel diagram (full content width, replaces the earlier `li-03` image):

- **Band 1** (indigo `#4F46E5` border, `#EEF2FF` fill), title `1 · FULL-LIFECYCLE AI GENERATION · −35.5 h INITIALLY SAVED`, four chips with coloured top bars: `AI coding agents −19.0 h` (blue; 2× PRs · +154% diffs · +81% clones), `K8s & SQL checks −5.5 h` (violet; fast logs · confident false leads), `AI RFC & specs −3.5 h` (teal; 10-page docs · generic patterns), `Notes & PR bots −7.5 h` (slate; auto-tickets · <30% bot signal).
- **Funnel** (light indigo trapezoid labelled `High-volume AI output`) narrowing into **Gate 2** (amber `#B45309` border, `#FFFBEB` fill): `2 · Human review & verification gate`, subtitle `The sprint bottleneck: every line still needs human accountability`.
- **Split** into two single-arrowhead branches: red `No guardrails` → **Path A · Undisciplined slop** (red card): `+91% to +441%` PR review wait · `1 h 56 m` lost per workslop doc · `+242.7%` prod incidents per PR · `31%` of PRs merge with no human review; red pill `All 35.5 h lost · DORA: flat`. Teal `Bounded delegation` → **Path B · Five guardrails** (teal `#0F766E` card), numbered: 1-page human specs (zero raw workslop); hard PR cap `<150 LOC` + code-reuse rules; shift AI review left to the IDE (pre-push); read-only K8s/SQL summaries + human fix; track review wait, churn & incidents per PR; teal pill `35.5 h kept · 1.80× stays real`.

Two takeaway bullets below the diagram:

- **Stop in-chat walls of text first:** Use `CLAUDE.md` / `AGENTS.md` BLUF rules, **Progressive Zoom** skills (30-sec map before details), and isolated **Subagents** so 5-paragraph dumps never bury the big picture.
- **Enforce stage gates:** `jscpd --fail-on-new-clones` in CI (Stage 1), mutation testing (`Stryker` / `TestSuiteBench`, Stage 2), 1-page RFCs + `WIP=1` (Stages 3 to 4), Stacked PRs `<150 LOC` + IDE pre-push review (Stage 5), and batched merge queues + canary flags (Stage 6).

Footnote, secondary text: `Drop-in CLAUDE.md, AGENTS.md, GEMINI.md, Cursor rules, skills & subagents included in the companion repository.`

---

### Page 12 · The Anti-Slop Toolkit: In-Chat Zoom & 6 Stage Gates

Kicker: `OPEN-SOURCE TOOLKIT · CLAUDE.MD · AGENTS.MD · SKILLS`

Headline: `Stop 5-paragraph chat dumps first, then gate every stage of the sprint` (highlight "Stop 5-paragraph chat dumps" in indigo `#4F46E5`)

Native two-part diagram (full content width, replaces the earlier `li-04` image):

- **Part 1 · Stop in-chat workslop (rule files + skills)** (indigo band): three cards joined by single-arrowhead arrows: `1 · Isolated explorer subagent` (searches 15+ files & logs in its own context, returns a 15-line brief) → `2 · Zoom level 1: 30-second mental map` (1-sentence BLUF + 5-node flow + top 3 file:line refs, then stops) → `3 · Zoom levels 2 & 3, on request only` (state transitions, edge cases & code only when the developer asks).
- **Connector**: teal down arrow labelled `Clean mental map feeds disciplined stage gates`.
- **Part 2 · Stage-by-stage sprint gates · keeps the 35.5 h saved** (teal band): 3 × 2 grid of stage cards with coloured left bars: `1 · Coding` (`jscpd` + de-bloat audit: block new clones & silent catch), `2 · Debug / Test` (`Stryker` mutants: read-only logs + kill self-passing tests), `3 · Design` (1-page RFC skill: ≤350 words + `<details>` appendix), `4 · Planning` (`WIP = 1` rule: 1 active task + completion command), `5 · Review` (Stacked PRs `<150 LOC`: gh stack / Graphite + IDE pre-push check), `6 · CI / Ops` (scoped merge queue: batched CI + canary auto-rollback).

Two concise takeaway lines below the diagram:

- **Fix your IDE chat UI (`CLAUDE.md` / `AGENTS.md` / `GEMINI.md` / `.cursor/rules`):** Delegate file searches to isolated subagents (`mental-map-explorer.md`) and enforce 3-level **Progressive Zoom** (`30-sec map -> state flow -> code on demand`).
- **Gate the 6 stages:** `jscpd --fail-on-new-clones` (Stage 1), `Stryker` mutation checks (Stage 2), 1-page RFC skill (Stage 3), `WIP=1` (Stage 4), Stacked PRs `<150 LOC` + IDE pre-push review (Stage 5), and scoped merge queues + canaries (Stage 6).

Footnote, secondary text: `All ready-to-copy rule files, skills, subagents, and stage prompts are in the repository's toolkit/ folder.`

---

### Page 13 · Final Summary & Sources

Kicker: `THE TAKEAWAY · FULL-SPRINT REALITY CHECK`

Headline: `AI made writing cheap. Reviewing and verifying is now the bottleneck.` (highlight "Reviewing and verifying is now the bottleneck." in indigo `#4F46E5`)

Three summary cards stacked:

- Badge `-35.5 h` (blue `#2563EB` bar): **Initial AI time savings are real across all 6 stages.** Coding (`-19h`), K8s/DB troubleshooting (`-5.5h`), RFC drafting (`-3.5h`), meetings/slides (`-3.5h`), review bots (`-2h`), and CI/CD (`-2h`) cut initial work from `80h` to `44.5h`.
- Badge `+35.5 h` (amber `#B45309` bar): **Without guardrails, cleanup and review eat every saved hour.** Cleaning up duplicated code (`+3h`), debugging AI bugs (`+8h`), rewriting bloated design docs (`+5.5h`), parallel WIP (`+3.5h`), 2× PR review queues (`+10.5h`), and prod incidents (`+5h`) refill the `80h` sprint.
- Badge `The Fix` (indigo `#4F46E5` bar): **Don't ask "How fast can AI write this?"** Ask: **"How fast can another engineer review, verify, and debug what AI just produced?"**

Published Research Citations (listed cleanly at bottom):
- `Faros AI (2025 & 2026) · AI Productivity Paradox & Acceleration Whiplash Reports`
- `LinearB (2026) · Software Engineering Benchmarks Report: AI Productivity Edition`
- `GitClear (2025 & 2026) · The Maintainability Gap: AI Code Quality Research`
- `Harvard Business Review / Stanford / BetterUp (2025) · AI-Generated "Workslop" Study`
- `Microsoft Research & OSU (2026) · To Copilot and Beyond · MSR '26 Code Review Agent Study`
- `Google Cloud DORA (2025) · ETH Zurich TestSuiteBench (2026) · LeadDev (2025) · Challenger (2026)`

---

## Companion LinkedIn Post Text (Ready to Copy & Paste)

```text
We use AI for coding, debugging, design, and docs. Why aren't we 10× faster?

To understand why and find a real answer, I built an illustrative 80-hour sprint model (10 days × 8 hours) from published 2025 and 2026 research telemetry (GitClear, LinearB, Faros AI, Stanford, Microsoft Research, and Google DORA)—rather than relying on a single team's stopwatch log—by extracting the stage shares and percentage changes measured across those studies.

Here is what happens when you map those research percentages onto one 80-hour sprint:

When you use AI across every stage of an 80-hour sprint, it genuinely saves ~35.5 hours of initial coding, troubleshooting, and drafting time (80h → 44.5h).

Then, cleaning up, debugging, and reviewing that AI output adds +35.5 hours right back:

1. Hands-on Coding (24h → 5h initial → 8h net):
AI generates endpoints and boilerplate in 5h (-19h saved). But GitClear's 2026 study found refactoring fell -70%, code duplication jumped +81%, and error-masking wrappers rose +47%. Engineers spend +3h stripping out over-engineered wrappers and duplicate blocks.

2. Debugging, K8s/DB Investigation & Testing (12h → 6.5h initial → 14.5h net):
Coding agents save -5.5h running kubectl exec, reading pod/CI logs, port-forwarding, and running SQL queries. However, debugging unfamiliar AI code nobody on the team wrote by hand, checking confident false root-cause theories (Microsoft Research, 2026), and fixing +54% more bugs per developer (Faros AI, 2026) adds +8h back.

3. System Design & RFCs (12h → 8.5h initial → 14h net):
Prompting drafts a 10-page RFC in minutes (-3.5h saved). Yet a Stanford & BetterUp study in HBR found 40% of workers are getting hit with AI "workslop": polished, verbose docs missing real system context that cost teammates 1 hr 56 min per doc to fact-check and rewrite (+5.5h added, plus +13.8% task restarts).

4. Meetings, Slides & Sprint Planning (12h → 8.5h initial → 12h net):
AI writes the meeting minutes, slide decks, and Jira subtasks (-3.5h saved). Then engineers spend +3.5h trimming bloated auto-generated tickets and context-switching across +67.4% more parallel PR streams per day.

5. PR Code Review & AI Review Bots (10h → 8h initial → 18.5h net):
What about AI code review bots? An MSR '26 study of 3,109 PRs found 12 of 13 review bots have <60% signal (mostly noisy comments), and an industrial study by Bilkent University & Beko found PR closure time rose +42% (5h52m → 8h20m) after bot adoption. Meanwhile, human reviewers (often on smaller teams after AI-justified layoffs) face +98% more PRs that are +154% larger and wait 5.3× longer for pickup (LinearB, 2026). Net review load jumps +8.5h.

6. CI/CD & Production Ops (10h → 8h initial → 13h net):
AI saves -2h writing Helm/Terraform YAML and reading CI errors, but 2× PR volume clogs CI queues and drives +242.7% more production incidents per PR (Faros AI, 2026), adding +5h of ops firefighting.

In systems engineering, this is the Pipeline Bottleneck Rule: when generating code and docs becomes nearly free, human review and understanding becomes the bottleneck for the entire system.

Swipe through the 13-page breakdown below for the stage-by-stage 80-hour sprint math, the research citations, and the open-source toolkit (CLAUDE.md, AGENTS.md, GEMINI.md, Cursor rules, Progressive Zoom skill, and stage gates) to keep the 35.5 hours AI saves.
```

---

## Closing Checklist for the Design Tool

- [ ] **13 pages total**, 4:5 portrait (`1080 × 1350 px` or `2160 × 2700 px`), with no page counters (the pages are exported as standalone images).
- [ ] **Page 1** includes the native hero illustration band (six stage cards, 80 h bars, rebound chips, `1.21×` block), the single closing statement, and the source row stating the `-35.5 h` / `+35.5 h` figures are backed by published research.
- [ ] **Page 2** uses the `1,000 ms` producer-to-database pipeline analogy.
- [ ] **Page 3** shows the six-stage hours table with all four figures per stage (pre-AI, AI saves, rebound, net after AI), the `80.0 h` totals row, and the italic "Illustrative only" footnote explaining the hours are derived from the cited studies' percentages, not one team's measurements.
- [ ] **Page 5** shows the native upstream-cause band and two-sided bar chart (three agent speedups summing to `−5.5 h` against three rebounds summing to `+8.0 h`) above the dark net-balance summary bar.
- [ ] **Page 11** shows the native funnel: four AI generators (summing to `−35.5 h`) → human review gate → Path A slop stats vs Path B five guardrails.
- [ ] **Page 12** shows the native two-part diagram: three-step in-chat zoom flow feeding the 3 × 2 grid of six stage gates.
- [ ] **Pages 4 to 9** cover each of the 6 sprint stages in order with exact initial savings, rebound hours, and study citations.
- [ ] **No text overflows any card**, and body text is at least `1/36` of page width (`captions/tables >= 1/45`).
