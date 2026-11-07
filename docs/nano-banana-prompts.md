# Nano Banana Pro Image Generation Prompts: Full-Lifecycle AI Sprint Analysis (Complete 9-Diagram Set for Medium & 4 Portrait Diagrams for LinkedIn)

These prompts are written for **Google Nano Banana Pro** (diffusion-based text-to-image model) following the strict 7-section `diagram` specification. Every prompt uses one unified colour palette and exact numbers from the **illustrative 80-hour (`10 × 8h`) two-week sprint model** (constructed by applying the stage shares and percentage changes from published 2025 to 2026 industry studies: **Faros AI**, **LinearB**, **GitClear**, **Stanford/HBR**, **MSR '26**, **Microsoft Research**, **METR**, **Atlassian**, and **DORA**).

---

## Shared Palette Across All Diagrams

| Role / Sprint Stage | Accent Hex | Card Fill Hex | Meaning |
|---|---|---|---|
| **Orchestration / Net Math / Primary Frame** | Indigo `#4F46E5` | `#EEF2FF` | Sprint totals, net velocity, primary flow |
| **Stage 1: Hands-on Coding & Initial Speedup** | Blue `#2563EB` | `#EFF6FF` | Code generation, initial hours saved by AI |
| **Stage 2: Debugging, K8s/DB Investigation & Tests** | Violet `#7C3AED` | `#F5F3FF` | `kubectl`, pod logs, SQL queries, test suites |
| **Stage 3: System Design & Architecture RFCs** | Teal `#0F766E` | `#F0FDFA` | Architecture design docs, schemas, specs |
| **Stage 4 & 6: Planning, Meetings, CI/CD & Ops** | Slate `#475569` | `#F8FAFC` | Ceremonies, slide decks, CI pipelines, deploys |
| **Stage 5: PR Review Gate & Workslop Tax** | Amber `#B45309` | `#FFFBEB` | Human review bottleneck, doc/bot workslop |
| **Over-Engineering, Bugs & Prod Incidents** | Red `#B91C1C` | `#FFF1F2` | Duplicate code (`+81%`), bugs (`+54%`), incidents (`+242.7%`) |

---

## Diagram Index (Mapped to Medium Article & LinkedIn Carousel)

### Part A: Medium Article Diagrams (`16:9` Landscape, `2752 × 1536`)

| File Name | Diagram Title | Medium Article Section | Published Research Sources |
|---|---|---|---|
| `01-three-sprint-realities.jpg` | The Three Realities of an 80-Hour Full-Stack AI Sprint | Opening & Section 3 (The 80-Hour Model) | Faros AI (2025/2026), Atlassian (2025), Microsoft Research (2024/2026) |
| `02-pipeline-bottleneck-analogy.jpg` | Distributed Microservice Pipeline vs. AI Sprint Bottleneck | Section 1 (The Pipeline Bottleneck Rule) | Goldratt Theory of Constraints, Faros AI (`+98%` PRs, `+154%` size) |
| `03-stage-by-stage-tug-of-war.jpg` | Stage-by-Stage Tug-of-War (`-35.5 h` Saved vs. `+35.5 h` Rebound) | Section 3 (Initial Speedup vs. Cleanup & Review Tax) | All 6 Sprint Stages Combined |
| `04-write-only-code-bloat.jpg` | Human Refactoring vs. AI "Write-Only" Code Bloat | Section 4.1 (Stage 1: Hands-On Coding) | GitClear (2026), LinearB (2026) |
| `05-debugging-mental-map-gap.jpg` | K8s/SQL Agent Investigation vs. The Mental Map & Bug Rebound | Section 4.2 (Stage 2: Debugging & Testing) | Microsoft Research & OSU (2026), Faros AI (`+54%` bugs/dev) |
| `06-workslop-and-review-bot-noise.jpg` | The "Workslop" Transfer Tax & Code Review Bot Noise | Sections 4.3 to 4.5 (Design, Docs & PR Review) | Stanford/BetterUp HBR (2025), MSR '26 (`3,109` PRs), Cihan et al. (`4,335` PRs), LinearB |
| `07-verification-funnel-guardrails.jpg` | The Full-Stack AI Review Funnel & Engineering Playbook | Section 6 (Bounded Delegation Playbook) | DORA (2025), Microsoft Research (2026), GitClear (2026) |
| `08-in-chat-progressive-zoom.jpg` | Stopping In-Chat Workslop: 5-Paragraph Dump vs. Progressive Zoom & Subagents | Section 6.1 (Stopping In-Chat Workslop) | Anthropic Steering Claude Code (2026), BLUF / Progressive Disclosure |
| `09-stage-by-stage-mitigation-architecture.jpg` | Stage-by-Stage Engineering Mitigations Across the 6 Sprint Stages | Section 6.2 & 6.3 (Stage-by-Stage Mitigations & Toolkit) | `jscpd`, *TestSuiteBench* / `Stryker`, Stacked PRs (`gh stack`), Merge Queues |

### Part B: LinkedIn PDF Carousel Diagrams (`3:4` / `4:5` Portrait, `1792 × 2400`)

| File Name | Diagram Title | Claude Design Carousel Slide | Why Portrait (`3:4` / `4:5`) |
|---|---|---|---|
| `li-01-sprint-tug-of-war.jpg` | The 80-Hour Sprint Tug-of-War (3 Bars + 6 Stages) | **Page 3** (Replaces the dense 35-cell spreadsheet table) | Fills the vertical slide area between headline and footer with large 48 px phone-readable labels |
| `li-02-bloat-and-mental-map.jpg` | From Write-Only Code Bloat to the Debugging Mental-Map Penalty | **Page 5** (Visualizes Stage 1 & Stage 2 rebound mechanics) | Breaks up the 5-page text-card run with a top-to-bottom causal diagram |
| `li-03-verification-funnel.jpg` | The Review Funnel: Slop Flood vs. The 5 Guardrails | **Page 11** (Visualizes the Verification Funnel & Playbook) | Shows visually where the engineering guardrails sit in the delivery pipeline |
| `li-04-chat-zoom-and-stage-gates.jpg` | Progressive Zoom + 6 Stage Gates Toolkit | **Page 12** (Visualizes the In-Chat Zoom & 6-Stage Mitigation Toolkit) | Gives readers a visual architecture map of the `CLAUDE.md` / `AGENTS.md` toolkit |

---

## Diagram 1 (`01-three-sprint-realities.jpg`): The Three Realities of an 80-Hour Full-Stack AI Sprint

**What it shows:** A three-swimlane horizontal comparison of a 2-week sprint (`10 days × 8 hours = 80.0 hours`): (1) Pre-AI Baseline (`80.0 h`), (2) Initial AI Speedup when AI is used across all 6 stages (`44.5 h`, saving `35.5 h`), and (3) Real-World AI Sprint after the Cleanup, Debugging, and Review Rebound refills the sprint (`80.0 h`, `~1.21x` net task output).

### Prompt to Paste into Nano Banana Pro

```text
Create a comparison diagram of a two-week software engineering sprint (10 days x 8 hours = 80.0 hours) across three horizontal swimlanes: Pre-AI Baseline, Initial AI Speedup Across All 6 Stages, and Real-World AI Sprint After Cleanup and Review. Output a high-resolution 16:9 landscape raster image. All directions below are private; print only the quoted labels and captions. No extra title, layout terminology or invented text.

VISUAL STYLE (PRIVATE):
White canvas, near-white group panels, crisp sans-serif such as Inter, dark slate text #0F172A with secondary #475569, fine 3px borders, consistent rounded corners, generous whitespace. Very pale tinted fills on cards and proportional horizontal timeline segments with saturated colour only on small icons, left accent bars and outlines; never a whole layer in saturated colour. The focal point is Swimlane 3 ("3. Real-World AI Sprint (After Cleanup & Review)") and its expanded amber PR Review block ("PR Review · 18.5 h (+85%)"), which has the strongest border and largest name; everything else is quieter. Avoid condensed type, tiny captions, broad grey backgrounds, heavy outlines, gradients, 3D, glows, textures, mascots, robots, or brains.

ICONS (PRIVATE):
One small simple line icon beside each stage name, same size and stroke throughout: code brackets on Coding, a terminal-and-database icon on Debugging K8s/DB & Tests, a blueprint compass on System Design & RFCs, a calendar-slide icon on Planning & Meetings, a person-and-check badge on PR Review, and a pipeline-rocket icon on CI/CD & Prod Ops. No invented brand logos.

SPATIAL LAYOUT AND EXACT LABELS (PRIVATE):
Arrange the canvas into three well-spaced horizontal swimlanes stacked top to bottom across most of the canvas, with a summary card column on the right and a compact legend strip at the bottom outside the main boundary.

Swimlane 1 (top): Left header card "1. Pre-AI Baseline Sprint" with caption "10 x 8h Days = 80.0 Hours". To its right, a full-width horizontal stacked bar divided into six proportional cards in reading order:
- Blue #2563EB accent (#EFF6FF fill): "Coding · 24.0 h" with caption "30% of sprint"
- Violet #7C3AED accent (#F5F3FF fill): "Debug & Tests · 12.0 h" with caption "Manual logs & SQL"
- Teal #0F766E accent (#F0FDFA fill): "Design & RFCs · 12.0 h" with caption "Architecture specs"
- Slate #475569 accent (#F8FAFC fill): "Planning & Docs · 12.0 h" with caption "Meetings & tickets"
- Amber #B45309 accent (#FFFBEB fill, person-and-check mark): "PR Review · 10.0 h" with caption "Manual review"
- Slate #475569 accent (#F8FAFC fill): "CI/CD & Ops · 10.0 h" with caption "Builds & deploys"
Right summary card for Swimlane 1 (slate outline): "80.0 Hours · 1.0x Baseline".

Swimlane 2 (middle): Left header card "2. Initial AI Speedup (All 6 Stages)" with caption "Before cleanup & review tax". To its right, a horizontal stacked bar spanning 44.5 of 80 hours, followed by a dashed pale-blue empty slot on the right labelled "35.5 Hours Initially Saved by AI (-44%)":
- Blue #2563EB accent (#EFF6FF fill): "Coding · 5.0 h" with caption "-19.0 h saved"
- Violet #7C3AED accent (#F5F3FF fill): "K8s/SQL Agent Debug · 6.5 h" with caption "-5.5 h saved"
- Teal #0F766E accent (#F0FDFA fill): "AI Draft RFCs · 8.5 h" with caption "-3.5 h saved"
- Slate #475569 accent (#F8FAFC fill): "AI Notes & Slides · 8.5 h" with caption "-3.5 h saved"
- Amber #B45309 accent (#FFFBEB fill): "AI Review Bots · 8.0 h" with caption "-2.0 h saved"
- Slate #475569 accent (#F8FAFC fill): "AI CI/YAML · 8.0 h" with caption "-2.0 h saved"
Right summary card for Swimlane 2 (indigo #4F46E5 accent): "44.5 Hours · 1.80x Paper Speedup".

Swimlane 3 (bottom, focal point): Left header card "3. Real-World AI Sprint (After Cleanup & Review)" with caption "+35.5 h Cleanup, Debugging & Review Rebound". To its right, a full-width horizontal stacked bar spanning all 80.0 hours:
- Blue #2563EB accent (#EFF6FF fill): "Coding + Cleanup · 8.0 h" with caption "+3.0 h fixing +81% clones"
- Red #B91C1C accent (#FFF1F2 fill): "Debug AI Bugs · 14.5 h" with caption "+8.0 h (+54% bugs/dev)"
- Teal #0F766E accent (#F0FDFA fill): "Rewrite RFC Slop · 14.0 h" with caption "+5.5 h (1h56m/doc tax)"
- Slate #475569 accent (#F8FAFC fill): "Planning & WIP · 12.0 h" with caption "+3.5 h (+67% PR contexts)"
- Focal Amber #B45309 accent (#FFFBEB fill, bold border, person-and-check mark): "PR Review · 18.5 h (+85%)" with caption "+10.5 h (2x PRs, 5.3x wait)"
- Red #B91C1C accent (#FFF1F2 fill): "CI & Prod Incidents · 13.0 h" with caption "+5.0 h (+242% incidents/PR)"
Right summary card for Swimlane 3 (amber #B45309 accent): "80.0 Hours · ~1.21x Net Tasks".

VISUAL CONNECTIONS (PRIVATE):
Use medium solid indigo #4F46E5 arrows and solid amber #B45309 arrows. Draw exactly two vertical arrows between Swimlane 2 and Swimlane 3:
1. One solid indigo #4F46E5 arrow from "Coding · 5.0 h" in Swimlane 2 down to "Coding + Cleanup · 8.0 h" in Swimlane 3 labelled "+3.0 h over-engineering cleanup".
2. One solid amber #B45309 arrow from the dashed slot "35.5 Hours Initially Saved by AI (-44%)" in Swimlane 2 down into the expanded right half of Swimlane 3 ("PR Review · 18.5 h (+85%)") labelled "+35.5 h absorbed by cleanup, debugging & PR review queues".
No other connectors. Summary cards and legend items have no connectors. Total connector count: 2.

LEGEND (VISIBLE):
Place a compact horizontal legend strip at the bottom outside the main boundary with five colour swatches, each label once:
- Blue #2563EB: "Hands-on coding & initial AI savings"
- Violet #7C3AED: "Agent K8s/DB debugging & test setup"
- Teal #0F766E: "System design & RFC specifications"
- Amber #B45309 (with person-and-check mark): "Human PR review & document review gate"
- Red #B91C1C: "Rework from code bloat, AI bugs & production incidents"

FINAL CHECK (PRIVATE, DO NOT PRINT):
Exactly three horizontal sprint swimlanes, six segments per bar, three summary cards on the right, two vertical arrows total, five legend items each once. No printed layout words, no percentages used as layout coordinates, no title above the canvas.
```

---

## Diagram 2 (`02-pipeline-bottleneck-analogy.jpg`): Producer-Database Queue Analogy vs. AI Sprint Bottleneck

**What it shows:** A two-panel comparison illustrating the **Pipeline Bottleneck Rule (Theory of Constraints)** for software engineers. Panel 1 shows a `1,000 ms` producer-to-database pipeline where making the Producer Worker `10×` faster (`300 ms → 30 ms`) only achieves `730 ms` (`1.37×`) single-job latency while throughput stays capped at 1 job per `700 ms`, and climbs past `1,000 ms+` when the fast producer submits `2×` more jobs than the database can drain (saturating both the connection pool and row locks). Panel 2 shows the parallel in an `80-hour` engineering sprint where AI is the producer and human engineers are the review/verification consumer pool.

### Prompt to Paste into Nano Banana Pro

```text
Create a two-panel horizontal comparison diagram contrasting a 1,000 ms producer-to-database pipeline (top panel) with an 80-hour software engineering sprint pipeline (bottom panel) when a 10x faster producer overloads a fixed downstream consumer. Output a high-resolution 16:9 landscape raster image. All directions below are private; print only the quoted labels and captions. No extra title, layout terminology or invented text.

VISUAL STYLE (PRIVATE):
White canvas, near-white group panels, crisp sans-serif such as Inter, dark slate text #0F172A with secondary #475569, fine 3px borders, consistent rounded corners, generous whitespace. Very pale tinted fills on cards with saturated colour only on small icons, left accent bars and outlines. The focal point is the bottom-right amber/red bottleneck card ("Human Review & Verification Queue · 80.0 Hours"), which has the strongest border and largest title. Avoid condensed type, tiny captions, broad grey backgrounds, heavy outlines, gradients, 3D, glows, textures, mascots, robots, or brains.

ICONS (PRIVATE):
One small simple line icon beside each card name: a server-cpu icon on Producer Worker, a database-lock icon on Database Queue Overload, a code-brackets icon on Initial AI Generation, and a person-and-check badge on Human Review & Verification Queue. No invented brand logos.

SPATIAL LAYOUT AND EXACT LABELS (PRIVATE):
Arrange the canvas into two large horizontal group panels stacked top and bottom across most of the canvas, with a legend strip at the bottom outside the main boundary.

Top Group Panel labelled "1. Systems Analogy: Fast Producer Overloading a Fixed Database":
Inside the top panel, place three horizontal flow cards from left to right:
- First top card (blue #2563EB accent, #EFF6FF fill): "Baseline Job · 1,000 ms" with caption "300 ms Producer Worker + 700 ms DB Commit (1 job / 700 ms)"
- Second top card (indigo #4F46E5 accent, #EEF2FF fill): "10x Faster Producer · 730 ms (1.37x)" with caption "Producer drops 300 ms -> 30 ms · DB still caps throughput at 700 ms"
- Third top card (red #B91C1C accent, #FFF1F2 fill): "Producer Floods DB · 1,000 ms+ (Rising)" with caption "Pool wait + row lock contention erase 270 ms saved as backlog grows"

Bottom Group Panel labelled "2. Sprint Reality: Fast AI Generation Flooding Human Engineers (80.0 Hours)":
Inside the bottom panel, place three horizontal flow cards from left to right aligned directly below the three top cards:
- First bottom card (blue #2563EB accent, #EFF6FF fill): "Baseline Sprint · 80.0 Hours" with caption "24.0 h Hands-On Coding (30%) + 56.0 h Design, Review, Debug & Ops (70%)"
- Second bottom card (indigo #4F46E5 accent, #EEF2FF fill): "Initial AI Speedup · 44.5 Hours (1.80x)" with caption "AI Producer saves -35.5 h across Coding, K8s/SQL Checks, RFCs & Notes"
- Third bottom focal card (amber #B45309 accent, #FFFBEB fill, bold border, person-and-check mark): "Human Review & Verification Queue · 80.0 Hours" with caption "2x PRs (+154% size, +54% bugs) hit same or smaller team after AI layoffs (+35.5 h)"

VISUAL CONNECTIONS (PRIVATE):
Use medium solid indigo #4F46E5 arrows and solid red #B91C1C arrows:
1. In the Top Panel, one solid indigo #4F46E5 arrow from "Baseline Job · 1,000 ms" to "10x Faster Producer · 730 ms (1.37x)" labelled "10x faster producer", and one solid red #B91C1C arrow from "10x Faster Producer · 730 ms (1.37x)" to "Producer Floods DB · 1,000 ms+ (Rising)" labelled "Arrival rate > DB service rate".
2. In the Bottom Panel, one solid indigo #4F46E5 arrow from "Baseline Sprint · 80.0 Hours" to "Initial AI Speedup · 44.5 Hours (1.80x)" labelled "AI across all 6 stages (-35.5 h)", and one solid red #B91C1C arrow from "Initial AI Speedup · 44.5 Hours (1.80x)" to "Human Review & Verification Queue · 80.0 Hours" labelled "Cleanup & review queue (+35.5 h)".
No vertical arrows crossing between panels. Total connector count: 4.

LEGEND (VISIBLE):
Place a compact legend strip at the bottom outside the main boundary with three colour swatches, each label once:
- Blue #2563EB: "Baseline pipeline (Producer + Consumer)"
- Indigo #4F46E5: "Speeding up the producer alone (single-job ceiling)"
- Amber #B45309 / Red #B91C1C: "Downstream consumer overloaded when arrival rate exceeds capacity"

FINAL CHECK (PRIVATE, DO NOT PRINT):
Exactly two horizontal group panels, three cards per panel (six cards total), four horizontal arrows total, three legend items each once. Do not print node letters or codes such as A1, A2, A3, B1, B2, or B3 on any card. No printed layout words, no title above the canvas.
```

---

## Diagram 3 (`03-stage-by-stage-tug-of-war.jpg`): Stage-by-Stage Tug-of-War (`-35.5 h` Saved vs. `+35.5 h` Rebound)

**What it shows:** A two-column paired breakdown across all six sprint stages showing **what AI speeds up on the left (`-35.5 h` total)** versus **what AI slows down via cleanup, debugging, and review load on the right (`+35.5 h` total)**.

### Prompt to Paste into Nano Banana Pro

```text
Create a comparison diagram of the six software sprint stages showing Initial AI Time Saved on the left versus Cleanup, Debugging, and Review Hours Added on the right across an 80-hour two-week sprint. Output a high-resolution 16:9 landscape raster image. All directions below are private; print only the quoted labels and captions. No extra title, layout terminology or invented text.

VISUAL STYLE (PRIVATE):
White canvas, near-white group panels, crisp sans-serif such as Inter, dark slate text #0F172A with secondary #475569, fine 3px borders, consistent rounded corners, generous whitespace. Very pale tinted fills on cards with saturated colour only on small icons, left accent bars and outlines. The focal point is Row 5 on the right ("PR Review Queue & Bot Noise · +10.5 h"), which has the strongest amber border and largest title. Avoid condensed type, tiny captions, broad grey backgrounds, heavy outlines, gradients, 3D, glows, textures, mascots, robots, or brains.

ICONS (PRIVATE):
One small simple line icon beside each card title, same size and stroke throughout: a lightning bolt on left-column speedup cards, a warning-magnifier or person-and-check mark on right-column review tax cards. No invented brand logos.

SPATIAL LAYOUT AND EXACT LABELS (PRIVATE):
Arrange the canvas into two equal columns (left header "Initial AI Time Saved · -35.5 h" in blue #2563EB and right header "Cleanup, Debugging & Review Tax · +35.5 h" in amber #B45309) separated by a narrow central spine of six stage badges, with six horizontal rows aligned across both columns and a bottom totals bar.

Row 1 (Hands-On Coding):
- Left blue #2563EB card (#EFF6FF fill): "Boilerplate & Feature Generation · -19.0 h" with caption "24.0 h -> 5.0 h initial coding time"
- Center slate badge: "1. Coding (Net: 8.0 h)"
- Right red #B91C1C card (#FFF1F2 fill): "Over-Engineered Code & Clones · +3.0 h" with caption "GitClear: -70% refactoring, +81% duplication"

Row 2 (Debugging, K8s/DB & Tests):
- Left violet #7C3AED card (#F5F3FF fill): "kubectl, Pod Logs, SQL & Test Drafts · -5.5 h" with caption "12.0 h -> 6.5 h log & SQL checks"
- Center slate badge: "2. Debug & Test (Net: 14.5 h)"
- Right red #B91C1C card (#FFF1F2 fill): "Unfamiliar AI Bugs & False Leads · +8.0 h" with caption "Faros: +54% bugs/dev · confident false theories"

Row 3 (System Design & RFCs):
- Left teal #0F766E card (#F0FDFA fill): "Instant Architecture & RFC Drafts · -3.5 h" with caption "12.0 h -> 8.5 h initial drafting"
- Center slate badge: "3. Design (Net: 14.0 h)"
- Right amber #B45309 card (#FFFBEB fill): "Rewriting Design Workslop · +5.5 h" with caption "Stanford/HBR: 1h 56m lost per workslop doc"

Row 4 (Planning, Meetings & Slides):
- Left blue #2563EB card (#EFF6FF fill): "AI Meeting Minutes, Slides & Tickets · -3.5 h" with caption "12.0 h -> 8.5 h note taking"
- Center slate badge: "4. Planning (Net: 12.0 h)"
- Right amber #B45309 card (#FFFBEB fill): "Ticket Inflation & +67% Parallel WIP · +3.5 h" with caption "Faros: +26% stalled tasks (>7 days idle)"

Row 5 (PR Code Review, Focal Row):
- Left blue #2563EB card (#EFF6FF fill): "AI Review Bots (Lint & Syntax) · -2.0 h" with caption "10.0 h -> 8.0 h surface checks"
- Center slate badge: "5. PR Review (Net: 18.5 h)"
- Right focal amber #B45309 card (#FFFBEB fill, bold border, person-and-check mark): "PR Review Queue & Bot Noise · +10.5 h" with caption "MSR '26: <30% bot signal · LinearB: 5.3x wait"

Row 6 (CI/CD, Deploy & Prod Ops):
- Left blue #2563EB card (#EFF6FF fill): "Helm/Terraform YAML & CI Log Parse · -2.0 h" with caption "10.0 h -> 8.0 h config writing"
- Center slate badge: "6. CI/CD & Ops (Net: 13.0 h)"
- Right red #B91C1C card (#FFF1F2 fill): "2x CI Queues & +242% Incidents/PR · +5.0 h" with caption "Faros 2026: 3.4x higher incident rate per PR"

Bottom Summary Strip spanning both columns:
- Left summary card (blue #2563EB accent): "Total Initial AI Savings: -35.5 Hours (80.0 h -> 44.5 h)"
- Right summary card (amber #B45309 accent): "Total Cleanup & Review Tax: +35.5 Hours (44.5 h -> 80.0 h · 1.21x Net Output)"

VISUAL CONNECTIONS (PRIVATE):
In each of the six rows, draw one short solid blue #2563EB arrow from the left card into the center stage badge, and one short solid amber #B45309 arrow from the center stage badge into the right card (12 short horizontal arrows total, 2 per row). No vertical or diagonal arrows between rows. Bottom summary cards and legend items have no connectors. Total connector count: 12.

LEGEND (VISIBLE):
Place a compact legend strip at the bottom outside the main boundary with three colour swatches, each label once:
- Blue #2563EB / Violet #7C3AED / Teal #0F766E: "Initial drafting & log-check hours saved by AI (-35.5 h)"
- Amber #B45309 (with person-and-check mark): "Human review & document cleanup tax"
- Red #B91C1C: "Code bloat cleanup, bug fixes & production incident tax"

FINAL CHECK (PRIVATE, DO NOT PRINT):
Exactly six aligned rows, one left card, one center badge, and one right card per row, two bottom summary cards, 12 short horizontal arrows total, three legend items each once. Do not print the words "Left Column:" or "Right Column:" in the headers. No printed layout words, no title above the canvas.
```

---

## Diagram 4 (`04-write-only-code-bloat.jpg`): Human Refactoring vs. AI "Write-Only" Code Bloat

**What it shows:** Why Stage 1 (Hands-on Coding) requires `+3.0 h` of cleanup and creates downstream debt: compares **Human-Authored Modular Refactoring** (`0.37` refactor rate, consolidating shared functions) with **AI "Write-Only" Additive Bloat** (`-70%` refactoring drop, `+81%` duplicated blocks, `+47%` defensive error-masking wrappers, and `-74%` legacy maintenance from GitClear 2026 and LinearB 2026).

### Prompt to Paste into Nano Banana Pro

```text
Create a two-column structural comparison diagram contrasting Human Modular Refactoring (left column) with AI Write-Only Code Bloat and Wrapper Accumulation (right column), backed by GitClear 2026 and LinearB 2026 research metrics. Output a high-resolution 16:9 landscape raster image. All directions below are private; print only the quoted labels and captions. No extra title, layout terminology or invented text.

VISUAL STYLE (PRIVATE):
White canvas, near-white group panels, crisp sans-serif such as Inter, dark slate text #0F172A with secondary #475569, fine 3px borders, consistent rounded corners, generous whitespace. Very pale tinted fills on cards with saturated colour only on small icons, left accent bars and outlines. The focal point is the right-hand red panel ("AI Write-Only Mode (Additive Wrapper Bloat)"), which has the strongest border and largest title. Avoid condensed type, tiny captions, broad grey backgrounds, heavy outlines, gradients, 3D, glows, textures, mascots, robots, or brains.

ICONS (PRIVATE):
One small simple line icon beside each card name: a clean modular-cube icon on the left human cards, a copy-paste clone icon and warning shield on the right AI bloat cards. No invented brand logos.

SPATIAL LAYOUT AND EXACT LABELS (PRIVATE):
Arrange the canvas into two equal side-by-side panels with a legend strip outside the bottom boundary.

Left Panel (blue #2563EB outline, #F8FAFC background) labelled "Human Engineering (Refactor & Reuse Mode)":
Inside the left panel, show a clean three-card vertical architecture:
- First left card (blue #2563EB accent, #EFF6FF fill): "1. Understand Existing Module Graph" with caption "Reads cross-file callers & domain invariants before editing"
- Second left card (teal #0F766E accent, #F0FDFA fill): "2. Move & Consolidate Shared Logic" with caption "LinearB P75 Refactor Rate: 0.37 (1.5x to 2.2x higher than AI PRs)"
- Third left card (indigo #4F46E5 accent, #EEF2FF fill): "3. Compact, Incremental Diff (~157 LOC)" with caption "Single source of truth · Easy for teammates to review & debug"

Right Panel (focal red #B91C1C outline, #FFF1F2 pale tint) labelled "AI Write-Only Mode (Additive Wrapper Bloat)":
Inside the right panel, show four stacked cards illustrating structural erosion:
- First right card (red #B91C1C accent, white fill): "1. Loses Cross-File Context (-35% Reuse)" with caption "Avoids touching existing modules · Invents parallel helper files"
- Second right card (red #B91C1C accent, white fill): "2. Copy-Paste Clones (+81% Block Duplication)" with caption "GitClear 2026: Moved lines fell 21% -> 3.8% (-70% refactoring)"
- Third right card (amber #B45309 accent, #FFFBEB fill): "3. Defensive Error-Masking (+47% Guards)" with caption "Wraps broken state in try/catch, null-checks & fallback mocks"
- Fourth right card (red #B91C1C accent, white fill): "4. Bloated PR Diff (293 to 408 LOC at P75)" with caption "-74% legacy maintenance · Requires +3.0 h cleanup per sprint"

VISUAL CONNECTIONS (PRIVATE):
1. Inside the Left Panel, draw two solid blue #2563EB vertical arrows connecting "1. Understand Existing Module Graph" -> "2. Move & Consolidate Shared Logic" -> "3. Compact, Incremental Diff (~157 LOC)".
2. Inside the Right Panel, draw three solid red #B91C1C vertical arrows connecting "1. Loses Cross-File Context (-35% Reuse)" -> "2. Copy-Paste Clones (+81% Block Duplication)" -> "3. Defensive Error-Masking (+47% Guards)" -> "4. Bloated PR Diff (293 to 408 LOC at P75)".
No arrows between the Left Panel and Right Panel. Total connector count: 5.

LEGEND (VISIBLE):
Place a compact legend strip at the bottom outside the main boundary with three colour swatches, each label once:
- Blue #2563EB / Teal #0F766E: "Modular refactoring & cross-file reuse"
- Amber #B45309: "Error-masking wrappers that hide root causes (+47%)"
- Red #B91C1C: "Code duplication (+81%) & dropped refactoring (-70%)"

FINAL CHECK (PRIVATE, DO NOT PRINT):
Two side-by-side panels, three cards in the left panel, four cards in the right panel, five vertical arrows total, three legend items each once. Do not print the prefixes "Left:" or "Right:" in the panel headers. No printed layout words, no title above the canvas.
```

---

## Diagram 5 (`05-debugging-mental-map-gap.jpg`): K8s/SQL Agent Investigation vs. The Mental Map & Bug Rebound

**What it shows:** The Stage 2 debugging paradox (`12.0 h → 6.5 h initial → 14.5 h net`). Coding agents save `-5.5 hours` by automating `kubectl logs`, `kubectl exec`, port-forwarding, SQL queries, and CI log parsing. However, they add `+8.0 hours` back because engineers lack a **mental map** of AI-written code, chase **confident false root-cause theories** (Microsoft Research 2026), and fix **flawed AI unit tests that pass on buggy code** (`+54%` bugs/dev, Faros AI 2026).

### Prompt to Paste into Nano Banana Pro

```text
Create a workflow diagram of Stage 2 (Debugging, Kubernetes/Database Investigation, and Testing in an 80-hour sprint), showing how AI agents save 5.5 hours on log and SQL gathering but add 8.0 hours via the Missing Mental Map, confident false theories, and flawed AI unit tests. Output a high-resolution 16:9 landscape raster image. All directions below are private; print only the quoted labels and captions. No extra title, layout terminology or invented text.

VISUAL STYLE (PRIVATE):
White canvas, near-white group panels, crisp sans-serif such as Inter, dark slate text #0F172A with secondary #475569, fine 3px borders, consistent rounded corners, generous whitespace. Very pale tinted fills on cards with saturated colour only on small icons, left accent bars and outlines. The focal point is the right-hand red panel ("Phase 2: The +8.0 h Mental Map & Bug Rebound (6.5 h -> 14.5 h)"), which has the strongest border and largest title. Avoid condensed type, tiny captions, broad grey backgrounds, heavy outlines, gradients, 3D, glows, textures, mascots, robots, or brains.

ICONS (PRIVATE):
One small simple line icon beside each card name: a terminal icon on kubectl/Pod Logs, a database cylinder icon on Postgres SQL Checks, a compass-question icon on Missing Mental Map, a warning-alert icon on Confident False Theory, and a check-x icon on Flawed AI Unit Tests. No invented brand logos.

SPATIAL LAYOUT AND EXACT LABELS (PRIVATE):
Arrange the canvas from left to right across two main phases plus a bottom net-math bar and a legend strip outside the bottom boundary.

Left Panel (violet #7C3AED outline, #F5F3FF pale tint) labelled "Phase 1: Automated Log & SQL Gathering (-5.5 h Saved · 12.0 h -> 6.5 h)":
Inside the left panel, stack three horizontal cards:
- First left card (violet #7C3AED accent, white fill): "1. Kubernetes & Pod Agent" with caption "Runs kubectl logs, kubectl exec, port-forward & live API probes"
- Second left card (blue #2563EB accent, white fill): "2. Database & CI Pipeline Agent" with caption "Connects to PostgreSQL, runs diagnostic SQL & reads CI failure traces"
- Third left card (teal #0F766E accent, white fill): "3. Automated Test Generator" with caption "Generates unit & integration test files in seconds"

Right Panel (focal red #B91C1C outline, #FFF1F2 pale tint) labelled "Phase 2: The +8.0 h Mental Map & Bug Rebound (6.5 h -> 14.5 h)":
Inside the right panel, stack three horizontal cards aligned with the three left cards:
- First right focal card (red #B91C1C accent, white fill, bold border): "1. The Missing-Mental-Map Penalty (+3.5 h)" with caption "Engineer did not write the code · Must reverse-engineer AI logic during live outage"
- Second right card (amber #B45309 accent, #FFFBEB fill): "2. Confident False Root-Cause Theories (+2.5 h)" with caption "Microsoft Research (2026): Plausible but wrong theories waste hours on dead ends"
- Third right card (red #B91C1C accent, white fill): "3. Flawed AI Tests & +54% Bugs/Dev (+2.0 h)" with caption "AI tests mock out or lock in the buggy behavior · Faros 2026: +54% bugs/dev"

Bottom Net Math Card spanning both panels (indigo #4F46E5 accent, #EEF2FF fill):
"Stage 2 Net Balance: 12.0 h Pre-AI  -  5.5 h Agent Log/SQL Checks  +  8.0 h Mental Map & Bug Fixes  =  14.5 Hours (+2.5 h Net Increase)"

VISUAL CONNECTIONS (PRIVATE):
Draw three horizontal dashed steel-blue #0369A1 arrows connecting each Left Panel card to its corresponding Right Panel card:
1. From "1. Kubernetes & Pod Agent" to "1. The Missing-Mental-Map Penalty (+3.5 h)" labelled "Logs gathered, but code is unfamiliar".
2. From "2. Database & CI Pipeline Agent" to "2. Confident False Root-Cause Theories (+2.5 h)" labelled "SQL run, but root cause is wrong".
3. From "3. Automated Test Generator" to "3. Flawed AI Tests & +54% Bugs/Dev (+2.0 h)" labelled "Tests pass, but lock in buggy logic".
Bottom Net Math Card and legend items have no connectors. Total connector count: 3.

LEGEND (VISIBLE):
Place a compact legend strip at the bottom outside the main boundary with three colour swatches, each label once:
- Violet #7C3AED / Blue #2563EB: "Automated CLI, K8s & SQL log gathering (-5.5 h)"
- Amber #B45309: "False root-cause leads requiring human verification"
- Red #B91C1C: "Mental map reconstruction & escaped bug fixes (+8.0 h)"

FINAL CHECK (PRIVATE, DO NOT PRINT):
Two side-by-side phase panels, three cards per panel, one bottom net math card, three horizontal dashed arrows total, three legend items each once. Do not print node codes such as L1, L2, L3, R1, R2, or R3 on any card or arrow. No printed layout words, no title above the canvas.
```

---

## Diagram 6 (`06-workslop-and-review-bot-noise.jpg`): The "Workslop" Transfer Tax & Code Review Bot Noise

**What it shows:** How AI transfers effort from the **author** to **teammates** in Stages 3, 4, and 5:
1. **Top Half (The Workslop Tax in Design & Planning):** Author saves `20 min` prompting a 10-page RFC or 3-page meeting deck, shifting **1 hour 56 minutes per incident** of reading/rewriting work onto teammates (Stanford/BetterUp HBR 2025, `40%` prevalence) and causing **`+13.8%` task restarts** (Faros 2026).
2. **Bottom Half (The PR Review & Bot Noise Logjam):** Author pushes `+98%` more PRs (`+154%` larger); AI review bots generate **`<30%` signal on `60.2%` of closed PRs** (MSR ’26) and increase PR closure time by **`+42%` (`5h 52m → 8h 20m`, Cihan et al.)**, while human reviewers wait **`5.3×` longer for pickup (`17.6 h` vs `3.3 h`, LinearB 2026)**.

### Prompt to Paste into Nano Banana Pro

```text
Create a two-tier flow diagram illustrating how AI shifts effort from the author to teammates across System Design/Docs (Top Tier: The Workslop Transfer Tax) and Pull Request Code Review (Bottom Tier: Review Bot Noise and Queue Logjam). Output a high-resolution 16:9 landscape raster image. All directions below are private; print only the quoted labels and captions. No extra title, layout terminology or invented text.

VISUAL STYLE (PRIVATE):
White canvas, near-white group panels, crisp sans-serif such as Inter, dark slate text #0F172A with secondary #475569, fine 3px borders, consistent rounded corners, generous whitespace. Very pale tinted fills on cards with saturated colour only on small icons, left accent bars and outlines. The focal point is the bottom-right amber/red card ("3. Human Reviewer Queue · 18.5 h (+85% Load)"), which has the strongest border and largest title. Avoid condensed type, tiny captions, broad grey backgrounds, heavy outlines, gradients, 3D, glows, textures, mascots, robots, or brains.

ICONS (PRIVATE):
One small simple line icon beside each card name: a file-text icon on AI RFC/Slide Generator, a clock-warning icon on Workslop Receiver Tax, a bot-comment icon on AI Code Review Bot, and a person-and-check badge on Human Reviewer Queue. No invented brand logos.

SPATIAL LAYOUT AND EXACT LABELS (PRIVATE):
Arrange the canvas into two horizontal tiers stacked top and bottom across most of the canvas, with three flow cards per tier (left to right) and a legend strip at the bottom outside the main boundary.

Top Tier Panel labelled "Tier 1: System Design, RFCs & Meeting Docs (The Workslop Transfer Tax)":
- First top card (teal #0F766E accent, #F0FDFA fill): "1. Author Prompts AI (Saves ~20 min)" with caption "Generates 10-page RFC, slide deck or 15 Jira subtasks in one shot"
- Second top card (amber #B45309 accent, #FFFBEB fill): "2. Polished But Context-Free 'Workslop'" with caption "Stanford/HBR (2025): 40% of workers receive it · Generic patterns, unstated assumptions"
- Third top card (red #B91C1C accent, #FFF1F2 fill): "3. Teammates Spend 1 hr 56 min Per Doc" with caption "Team fact-checks & rewrites spec · Faros 2026: +13.8% task restarts (+5.5 h design tax)"

Bottom Tier Panel labelled "Tier 2: Pull Request Review & AI Review Agents (The Review Queue Logjam)":
- First bottom card (blue #2563EB accent, #EFF6FF fill): "1. Author Pushes +98% More & +154% Larger PRs" with caption "LinearB 2026: P75 diff jumps from 157 LOC (manual) to 293 to 408 LOC (AI)"
- Second bottom card (amber #B45309 accent, #FFFBEB fill): "2. AI Code Review Bot Adds Low-Signal Noise" with caption "MSR '26: 12 of 13 bots <60% signal · Cihan et al.: PR closure time +42% (5h52m -> 8h20m)"
- Third bottom focal card (amber #B45309 accent, #FFFBEB fill, bold border, person-and-check mark): "3. Human Reviewer Queue · 18.5 h (+85% Load)" with caption "5.3x longer pickup wait (17.6h vs 3.3h) · <60% AI PR acceptance · 31% merge unreviewed"

VISUAL CONNECTIONS (PRIVATE):
1. In Top Tier, draw two solid amber #B45309 horizontal arrows: from "1. Author Prompts AI (Saves ~20 min)" to "2. Polished But Context-Free 'Workslop'" labelled "Unedited output", and from "2. Polished But Context-Free 'Workslop'" to "3. Teammates Spend 1 hr 56 min Per Doc" labelled "Effort shifted to team".
2. In Bottom Tier, draw two solid red #B91C1C horizontal arrows: from "1. Author Pushes +98% More & +154% Larger PRs" to "2. AI Code Review Bot Adds Low-Signal Noise" labelled "Large diff triggers bot comments", and from "2. AI Code Review Bot Adds Low-Signal Noise" to "3. Human Reviewer Queue · 18.5 h (+85% Load)" labelled "Noise + missing context stalls review".
No vertical connectors between tiers. Total connector count: 4.

LEGEND (VISIBLE):
Place a compact legend strip at the bottom outside the main boundary with three colour swatches, each label once:
- Teal #0F766E / Blue #2563EB: "Fast upstream AI draft generation (Author)"
- Amber #B45309 (with person-and-check mark): "Workslop & low-signal bot noise (<30% to 60% signal)"
- Red #B91C1C: "Downstream human review & queue delay (+42% to +441%)"

FINAL CHECK (PRIVATE, DO NOT PRINT):
Exactly two horizontal tiers, three cards per tier (six cards total), four horizontal arrows total, three legend items each once. No printed layout words, no title above the canvas.
```

---

## Diagram 7 (`07-verification-funnel-guardrails.jpg`): The Full-Stack AI Review Funnel & Engineering Playbook

**What it shows:** A system-architecture style flowchart showing how AI agents across Coding, K8s/SQL Debugging, RFC Design, and Meetings feed into the Human Review & Approval Gate, contrasting **Path A: Undisciplined AI Output** (`+35.5 h` rebound, `+242.7%` incidents/PR) with **Path B: High-Performing Engineering Guardrails** (`<150 LOC` small batches, pre-commit IDE checks, 1-page human-written specs, read-only K8s/SQL summaries).

### Prompt to Paste into Nano Banana Pro

```text
Create a system overview diagram of the software delivery pipeline showing how full-lifecycle AI agents feed into the human review gate, comparing undisciplined AI output against practical engineering guardrails. Output a high-resolution 16:9 landscape raster image. All directions below are private; print only the quoted labels and captions. No extra title, layout terminology or invented text.

VISUAL STYLE (PRIVATE):
White canvas, near-white group panels, crisp sans-serif such as Inter, dark slate text #0F172A with secondary #475569, fine 3px borders, consistent rounded corners, generous whitespace. Very pale tinted fills on cards with saturated colour only on small icons, left accent bars and outlines. The focal point is the central amber gate card ("Human Review & Verification Gate"), which has the strongest border and largest name. Avoid condensed type, tiny captions, broad grey backgrounds, heavy outlines, gradients, 3D, glows, textures, mascots, robots, or brains.

ICONS (PRIVATE):
One small simple line icon beside each component name: terminal/code icons on the four left AI inputs, a person-and-check badge on the central Human Review Gate, a warning triangle on the top red failure path, and a check-shield icon on the bottom indigo guardrail path. No invented brand logos.

SPATIAL LAYOUT AND EXACT LABELS (PRIVATE):
Arrange the canvas from left to right across three well-spaced zones: Left Zone (Four Full-Lifecycle AI Generators), Center Zone (The Review Bottleneck Gate), and Right Zone (Two Diverging Delivery Outcomes).

Left Zone (stacked vertically inside a light panel labelled "Full-Lifecycle AI Generation (-35.5 h Initial Saved)"):
- Card 1 (blue #2563EB accent, #EFF6FF fill): "AI Coding Agents" with caption "2x PR volume · +154% larger diffs · +81% clones"
- Card 2 (violet #7C3AED accent, #F5F3FF fill): "K8s, Pod Log & SQL Agents" with caption "Fast logs · confident root-cause guesses"
- Card 3 (teal #0F766E accent, #F0FDFA fill): "AI RFC & Design Generators" with caption "10-page specs · generic patterns"
- Card 4 (slate #475569 accent, #F8FAFC fill): "AI Meeting Notes & PR Bots" with caption "Auto-tickets · <30% signal bot comments"

Center Zone (single large focal card):
- Focal Card (amber #B45309 accent, #FFFBEB fill, bold 3px border, person-and-check mark): "Human Review & Verification Gate" with caption "The True Sprint Bottleneck · Must check intent, architecture, edge cases & prod safety"

Right Zone (two stacked outcome panels):
- Top Right Panel (red #B91C1C accent, #FFF1F2 fill): "Path A: Undisciplined AI (The Slop Flood)" with three internal metric badges:
  1. "PR Review Time: +91% to +441%"
  2. "Workslop Tax: 1h 56m lost per doc"
  3. "Prod Incidents/PR: +242.7% · DORA Flat"
- Bottom Right Panel (indigo #4F46E5 accent, #EEF2FF fill): "Path B: High-Performing Guardrails (Bounded Delegation)" with three internal guardrail badges:
  1. "Small Batches (<150 LOC) & Pre-Push AI Check"
  2. "1-Page Human-Written Specs (Zero Raw Slop)"
  3. "Read-Only K8s/SQL Summaries + Human Sign-Off"

VISUAL CONNECTIONS (PRIVATE):
Use medium solid indigo #4F46E5 arrows, solid red #B91C1C arrows, and solid amber #B45309 arrows:
1. One vertical spine collecting the four Left Zone cards into one solid indigo #4F46E5 arrow entering the left side of "Human Review & Verification Gate" labelled "High-volume AI output".
2. One solid red #B91C1C arrow from the top-right of "Human Review & Verification Gate" to "Path A: Undisciplined AI (The Slop Flood)" labelled "No batch limits or spec filters (+35.5 h rebound)".
3. One solid indigo #4F46E5 arrow from the bottom-right of "Human Review & Verification Gate" to "Path B: High-Performing Guardrails (Bounded Delegation)" labelled "Left-shifted quality gates (Keeps AI speedup)".
No other connectors. Internal badges and legend items have no connectors. Total connector count: 3 (counting the left fan-in spine as 1 combined connector plus 2 outgoing branches).

LEGEND (VISIBLE):
Place a compact legend strip at the bottom outside the main boundary with three colour swatches, each label once:
- Blue #2563EB / Violet #7C3AED / Teal #0F766E: "AI generation & automated log gathering"
- Amber #B45309 (with person-and-check mark): "Human review & accountability gate"
- Red #B91C1C vs Indigo #4F46E5: "Rebound path vs Engineered guardrail path"

FINAL CHECK (PRIVATE, DO NOT PRINT):
Four input cards on the left, one focal gate card in the center, two outcome panels on the right (each with three internal badges), one fan-in spine and two outgoing arrows, three legend items each once. No printed layout words, no title above the canvas.
```

---

## Diagram 8 (`08-in-chat-progressive-zoom.jpg`): Stopping In-Chat Workslop: 5-Paragraph Dump vs. Progressive Zoom & Subagents

**What it shows:** A two-column comparison for **Section 6.1** contrasting **Default AI Chat Mode (The 5-Paragraph Wall of Text)**: where raw file searches, line-by-line diff narration, and edge-case trivia bury the architectural decision in paragraph 4 and overload human working memory: against **Engineered Harness Mode (BLUF + Progressive Zoom + Isolated Subagent)** configured via `CLAUDE.md`, `AGENTS.md`, `GEMINI.md`, and `.cursor/rules/`.

### Prompt to Paste into Nano Banana Pro

```text
Create a two-column comparison diagram contrasting Default AI Coding Chat (Left: The 5-Paragraph Wall-of-Text Dump) with Engineered Progressive Zoom and Subagent Isolation (Right: Big Picture First, Details on Demand). Output a high-resolution 16:9 landscape raster image. All directions below are private; print only the quoted labels and captions. No extra title, layout terminology or invented text.

VISUAL STYLE (PRIVATE):
White canvas, near-white group panels, crisp sans-serif such as Inter, dark slate text #0F172A with secondary #475569, fine 3px borders, consistent rounded corners, generous whitespace. Very pale tinted fills on cards with saturated colour only on small icons, left accent bars and outlines. The focal point is the right-hand indigo/blue panel ("Engineered Harness: BLUF + Progressive Zoom + Subagents"), specifically its "Zoom Level 1: 30-Second Mental Map (Default)" card, which has the strongest border and largest title. Avoid condensed type, tiny captions, broad grey backgrounds, heavy outlines, gradients, 3D, glows, textures, mascots, robots, or brains.

ICONS (PRIVATE):
One small simple line icon beside each card name: a warning-text icon on the left wall-of-text cards, a compass-map icon on Zoom Level 1, a filter-funnel icon on Isolated Explorer Subagent, and asliders/layers icon on Zoom Levels 2 & 3. No invented brand logos.

SPATIAL LAYOUT AND EXACT LABELS (PRIVATE):
Arrange the canvas into two equal side-by-side panels with a bottom configuration strip and a compact legend outside the bottom boundary.

Left Panel (red #B91C1C outline, #FFF1F2 pale tint) labelled "1. Default AI Chat UI (The 5-Paragraph Wall-of-Text Dump)":
Inside the left panel, stack four cards showing how the mental map gets buried:
- First left card (red #B91C1C accent, white fill): "Paragraphs 1 to 2: Tool & File Narration Noise" with caption "Lists every file opened, grep run & line touched in main context"
- Second left card (red #B91C1C accent, white fill): "Paragraph 3: Line-by-Line Diff Repetition" with caption "Narrates code changes in prose that are already visible in the IDE diff"
- Third left card (amber #B45309 accent, #FFFBEB fill): "Paragraph 4: The Actual Architectural Decision (Buried)" with caption "Key trade-off or root cause hidden inside 500 words of low-level trivia"
- Fourth left card (red #B91C1C accent, white fill): "Result: Working Memory Overload & Lost Mental Map" with caption "Developer skims, loses the big picture & rubber-stamps the change"

Right Panel (focal indigo #4F46E5 outline, #EEF2FF pale tint) labelled "2. Engineered Harness (BLUF + Progressive Zoom + Subagents)":
Inside the right panel, stack four clean cards showing controlled disclosure:
- First right card (violet #7C3AED accent, white fill): "Step 0: Isolated Subagent (mental-map-explorer.md)" with caption "Runs 15-file search & K8s/SQL log checks in isolated context · Returns 15-line brief"
- Second right focal card (indigo #4F46E5 accent, white fill, bold 4px border): "Zoom Level 1: 30-Second Mental Map (Default Response)" with caption "1-sentence BLUF + 5-node ASCII/Mermaid flow + top 3 file:line boundaries · STOPS HERE"
- Third right card (teal #0F766E accent, #F0FDFA fill): "Zoom Level 2: Mechanism & State Flow (On Request Only)" with caption "Shown only when developer replies 'Zoom 1' · Locks, failure modes & trade-offs"
- Fourth right card (blue #2563EB accent, #EFF6FF fill): "Zoom Level 3: Nitty-Gritty Code & Logs (On Request Only)" with caption "Exact code blocks & collapsible <details> logs · Post-edit lists file:line paths only"

Bottom Configuration Bar spanning both panels (slate #334155 outline, #F8FAFC fill):
"Configured via: CLAUDE.md (/output-style concise)  ·  AGENTS.md  ·  GEMINI.md  ·  .cursor/rules/anti-slop-and-bluf.mdc  ·  codex-config.toml (verbosity = low)"

VISUAL CONNECTIONS (PRIVATE):
1. Inside Left Panel, draw three solid red #B91C1C vertical arrows connecting Paragraph 1-2 -> Paragraph 3 -> Paragraph 4 -> Result.
2. Inside Right Panel, draw one solid violet #7C3AED arrow from "Step 0: Isolated Subagent" to "Zoom Level 1: 30-Second Mental Map" labelled "Distilled 15-line brief", and two dashed indigo #4F46E5 arrows from Zoom Level 1 -> Zoom Level 2 -> Zoom Level 3 labelled "Only when human asks to zoom in". Total connector count: 6.

LEGEND (VISIBLE):
Place a compact legend strip at the bottom outside the main boundary with three colour swatches, each label once:
- Red #B91C1C / Amber #B45309: "Unfiltered chat dump (buries key decision in nitty-gritty detail)"
- Violet #7C3AED: "Subagent context isolation (keeps raw searches out of main chat)"
- Indigo #4F46E5 / Teal #0F766E: "Progressive Zoom (30-second big picture first, details on demand)"

FINAL CHECK (PRIVATE, DO NOT PRINT):
Two side-by-side panels, four cards per panel, one bottom config bar, six vertical arrows total, three legend items each once. No printed layout words, no title above the canvas.
```

---

## Diagram 9 (`09-stage-by-stage-mitigation-architecture.jpg`): Stage-by-Stage Engineering Mitigations Across the 6 Sprint Stages

**What it shows:** A six-card architectural grid for **Section 6.2 & 6.3** mapping each of the six sprint stages (`Coding`, `Debugging & Testing`, `System Design`, `Sprint Planning`, `PR Code Review`, and `CI/CD & Prod Ops`) to its specific AI failure mode and the concrete engineering gate/tool that solves it (`jscpd --fail-on-new-clones`, `TestSuiteBench` / `Stryker` mutation testing, 1-page RFCs + `<details>`, `WIP = 1` + completion evidence, Stacked PRs `<150 LOC` + IDE pre-push review, and batched/scoped merge queues + canary flags).

### Prompt to Paste into Nano Banana Pro

```text
Create a six-stage architectural grid diagram showing the specific AI bottleneck and the corresponding engineering mitigation gate across all six stages of an 80-hour software engineering sprint. Output a high-resolution 16:9 landscape raster image. All directions below are private; print only the quoted labels and captions. No extra title, layout terminology or invented text.

VISUAL STYLE (PRIVATE):
White canvas, near-white group panels, crisp sans-serif such as Inter, dark slate text #0F172A with secondary #475569, fine 3px borders, consistent rounded corners, generous whitespace. Very pale tinted fills on cards with saturated colour only on small icons, left accent bars and outlines. Arrange as a clean 2-row by 3-column pipeline grid where Stage 5 ("5. PR Review Gate: Stacked PRs (<150 LOC) & IDE Pre-Push Audit") has the boldest border as the primary bottleneck gate. Avoid condensed type, tiny captions, broad grey backgrounds, heavy outlines, gradients, 3D, glows, textures, mascots, robots, or brains.

ICONS (PRIVATE):
One small simple line icon beside each stage header: code brackets on Stage 1, terminal-bug icon on Stage 2, blueprint compass on Stage 3, kanban-check icon on Stage 4, person-and-check badge on Stage 5, and shield-rocket icon on Stage 6. No invented brand logos.

SPATIAL LAYOUT AND EXACT LABELS (PRIVATE):
Arrange six stage cards in two horizontal rows of three cards each (Top Row: Stages 1, 2, 3 left to right; Bottom Row: Stages 4, 5, 6 left to right), plus a compact legend strip at the bottom outside the main boundary.

Top Row (Stages 1 to 3, left to right):
- Stage 1 Card (blue #2563EB accent, #EFF6FF fill): "1. Coding: Block Clones & Silent Catch"
  - Trap line: "Trap: -70% refactoring, +81% clones, +47% error masking"
  - Gate 1: "CI Gate: jscpd --baseline-from-ref main --fail-on-new-clones"
  - Gate 2: "Subagent: debloat & silent-failure-hunter before commit"
- Stage 2 Card (violet #7C3AED accent, #F5F3FF fill): "2. Debug & Test: Mutation & Read-Only Bundles"
  - Trap line: "Trap: No mental map, +54% bugs, <60% test mutation score"
  - Gate 1: "Debug: Read-only K8s/SQL facts separated from hypotheses"
  - Gate 2: "Testing: Stryker / mutmut mutation check + Revert Test"
- Stage 3 Card (teal #0F766E accent, #F0FDFA fill): "3. System Design: 1-Page RFC & <details>"
  - Trap line: "Trap: 1h 56m lost per 10-page workslop doc, +13.8% restarts"
  - Gate 1: "Skill: one-page-rfc (<=350 words, Non-Goals, Trade-off table)"
  - Gate 2: "Format: Fold raw SQL/schemas inside <details> appendix"

Bottom Row (Stages 4 to 6, left to right):
- Stage 4 Card (slate #475569 accent, #F8FAFC fill): "4. Planning: WIP = 1 & Completion Evidence"
  - Trap line: "Trap: Ticket inflation, +67.4% PR contexts, +26% stalled work"
  - Gate 1: "Kanban Rule: WIP = 1 active task per agent thread"
  - Gate 2: "Done Gate: Executable curl / SQL / test command required"
- Stage 5 Focal Card (amber #B45309 accent, #FFFBEB fill, bold 4px border, person-and-check mark): "5. PR Review: Stacked PRs (<150 LOC) & Shift-Left"
  - Trap line: "Trap: 2x PRs, +154% diff size, 5.3x wait, <30% bot signal"
  - Gate 1: "Decompose: 2 to 3 Stacked PRs (<150 LOC via gh stack / Graphite)"
  - Gate 2: "Shift Left: Local IDE pre-push-review (>=80 confidence only)"
- Stage 6 Card (indigo #4F46E5 accent, #EEF2FF fill): "6. CI/CD & Ops: Scoped Merge Queues & Canaries"
  - Trap line: "Trap: 4x to 10x agent merge surge, +242.7% prod incidents/PR"
  - Gate 1: "CI Queue: Batched & monorepo-scoped queues (Trunk / Mergify)"
  - Gate 2: "Deploy: Feature flags + 5%->25%->100% auto-rollback canary"

VISUAL CONNECTIONS (PRIVATE):
Draw five solid indigo #4F46E5 arrows connecting the six stages in sequence:
1. Stage 1 -> Stage 2 (horizontal)
2. Stage 2 -> Stage 3 (horizontal)
3. Stage 3 -> Stage 4 (clean orthogonal step from top-right down to bottom-left)
4. Stage 4 -> Stage 5 (horizontal)
5. Stage 5 -> Stage 6 (horizontal)
Total connector count: 5.

LEGEND (VISIBLE):
Place a compact legend strip at the bottom outside the main boundary with three colour swatches, each label once:
- Blue #2563EB / Violet #7C3AED / Teal #0F766E: "Upstream code, test & spec quality gates (Stages 1 to 3)"
- Amber #B45309 (with person-and-check mark): "Small-batch stacked PR & shift-left review gate (Stage 5)"
- Indigo #4F46E5: "High-throughput merge queue & progressive delivery safety net (Stage 6)"

FINAL CHECK (PRIVATE, DO NOT PRINT):
Six stage cards in a 2x3 grid, five sequential arrows connecting 1->2->3->4->5->6, three legend items each once. No printed layout words, no title above the canvas.
```

---

## Part B: LinkedIn Carousel Portrait Diagrams (`3:4` / `4:5` Portrait, `1792 × 2400`)

Set **Aspect Ratio to `3:4` (or `4:5`) Portrait** and **Resolution to `2K` (`1792 × 2400`)** in Google AI Studio / Vertex AI Studio when generating these four diagrams. Save them into `docs/diagrams/` under the exact filenames below so Claude Design can place them directly onto Pages 3, 5, 11, and 12 of the PDF carousel.

---

## Portrait Diagram 1 (`li-01-sprint-tug-of-war.jpg`): The 80-Hour Sprint Tug-of-War (For Carousel Page 3)

**What it shows:** A phone-readable `3:4` portrait visual replacing the dense 35-cell spreadsheet table on **Page 3** of the LinkedIn carousel. Top section shows the three 80-hour sprint summary bars (`80.0 h` Pre-AI, `44.5 h` Initial AI Speedup saving `35.5 h`, and `80.0 h` Real AI Sprint after the `+35.5 h` rebound). Bottom section shows the six stages as clean paired tug-of-war rows (`Saved` on the left, `Stage Net` in the center, `Added Rebound` on the right).

### Prompt to Paste into Nano Banana Pro (Set Aspect Ratio: `3:4` Portrait, Resolution: `2K`)

```text
Create a compact professional comparison diagram for a phone-viewed technical carousel. Pure white canvas, 3:4 portrait at 1792 x 2400 resolution. No standalone title, headline, subtitle or empty title band. Begin directly with the top summary panel. All instructions below are private; print only the quoted labels and captions.

VISUAL STYLE (PRIVATE):
Pure white canvas #FFFFFF with near-white group panels #F8FAFC, crisp Inter-like sans-serif typography, semibold #0F172A card titles around 48 px, regular #475569 captions at least 38 px, fine 3px borders, uniform 12px rounded corners, and generous vertical spacing. Use pale fills with saturated colour only on left accent bars, outlines, and small icons: blue #2563EB on #EFF6FF for initial AI savings; indigo #4F46E5 on #EEF2FF for net stage badges; amber #B45309 on #FFFBEB for human review and document cleanup tax; red #B91C1C on #FFF1F2 for bugs, clones, and incidents. No shadows, gradients, 3D effects, mascots, robots, or brains.

ICONS (PRIVATE):
One simple 44 px outline icon per card: clock icon on the three top bars, lightning bolt on left speedup cards, and warning or person-and-check mark on right rebound cards.

SPATIAL LAYOUT AND EXACT LABELS (PRIVATE):
Arrange the portrait canvas vertically from top to bottom in two clean sections with a compact legend at the very bottom.

Top Section (one rounded panel labelled "Three Realities of a 10 x 8h (80-Hour) Sprint" containing three stacked horizontal progress bars):
- First horizontal bar (slate #475569 outline, full width): "1. Pre-AI Baseline · 80.0 Hours (1.0x)" with caption "24h Coding (30%) + 56h Debug, Design, Plan, Review & Ops (70%)"
- Second horizontal bar (blue #2563EB outline, 56% filled + 44% dashed pale-blue saved slot): "2. Initial AI Speedup · 44.5 Hours (1.80x Paper)" with right dashed slot labelled "-35.5 Hours Saved Across All 6 Stages"
- Third horizontal bar (focal amber #B45309 outline, full width): "3. Real-World AI Sprint · 80.0 Hours (~1.21x Net Tasks)" with caption "+35.5 Hours Rebound from Code Cleanup, Doc Rewrites & 2x PR Queues"

Bottom Section (six stacked horizontal rows showing Stage Tug-of-War, each row having Left Blue Card -> Center Indigo Badge -> Right Amber/Red Card):
- Row 1: Left blue card "-19.0 h Boilerplate" -> Center badge "1. Coding · 8.0 h Net" -> Right red card "+3.0 h Cleanup (+81% clones)"
- Row 2: Left blue card "-5.5 h K8s & SQL Checks" -> Center badge "2. Debug · 14.5 h Net" -> Right red card "+8.0 h AI Bugs (+54% bugs/dev)"
- Row 3: Left blue card "-3.5 h Draft RFCs" -> Center badge "3. Design · 14.0 h Net" -> Right amber card "+5.5 h Workslop (1h 56m/doc)"
- Row 4: Left blue card "-3.5 h Notes & Slides" -> Center badge "4. Planning · 12.0 h Net" -> Right amber card "+3.5 h Parallel WIP (+67% PRs)"
- Row 5 (Focal Row, bold border): Left blue card "-2.0 h Lint Bots" -> Center badge "5. PR Review · 18.5 h Net" -> Right focal amber card "+10.5 h Queue (2x PRs, 5.3x wait)"
- Row 6: Left blue card "-2.0 h CI & Helm YAML" -> Center badge "6. CI/CD Ops · 13.0 h Net" -> Right red card "+5.0 h Incidents (+242%/PR)"

VISUAL CONNECTIONS (PRIVATE):
1. In the Top Section, draw one solid amber #B45309 vertical arrow from "-35.5 Hours Saved Across All 6 Stages" down into "3. Real-World AI Sprint · 80.0 Hours (~1.21x Net Tasks)" labelled "Saved hours absorbed downstream".
2. In each of the six Bottom Section rows, draw one short blue #2563EB arrow from the left card to the center badge, and one short amber #B45309 arrow from the center badge to the right card (12 short arrows). Total connector count: 13.

LEGEND (VISIBLE):
Bottom compact white box with three swatches, each label once:
- Blue #2563EB: "Initial AI time saved (-35.5 h total)"
- Indigo #4F46E5: "Net stage hours in real 80h sprint"
- Amber #B45309 / Red #B91C1C: "Cleanup, bug & review rebound (+35.5 h total)"

FINAL CHECK (PRIVATE, DO NOT PRINT):
Portrait 3:4 layout. Top panel has 3 horizontal bars; bottom section has 6 aligned 3-card rows; 13 arrows total; 3 legend items. Do not print "Row 1", "Row 2", "Top Section", or "Bottom Section". All text large and readable on a phone screen.
```

---

## Portrait Diagram 2 (`li-02-bloat-and-mental-map.jpg`): From Write-Only Code Bloat to the Debugging Mental-Map Penalty (For Carousel Page 5)

**What it shows:** A `3:4` portrait two-stage vertical flow diagram for **Page 5** of the LinkedIn carousel showing how **Stage 1 AI "Write-Only" Code Bloat** (`-70%` refactoring, `+81%` clones, `+47%` error-masking guards) flows directly into **Stage 2 Debugging & Testing**, where `-5.5 h` of fast `kubectl`/SQL agent log gathering is outweighed by `+8.0 h` of Missing-Mental-Map debugging, confident false theories, and flawed AI unit tests (`12.0 h → 14.5 h` net).

### Prompt to Paste into Nano Banana Pro (Set Aspect Ratio: `3:4` Portrait, Resolution: `2K`)

```text
Create a vertical two-tier technical cause-and-effect diagram for a phone-viewed carousel. Pure white canvas, 3:4 portrait at 1792 x 2400 resolution. No standalone title, headline, subtitle or empty title band. Begin directly with the Top Tier panel. All instructions below are private; print only the quoted labels and captions.

VISUAL STYLE (PRIVATE):
Pure white canvas #FFFFFF, crisp Inter-like sans-serif typography, semibold #0F172A card names around 48 px, regular #475569 captions at least 38 px, solid 3px borders, 12px rounded corners, and generous spacing. Use blue #2563EB on #EFF6FF and violet #7C3AED on #F5F3FF for AI speedups; amber #B45309 on #FFFBEB for false theories and error masking; red #B91C1C on #FFF1F2 for code bloat and mental-map rework; indigo #4F46E5 on #EEF2FF for the bottom net math bar. No shadows, gradients, 3D effects, robots, or brains.

ICONS (PRIVATE):
One simple 44 px outline icon per card: code brackets, copy-paste files, warning shield, terminal prompt, compass question mark, and check-x test icon.

SPATIAL LAYOUT AND EXACT LABELS (PRIVATE):
Arrange the portrait canvas from top to bottom across two main tiers connected by a central downward arrow, plus a bottom net math bar and compact legend.

Top Tier Panel (red #B91C1C outline, #FFF1F2 pale background) labelled "Upstream Cause: AI 'Write-Only' Code Bloat (GitClear & LinearB Studies)":
Inside the top panel, arrange two equal columns side by side:
- Left card (blue #2563EB accent, white fill): "Human Refactoring Mode" with three short lines:
  "Consolidates shared logic"
  "P75 Refactor Rate: 0.37"
  "Compact diffs (~157 LOC)"
- Right card (red #B91C1C accent, white fill, bold border): "AI Additive Bloat Mode" with three short lines:
  "-70% refactoring · +81% clones"
  "+47% error-masking guards"
  "Bloated diffs (293 to 408 LOC)"

Center Transition (between Top Tier and Bottom Tier):
One prominent solid red #B91C1C downward arrow from "AI Additive Bloat Mode" into the Bottom Tier, labelled "Unfamiliar, error-masked code hits staging & production".

Bottom Tier Panel (slate #334155 outline, #F8FAFC background) labelled "Downstream Effect: Stage 2 Debugging & Testing (12.0 h -> 14.5 h Net)":
Inside the bottom panel, stack three paired horizontal rows (Left Violet/Blue Speedup Card -> Right Red/Amber Rebound Card):
- Pair 1: Left violet #7C3AED card "K8s & Pod Agent (-2.5 h)" with caption "kubectl logs, exec & port-forward" -> Right focal red #B91C1C card "Missing-Mental-Map Penalty (+3.5 h)" with caption "Must reverse-engineer unfamiliar AI code live"
- Pair 2: Left blue #2563EB card "Postgres SQL Agent (-1.5 h)" with caption "Runs diagnostic SQL & CI log checks" -> Right amber #B45309 card "Confident False Theories (+2.5 h)" with caption "Microsoft 2026: Wrong root-cause stories"
- Pair 3: Left teal #0F766E card "AI Test Generator (-1.5 h)" with caption "Generates unit test files" -> Right red #B91C1C card "Flawed AI Tests (+2.0 h)" with caption "Tests pass on buggy code · +54% bugs/dev"

Bottom Net Balance Card (indigo #4F46E5 accent, #EEF2FF fill):
"Stage 2 Net Math: 12.0 h Pre-AI  -  5.5 h Agent Checks  +  8.0 h Bug Rework  =  14.5 Hours (+2.5 h)"

VISUAL CONNECTIONS (PRIVATE):
1. One solid red #B91C1C vertical arrow from the Top Tier ("AI Additive Bloat Mode") to the Bottom Tier.
2. Three horizontal dashed steel-blue #0369A1 arrows inside the Bottom Tier connecting each Left card to its Right card. Total connector count: 4.

LEGEND (VISIBLE):
Bottom compact white box with three swatches, each label once:
- Violet #7C3AED / Blue #2563EB: "Automated K8s, SQL & test speedup (-5.5 h)"
- Amber #B45309: "Error-masking guards & false root causes"
- Red #B91C1C: "Write-only bloat & mental-map penalty (+8.0 h)"

FINAL CHECK (PRIVATE, DO NOT PRINT):
Portrait 3:4 layout. Top panel has 2 cards; 1 vertical arrow between tiers; bottom panel has 3 paired rows (6 cards) with 3 horizontal dashed arrows; 1 bottom net math bar; 3 legend items. Do not print "Pair 1", "Pair 2", "Pair 3", "Top Tier", or "Bottom Tier".
```

---

## Portrait Diagram 3 (`li-03-verification-funnel.jpg`): The Review Funnel & 5 Engineering Guardrails (For Carousel Page 11)

**What it shows:** A `3:4` portrait top-to-bottom architecture diagram for **Page 11 (The Playbook)** of the LinkedIn carousel. Top shows the 4 full-lifecycle AI generators (`-35.5 h` saved) funneling into the central **Human Review & Verification Gate**, then splitting at the bottom into **Left: Undisciplined Slop Flood (`+35.5 h` lost)** versus **Right: The 5 Engineering Guardrails (Keeps AI speedup)**.

### Prompt to Paste into Nano Banana Pro (Set Aspect Ratio: `3:4` Portrait, Resolution: `2K`)

```text
Create a top-to-bottom vertical flow diagram of the AI software delivery funnel and engineering guardrails for a phone-viewed carousel. Pure white canvas, 3:4 portrait at 1792 x 2400 resolution. No standalone title, headline, subtitle or empty title band. Begin directly with the top generator grid. All instructions below are private; print only the quoted labels and captions.

VISUAL STYLE (PRIVATE):
Pure white canvas #FFFFFF, crisp Inter-like sans-serif typography, semibold #0F172A card titles around 46 px, regular #475569 captions at least 36 px, solid 3px borders, 12px rounded corners, and clean vertical flow. Use blue #2563EB, violet #7C3AED, teal #0F766E, and slate #475569 on pale tints for the top AI generators; amber #B45309 on #FFFBEB for the central Human Review Gate; red #B91C1C on #FFF1F2 for the bottom-left Slop Flood path; indigo #4F46E5 and green #15803D on #F0FDF4 for the bottom-right 5 Guardrails path. No shadows, gradients, 3D effects, robots, or brains.

ICONS (PRIVATE):
One simple 44 px outline icon per card: code brackets, terminal, blueprint document, bot icon, person-and-check mark on the central gate, warning triangle on the left path, and shield-check mark on the right guardrail cards.

SPATIAL LAYOUT AND EXACT LABELS (PRIVATE):
Arrange the portrait canvas from top to bottom across three vertical zones with a compact legend at the bottom.

Top Zone (light panel labelled "1. Full-Lifecycle AI Generation (-35.5 Hours Initially Saved)" containing a 2 x 2 grid of four compact cards):
- Top-left card (blue #2563EB accent): "AI Coding Agents (-19.0 h)" with caption "2x PRs · +154% diff size · +81% clones"
- Top-right card (violet #7C3AED accent): "K8s & SQL Checks (-5.5 h)" with caption "Fast logs · confident false leads"
- Bottom-left card (teal #0F766E accent): "AI RFC & Spec Drafts (-3.5 h)" with caption "10-page docs · generic patterns"
- Bottom-right card (slate #475569 accent): "AI Notes & PR Bots (-7.5 h)" with caption "Auto-tickets · <30% bot signal"

Center Zone (single wide focal card spanning full width):
- Focal Gate Card (amber #B45309 accent, #FFFBEB fill, bold 4px border, person-and-check mark): "2. Human Review & Verification Gate" with caption "The Sprint Bottleneck · Every line of code, spec & SQL fix requires human accountability"

Bottom Zone (two side-by-side vertical outcome columns below the Gate):
- Left Column Panel (red #B91C1C outline, #FFF1F2 fill, 42% width) labelled "Path A: Undisciplined Slop":
  - Red card 1: "+91% to +441% PR Review Wait" with caption "5.3x longer pickup (17.6h)"
  - Red card 2: "1h 56m Lost Per Workslop Doc" with caption "+13.8% task restarts"
  - Red card 3: "+242.7% Prod Incidents / PR" with caption "31% PRs merge unreviewed"
  - Red bottom badge: "All 35.5 Hours Lost (DORA Flat)"

- Right Column Panel (focal indigo #4F46E5 / green #15803D outline, #F0FDF4 pale fill, 58% width) labelled "Path B: The 5 Engineering Guardrails":
  - Guardrail 1 (teal #0F766E bar): "1. 1-Page Human Specs (Zero Raw Workslop)"
  - Guardrail 2 (blue #2563EB bar): "2. Hard PR Cap (<150 LOC) & Code-Reuse Rules"
  - Guardrail 3 (amber #B45309 bar): "3. Shift AI Review Left to IDE (Pre-Push)"
  - Guardrail 4 (violet #7C3AED bar): "4. Read-Only K8s/SQL Summaries + Human Fix"
  - Guardrail 5 (indigo #4F46E5 bar): "5. Track Review Wait, Churn & Incidents/PR"

VISUAL CONNECTIONS (PRIVATE):
1. One solid indigo #4F46E5 arrow from the bottom of the Top Zone ("1. Full-Lifecycle AI Generation (-35.5 Hours Initially Saved)") straight down into "2. Human Review & Verification Gate" labelled "High-volume AI output".
2. One solid red #B91C1C arrow branching from the bottom-left of the Gate down into "Path A: Undisciplined Slop" labelled "No guardrails".
3. One solid green #15803D arrow branching from the bottom-right of the Gate down into "Path B: The 5 Engineering Guardrails" labelled "Bounded delegation".
Total connector count: 3.

LEGEND (VISIBLE):
Bottom compact white box with three swatches, each label once:
- Blue #2563EB / Violet #7C3AED: "Full-lifecycle AI generation (-35.5 h)"
- Amber #B45309 (with person-and-check mark): "Human review & verification bottleneck"
- Red #B91C1C vs Green #15803D: "Rebound path vs 5 engineering guardrails"

FINAL CHECK (PRIVATE, DO NOT PRINT):
Portrait 3:4 layout. Top zone has 4 cards in a 2x2 grid; center has 1 wide gate card; bottom has 2 columns (Left has 3 red cards + 1 badge; Right has 5 guardrail cards); 3 vertical/branching arrows total; 3 legend items. Do not print "Top Zone", "Center Zone", or "Bottom Zone".
```

---

## Portrait Diagram 4 (`li-04-chat-zoom-and-stage-gates.jpg`): Progressive Zoom & The 6-Stage Mitigation Toolkit (For Carousel Page 12)

**What it shows:** A `3:4` portrait visual for **Page 12** of the LinkedIn carousel showing the two halves of the companion **`toolkit/`**: (Top Half) **Stopping In-Chat Workslop** via `CLAUDE.md` / `AGENTS.md` BLUF rules, Isolated Subagents (`mental-map-explorer.md`), and 3-Level Progressive Zoom (`Zoom 1 -> 2 -> 3`); and (Bottom Half) **The 6 Stage-by-Stage Engineering Gates** (`jscpd`, `Stryker` mutation testing, 1-page RFCs, `WIP = 1`, Stacked PRs `<150 LOC`, and batched merge queues + canary flags).

### Prompt to Paste into Nano Banana Pro (Set Aspect Ratio: `3:4` Portrait, Resolution: `2K`)

```text
Create a vertical two-part engineering architecture diagram for a phone-viewed technical carousel. Pure white canvas, 3:4 portrait at 1792 x 2400 resolution. No standalone title, headline, subtitle or empty title band. Begin directly with the Top Panel. All instructions below are private; print only the quoted labels and captions.

VISUAL STYLE (PRIVATE):
Pure white canvas #FFFFFF, crisp Inter-like sans-serif typography, semibold #0F172A card titles around 46 px, regular #475569 captions at least 36 px, solid 3px borders, 12px rounded corners, and clean vertical spacing. Use violet #7C3AED, indigo #4F46E5, and teal #0F766E on pale tints for the Top Panel (In-Chat Progressive Zoom); use blue #2563EB, amber #B45309, and green #15803D on pale tints for the Bottom Panel (6 Stage Gates). No shadows, gradients, 3D effects, robots, or brains.

ICONS (PRIVATE):
One simple 44 px outline icon per card: filter funnel, compass map, layers icon, code brackets, terminal, blueprint, kanban check, person-and-check mark, and shield rocket.

SPATIAL LAYOUT AND EXACT LABELS (PRIVATE):
Arrange the portrait canvas from top to bottom across two rounded group panels connected by one central downward arrow, plus a bottom toolkit badge bar and compact legend.

Top Panel (indigo #4F46E5 outline, #EEF2FF pale tint) labelled "Part 1: Stop In-Chat Workslop (CLAUDE.md · AGENTS.md · GEMINI.md)":
Inside the top panel, stack three horizontal flow cards from top to bottom:
- Card 1 (violet #7C3AED accent, white fill): "1. Isolated Explorer Subagent (mental-map-explorer.md)" with caption "Searches 15+ files & K8s/SQL logs in isolated context · Returns 15-line brief"
- Card 2 (focal indigo #4F46E5 accent, white fill, bold 4px border): "2. Zoom Level 1: 30-Second Mental Map (Default)" with caption "1-sentence BLUF + 5-node flow diagram + top 3 file:line boundaries · STOPS HERE"
- Card 3 (teal #0F766E accent, white fill): "3. Zoom Levels 2 & 3 (On Request Only)" with caption "State transitions, edge cases & code shown only when developer asks to zoom in"

Bottom Panel (green #15803D outline, #F0FDF4 pale tint) labelled "Part 2: Stage-by-Stage Sprint Gates (Keeps the 35.5 Hours Saved)":
Inside the bottom panel, arrange a 3-row by 2-column grid of six compact stage cards:
- Row 1 Left (blue #2563EB bar): "1. Coding: jscpd + De-Bloat" with caption "Block new clones & silent catch"
- Row 1 Right (violet #7C3AED bar): "2. Debug/Test: Stryker Mutants" with caption "Read-only logs + kill self-passing tests"
- Row 2 Left (teal #0F766E bar): "3. Design: 1-Page RFC Skill" with caption "<=350 words + <details> appendix"
- Row 2 Right (slate #475569 bar): "4. Planning: WIP = 1 Rule" with caption "1 active task + completion command"
- Row 3 Left (amber #B45309 bar, person-and-check mark): "5. Review: Stacked PRs <150 LOC" with caption "gh stack / Graphite + IDE pre-push check"
- Row 3 Right (indigo #4F46E5 bar): "6. CI/Ops: Scoped Merge Queue" with caption "Batched CI + canary auto-rollback"

Bottom Toolkit Bar (slate #334155 outline, #F8FAFC fill):
"Open-Source Toolkit Included: CLAUDE.md · AGENTS.md · GEMINI.md · .cursor/rules · 3 Skills · 2 Subagents"

VISUAL CONNECTIONS (PRIVATE):
1. Inside Top Panel, draw two solid indigo #4F46E5 vertical arrows connecting Card 1 -> Card 2 -> Card 3.
2. Draw one solid green #15803D vertical arrow from Top Panel down to Bottom Panel labelled "Clean mental map feeds disciplined stage gates". Total connector count: 3.

LEGEND (VISIBLE):
Bottom compact white box with three swatches, each label once:
- Violet #7C3AED / Indigo #4F46E5: "In-chat subagent isolation & 3-level Progressive Zoom"
- Amber #B45309: "Stacked PRs (<150 LOC) & shift-left IDE review"
- Green #15803D / Blue #2563EB: "Automated CI clone, mutation & canary gates"

FINAL CHECK (PRIVATE, DO NOT PRINT):
Portrait 3:4 layout. Top panel has 3 stacked cards; 1 vertical arrow between panels; bottom panel has 6 stage cards in a 3x2 grid; 1 bottom toolkit bar; 3 legend items. Do not print "Row 1 Left" or layout directions.
```
