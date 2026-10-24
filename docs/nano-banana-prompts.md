# Nano Banana Pro Image Generation Prompts: Full-Lifecycle AI Sprint Analysis (Complete 7-Diagram Set for Medium & LinkedIn)

These prompts are written for **Google Nano Banana Pro** (diffusion-based text-to-image model) following the strict 7-section `diagram` specification. Every prompt outputs a **16:9 high-resolution landscape raster image** using one unified colour palette and exact numbers from the **80-hour (`10 × 8h`) two-week sprint analysis** and published 2025 to 2026 telemetry (**Faros AI**, **LinearB**, **GitClear**, **Stanford/HBR**, **MSR '26**, **Microsoft Research**, **METR**, **Atlassian**, and **DORA**).

---

## Shared Palette Across All 7 Diagrams

| Role / Sprint Stage | Accent Hex | Card Fill Hex | Meaning |
|---|---|---|---|
| **Orchestration / Net Math / Primary Frame** | Indigo `#4F46E5` | `#EEF2FF` | Sprint totals, net velocity, primary flow |
| **Stage 1: Hands-on Coding & Gross Speedup** | Blue `#2563EB` | `#EFF6FF` | Code generation, gross hours saved by AI |
| **Stage 2: Debugging, K8s/DB Triage & Tests** | Violet `#7C3AED` | `#F5F3FF` | `kubectl`, pod logs, SQL queries, test suites |
| **Stage 3: System Design & Architecture RFCs** | Teal `#0F766E` | `#F0FDFA` | Architecture design docs, schemas, specs |
| **Stage 4 & 6: Planning, Meetings, CI/CD & Ops** | Slate `#475569` | `#F8FAFC` | Ceremonies, slide decks, CI pipelines, deploys |
| **Stage 5: PR Review Gate & Workslop Tax** | Amber `#B45309` | `#FFFBEB` | Human review bottleneck, doc/bot workslop |
| **Over-Engineering, Bugs & Prod Incidents** | Red `#B91C1C` | `#FFF1F2` | Duplicate code (`+81%`), bugs (`+54%`), incidents (`+242.7%`) |

---

## Diagram Index (Mapped to Medium Article Sections)

| File Name | Diagram Title | Medium Article Section | Primary Data Sources |
|---|---|---|---|
| `01-three-sprint-realities.jpg` | The Three Realities of an 80-Hour Full-Stack AI Sprint | Opening & Section 3 (The 80-Hour Model) | Faros AI (2025/2026), Atlassian (2025), Microsoft Research (2024/2026) |
| `02-pipeline-bottleneck-analogy.jpg` | Distributed Microservice Pipeline vs. AI Sprint Bottleneck | Section 1 (The Pipeline Bottleneck Rule) | Goldratt Theory of Constraints, Faros AI (`+98%` PRs, `+154%` size) |
| `03-stage-by-stage-tug-of-war.jpg` | Stage-by-Stage Tug-of-War (`-35.5 h` Saved vs. `+35.5 h` Rebound) | Section 3 (Gross Speedup vs. Slop Tax) | All 6 Sprint Stages Combined |
| `04-write-only-code-bloat.jpg` | Human Refactoring vs. AI "Write-Only" Code Bloat | Section 4.1 (Stage 1: Hands-On Coding) | GitClear (2026, 623M LOC), LinearB (2026, 8.1M PRs) |
| `05-debugging-mental-map-gap.jpg` | K8s/SQL Agent Triage vs. The Mental Map & Hallucination Tax | Section 4.2 (Stage 2: Debugging & Testing) | Microsoft Research & OSU (2026, `n=860`), Faros AI (`+54%` bugs/dev) |
| `06-workslop-and-review-bot-noise.jpg` | The "Workslop" Transfer Tax & Code Review Bot Noise | Sections 4.3 to 4.5 (Design, Docs & PR Review) | Stanford/BetterUp HBR (2025), MSR '26 (`3,109` PRs), Cihan et al. (`4,335` PRs), LinearB |
| `07-verification-funnel-guardrails.jpg` | The Full-Stack AI Verification Funnel & Engineering Playbook | Section 6 (Bounded Delegation Playbook) | DORA (2025), Microsoft Research (2026), GitClear (2026) |

---

## Diagram 1 (`01-three-sprint-realities.jpg`): The Three Realities of an 80-Hour Full-Stack AI Sprint

**What it shows:** A three-swimlane horizontal comparison of a 2-week sprint (`10 days × 8 hours = 80.0 hours`): (1) Pre-AI Baseline (`80.0 h`), (2) Gross AI Speedup when AI is used across all 6 stages (`44.5 h`, saving `35.5 h`), and (3) Real-World AI Sprint after the Over-Engineering, Workslop, and Review Rebound refills the sprint (`80.0 h`, `~1.21x` net task velocity).

### Prompt to Paste into Nano Banana Pro

```text
Create a comparison diagram of a two-week software engineering sprint (10 days x 8 hours = 80.0 hours) across three horizontal swimlanes: Pre-AI Baseline, Gross AI Speedup Across All 6 Stages, and Real-World AI Sprint After Slop and Verification Tax. Output a high-resolution 16:9 landscape raster image. All directions below are private; print only the quoted labels and captions. No extra title, layout terminology or invented text.

VISUAL STYLE (PRIVATE):
White canvas, near-white group panels, crisp sans-serif such as Inter, dark slate text #0F172A with secondary #475569, fine 3px borders, consistent rounded corners, generous whitespace. Very pale tinted fills on cards and proportional horizontal timeline segments with saturated colour only on small icons, left accent bars and outlines; never a whole layer in saturated colour. The focal point is Swimlane 3 ("3. Real-World AI Sprint · 80.0 h") and its expanded amber PR Review block ("PR Review · 18.5 h (+85%)"), which has the strongest border and largest name; everything else is quieter. Avoid condensed type, tiny captions, broad grey backgrounds, heavy outlines, gradients, 3D, glows, textures, mascots, robots, or brains.

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

Swimlane 2 (middle): Left header card "2. Gross AI Speedup (All 6 Stages)" with caption "Before rework & slop tax". To its right, a horizontal stacked bar spanning 44.5 of 80 hours, followed by a dashed pale-blue empty slot on the right labelled "35.5 Hours Gross Saved by AI (-44%)":
- Blue #2563EB accent (#EFF6FF fill): "Coding · 5.0 h" with caption "-19.0 h saved"
- Violet #7C3AED accent (#F5F3FF fill): "K8s/SQL Agent Debug · 6.5 h" with caption "-5.5 h saved"
- Teal #0F766E accent (#F0FDFA fill): "AI Draft RFCs · 8.5 h" with caption "-3.5 h saved"
- Slate #475569 accent (#F8FAFC fill): "AI Notes & Slides · 8.5 h" with caption "-3.5 h saved"
- Amber #B45309 accent (#FFFBEB fill): "AI Review Bots · 8.0 h" with caption "-2.0 h saved"
- Slate #475569 accent (#F8FAFC fill): "AI CI/YAML · 8.0 h" with caption "-2.0 h saved"
Right summary card for Swimlane 2 (indigo #4F46E5 accent): "44.5 Hours · 1.80x Paper Speedup".

Swimlane 3 (bottom, focal point): Left header card "3. Real-World AI Sprint (Net Telemetry)" with caption "+35.5 h Slop, Cleanup & Review Rebound". To its right, a full-width horizontal stacked bar spanning all 80.0 hours:
- Blue #2563EB accent (#EFF6FF fill): "Coding + De-Bloat · 8.0 h" with caption "+3.0 h fixing +81% clones"
- Red #B91C1C accent (#FFF1F2 fill): "Debug AI Bugs · 14.5 h" with caption "+8.0 h (+54% bugs/dev)"
- Teal #0F766E accent (#F0FDFA fill): "Decode RFC Slop · 14.0 h" with caption "+5.5 h (1h56m/doc tax)"
- Slate #475569 accent (#F8FAFC fill): "Planning & WIP · 12.0 h" with caption "+3.5 h (+67% PR contexts)"
- Focal Amber #B45309 accent (#FFFBEB fill, bold border, person-and-check mark): "PR Review · 18.5 h (+85%)" with caption "+10.5 h (2x PRs, 5.3x wait)"
- Red #B91C1C accent (#FFF1F2 fill): "CI & Prod Incidents · 13.0 h" with caption "+5.0 h (+242% incidents/PR)"
Right summary card for Swimlane 3 (amber #B45309 accent): "80.0 Hours · ~1.21x Net Tasks".

VISUAL CONNECTIONS (PRIVATE):
Use medium solid indigo #4F46E5 arrows and solid amber #B45309 arrows. Draw exactly two vertical arrows between Swimlane 2 and Swimlane 3:
1. One solid indigo #4F46E5 arrow from "Coding · 5.0 h" in Swimlane 2 down to "Coding + De-Bloat · 8.0 h" in Swimlane 3 labelled "+3.0 h over-engineering cleanup".
2. One solid amber #B45309 arrow from the dashed slot "35.5 Hours Gross Saved by AI (-44%)" in Swimlane 2 down into the expanded right half of Swimlane 3 ("PR Review · 18.5 h (+85%)") labelled "+35.5 h absorbed by verification, workslop & review queues".
No other connectors. Summary cards and legend items have no connectors. Total connector count: 2.

LEGEND (VISIBLE):
Place a compact horizontal legend strip at the bottom outside the main boundary with five colour swatches, each label once:
- Blue #2563EB: "Hands-on coding & gross AI savings"
- Violet #7C3AED: "Agent K8s/DB debugging & test generation"
- Teal #0F766E: "System design & RFC specifications"
- Amber #B45309 (with person-and-check mark): "Human PR review & workslop verification gate"
- Red #B91C1C: "Rework from code bloat, AI bugs & production incidents"

FINAL CHECK (PRIVATE, DO NOT PRINT):
Exactly three horizontal sprint swimlanes, six segments per bar, three summary cards on the right, two vertical arrows total, five legend items each once. No printed layout words, no percentages used as layout coordinates, no title above the canvas.
```

---

## Diagram 2 (`02-pipeline-bottleneck-analogy.jpg`): Distributed Microservice Pipeline vs. AI Sprint Bottleneck

**What it shows:** A two-panel comparison illustrating the **Pipeline Bottleneck Rule (Theory of Constraints)** for software engineers. Panel 1 shows a `1,000 ms` API endpoint where making compute `10×` faster (`300 ms → 30 ms`) only achieves `730 ms` (`1.37×`) on paper, and climbs back to `1,000 ms` when `2×` traffic and `2.5×` bloated payloads saturate database locks and deserialization. Panel 2 shows the exact parallel in an `80-hour` engineering sprint.

### Prompt to Paste into Nano Banana Pro

```text
Create a two-panel horizontal comparison diagram contrasting a 1,000 ms distributed API request pipeline (top panel) with an 80-hour software engineering sprint pipeline (bottom panel) under 10x upstream acceleration and payload bloat. Output a high-resolution 16:9 landscape raster image. All directions below are private; print only the quoted labels and captions. No extra title, layout terminology or invented text.

VISUAL STYLE (PRIVATE):
White canvas, near-white group panels, crisp sans-serif such as Inter, dark slate text #0F172A with secondary #475569, fine 3px borders, consistent rounded corners, generous whitespace. Very pale tinted fills on cards with saturated colour only on small icons, left accent bars and outlines. The focal point is the bottom-right amber/red bottleneck card ("Human Verification & PR Review Queue · Saturates back to 80.0 h"), which has the strongest border and largest title. Avoid condensed type, tiny captions, broad grey backgrounds, heavy outlines, gradients, 3D, glows, textures, mascots, robots, or brains.

ICONS (PRIVATE):
One small simple line icon beside each card name: a server-cpu icon on App Compute, a database-lock icon on DB & Deserialization, a code-brackets icon on AI Generation, and a person-and-check badge on Human Verification & PR Review Queue. No invented brand logos.

SPATIAL LAYOUT AND EXACT LABELS (PRIVATE):
Arrange the canvas into two large horizontal group panels stacked top and bottom across most of the canvas, with a legend strip at the bottom outside the main boundary.

Top Group Panel labelled "1. Distributed Systems Analogy: A 1,000 ms API Endpoint":
Inside the top panel, place three horizontal flow cards from left to right:
- Card A1 (blue #2563EB accent, #EFF6FF fill): "Baseline API · 1,000 ms" with caption "300 ms App Compute + 700 ms DB Locks & Network I/O"
- Card A2 (indigo #4F46E5 accent, #EEF2FF fill): "Paper 10x Compute · 730 ms (1.37x)" with caption "App Code rewritten in Rust (300 ms -> 30 ms) · DB still takes 700 ms"
- Card A3 (red #B91C1C accent, #FFF1F2 fill): "With 2x Traffic & 2.5x Payload Bloat · 1,000 ms" with caption "DB connection pool & JSON deserialization saturate · Gain erased"

Bottom Group Panel labelled "2. Software Delivery Reality: An 80.0-Hour Two-Week Sprint":
Inside the bottom panel, place three horizontal flow cards from left to right aligned directly below Cards A1, A2, and A3:
- Card B1 (blue #2563EB accent, #EFF6FF fill): "Baseline Sprint · 80.0 Hours" with caption "24.0 h Hands-On Coding (30%) + 56.0 h Design, Review, Test & Ops (70%)"
- Card B2 (indigo #4F46E5 accent, #EEF2FF fill): "Gross Full-Stack AI · 44.5 Hours (1.80x)" with caption "-35.5 h saved across Coding, K8s/SQL Triage, RFCs, Notes & Bots"
- Focal Card B3 (amber #B45309 accent, #FFFBEB fill, bold border, person-and-check mark): "Human Verification & PR Review Queue · 80.0 Hours" with caption "+98% PRs, +154% PR size, +81% clones & 1h56m doc slop eat all +35.5 h"

VISUAL CONNECTIONS (PRIVATE):
Use medium solid indigo #4F46E5 arrows and solid red #B91C1C arrows:
1. In the Top Panel, one solid indigo #4F46E5 arrow from Card A1 to Card A2 labelled "10x faster compute", and one solid red #B91C1C arrow from Card A2 to Card A3 labelled "2x requests + 2.5x payload".
2. In the Bottom Panel, one solid indigo #4F46E5 arrow from Card B1 to Card B2 labelled "AI across all 6 stages (-35.5 h)", and one solid red #B91C1C arrow from Card B2 to Focal Card B3 labelled "Slop & verification rebound (+35.5 h)".
No vertical arrows crossing between panels. Total connector count: 4.

LEGEND (VISIBLE):
Place a compact legend strip at the bottom outside the main boundary with three colour swatches, each label once:
- Blue #2563EB: "Baseline workload (30% compute / 30% coding)"
- Indigo #4F46E5: "Isolated upstream speedup before queue contention"
- Amber #B45309 / Red #B91C1C: "Downstream bottleneck saturation from volume & payload bloat"

FINAL CHECK (PRIVATE, DO NOT PRINT):
Exactly two horizontal group panels, three cards per panel (six cards total), four horizontal arrows total, three legend items each once. No printed layout words, no title above the canvas.
```

---

## Diagram 3 (`03-stage-by-stage-tug-of-war.jpg`): Stage-by-Stage Tug-of-War (`-35.5 h` Saved vs. `+35.5 h` Rebound)

**What it shows:** A two-column diverging/paired breakdown across all six sprint stages showing **what AI speeds up on the left (`-35.5 h` total)** versus **what AI slows down via slop, over-engineering, and review load on the right (`+35.5 h` total)**.

### Prompt to Paste into Nano Banana Pro

```text
Create a comparison diagram of the six software sprint stages showing Gross AI Time Saved on the left versus Slop, Over-Engineering, and Verification Hours Added on the right across an 80-hour two-week sprint. Output a high-resolution 16:9 landscape raster image. All directions below are private; print only the quoted labels and captions. No extra title, layout terminology or invented text.

VISUAL STYLE (PRIVATE):
White canvas, near-white group panels, crisp sans-serif such as Inter, dark slate text #0F172A with secondary #475569, fine 3px borders, consistent rounded corners, generous whitespace. Very pale tinted fills on cards with saturated colour only on small icons, left accent bars and outlines. The focal point is Row 5 on the right ("PR Review Queue & Bot Noise · +10.5 h Added"), which has the strongest amber border and largest title. Avoid condensed type, tiny captions, broad grey backgrounds, heavy outlines, gradients, 3D, glows, textures, mascots, robots, or brains.

ICONS (PRIVATE):
One small simple line icon beside each card title, same size and stroke throughout: a lightning bolt on left-column speedup cards, a warning-magnifier or person-and-check mark on right-column verification tax cards. No invented brand logos.

SPATIAL LAYOUT AND EXACT LABELS (PRIVATE):
Arrange the canvas into two equal columns ("Left Column: Gross AI Speedup · -35.5 h Saved" in blue #2563EB and "Right Column: Slop & Verification Rebound · +35.5 h Added" in amber #B45309) separated by a narrow central spine of six stage badges, with six horizontal rows aligned across both columns and a bottom totals bar.

Row 1 (Hands-On Coding):
- Left blue #2563EB card (#EFF6FF fill): "Boilerplate & Feature Generation · -19.0 h" with caption "24.0 h -> 5.0 h raw coding time"
- Center slate badge: "1. Coding (Net: 8.0 h)"
- Right red #B91C1C card (#FFF1F2 fill): "Over-Engineered Code & Clones · +3.0 h" with caption "GitClear: -70% refactoring, +81% duplication"

Row 2 (Debugging, K8s/DB & Tests):
- Left violet #7C3AED card (#F5F3FF fill): "kubectl, Pod Logs, SQL & Test Drafts · -5.5 h" with caption "12.0 h -> 6.5 h raw triage time"
- Center slate badge: "2. Debug & Test (Net: 14.5 h)"
- Right red #B91C1C card (#FFF1F2 fill): "Unfamiliar AI Bugs & False Leads · +8.0 h" with caption "Faros: +54% bugs/dev · confident hallucinations"

Row 3 (System Design & RFCs):
- Left teal #0F766E card (#F0FDFA fill): "Instant Architecture & RFC Drafts · -3.5 h" with caption "12.0 h -> 8.5 h initial drafting"
- Center slate badge: "3. Design (Net: 14.0 h)"
- Right amber #B45309 card (#FFFBEB fill): "Decoding Design Workslop · +5.5 h" with caption "Stanford/HBR: 1h 56m lost per workslop doc"

Row 4 (Planning, Meetings & Slides):
- Left blue #2563EB card (#EFF6FF fill): "AI Meeting Minutes, Slides & Tickets · -3.5 h" with caption "12.0 h -> 8.5 h note taking"
- Center slate badge: "4. Planning (Net: 12.0 h)"
- Right amber #B45309 card (#FFFBEB fill): "Ticket Inflation & +67% Parallel WIP · +3.5 h" with caption "Faros: +26% stalled tasks (>7 days idle)"

Row 5 (PR Code Review, Focal Row):
- Left blue #2563EB card (#EFF6FF fill): "AI Review Bots (Lint & Syntax) · -2.0 h" with caption "10.0 h -> 8.0 h surface checks"
- Center slate badge: "5. PR Review (Net: 18.5 h)"
- Right focal amber #B45309 card (#FFFBEB fill, bold border, person-and-check mark): "PR Review Queue & Bot Noise · +10.5 h" with caption "MSR '26: <30% bot signal · LinearB: 5.3x wait"

Row 6 (CI/CD, Deploy & Prod Ops):
- Left blue #2563EB card (#EFF6FF fill): "Helm/Terraform YAML & CI Log Parse · -2.0 h" with caption "10.0 h -> 8.0 h config authoring"
- Center slate badge: "6. CI/CD & Ops (Net: 13.0 h)"
- Right red #B91C1C card (#FFF1F2 fill): "2x CI Queues & +242% Incidents/PR · +5.0 h" with caption "Faros 2026: 3.4x higher incident rate per PR"

Bottom Summary Strip spanning both columns:
- Left summary card (blue #2563EB accent): "Total Gross AI Speedup: -35.5 Hours (80.0 h -> 44.5 h)"
- Right summary card (amber #B45309 accent): "Total Slop & Verification Tax: +35.5 Hours (44.5 h -> 80.0 h · 1.21x Net Output)"

VISUAL CONNECTIONS (PRIVATE):
In each of the six rows, draw one short solid blue #2563EB arrow from the left card into the center stage badge, and one short solid amber #B45309 arrow from the center stage badge into the right card (12 short horizontal arrows total, 2 per row). No vertical or diagonal arrows between rows. Bottom summary cards and legend items have no connectors. Total connector count: 12.

LEGEND (VISIBLE):
Place a compact legend strip at the bottom outside the main boundary with three colour swatches, each label once:
- Blue #2563EB / Violet #7C3AED / Teal #0F766E: "Gross creation & triage hours saved by AI (-35.5 h)"
- Amber #B45309 (with person-and-check mark): "Human review & workslop verification tax"
- Red #B91C1C: "Code bloat cleanup, bug rework & production incident tax"

FINAL CHECK (PRIVATE, DO NOT PRINT):
Exactly six aligned rows, one left card, one center badge, and one right card per row, two bottom summary cards, 12 short horizontal arrows total, three legend items each once. No printed layout words, no title above the canvas.
```

---

## Diagram 4 (`04-write-only-code-bloat.jpg`): Human Refactoring vs. AI "Write-Only" Code Bloat

**What it shows:** Why Stage 1 (Hands-on Coding) requires `+3.0 h` of de-bloating and creates massive downstream debt: compares **Human-Authored Modular Refactoring** (`0.37` refactor rate, consolidating shared functions) with **AI "Write-Only" Additive Bloat** (`-70%` refactoring collapse, `+81%` duplicated blocks, `+47%` defensive error-masking wrappers, and `-74%` legacy maintenance from GitClear 2026 and LinearB 2026).

### Prompt to Paste into Nano Banana Pro

```text
Create a two-column structural comparison diagram contrasting Human Modular Refactoring (left column) with AI Write-Only Code Bloat and Wrapper Accumulation (right column), backed by GitClear 2026 (623M lines) and LinearB 2026 (8.1M PRs) metrics. Output a high-resolution 16:9 landscape raster image. All directions below are private; print only the quoted labels and captions. No extra title, layout terminology or invented text.

VISUAL STYLE (PRIVATE):
White canvas, near-white group panels, crisp sans-serif such as Inter, dark slate text #0F172A with secondary #475569, fine 3px borders, consistent rounded corners, generous whitespace. Very pale tinted fills on cards with saturated colour only on small icons, left accent bars and outlines. The focal point is the right-hand red panel ("Right: AI Write-Only Mode (Additive Bloat)"), which has the strongest border and largest title. Avoid condensed type, tiny captions, broad grey backgrounds, heavy outlines, gradients, 3D, glows, textures, mascots, robots, or brains.

ICONS (PRIVATE):
One small simple line icon beside each card name: a clean modular-cube icon on the left human cards, a copy-paste clone icon and warning shield on the right AI bloat cards. No invented brand logos.

SPATIAL LAYOUT AND EXACT LABELS (PRIVATE):
Arrange the canvas into two equal side-by-side panels with a bottom telemetry comparison bar and a legend strip outside the bottom boundary.

Left Panel (blue #2563EB outline, #F8FAFC background) labelled "Left: Human Engineering (Refactor & Reuse Mode)":
Inside the left panel, show a clean three-card vertical architecture:
- Top card (blue #2563EB accent, #EFF6FF fill): "1. Understand Existing Module Graph" with caption "Reads cross-file callers & domain invariants before editing"
- Middle card (teal #0F766E accent, #F0FDFA fill): "2. Move & Consolidate Shared Logic" with caption "LinearB P75 Refactor Rate: 0.37 (1.5x to 2.2x higher than AI PRs)"
- Bottom card (indigo #4F46E5 accent, #EEF2FF fill): "3. Compact, Incremental Diff (~157 LOC)" with caption "Single source of truth · Easy for teammates to review & debug"

Right Panel (focal red #B91C1C outline, #FFF1F2 pale tint) labelled "Right: AI Write-Only Mode (Additive Wrapper Bloat)":
Inside the right panel, show four stacked cards illustrating structural erosion:
- Card R1 (red #B91C1C accent, white fill): "1. Loses Cross-File Context (-35% Reuse)" with caption "Avoids touching existing modules · Invents parallel helper files"
- Card R2 (red #B91C1C accent, white fill): "2. Copy-Paste Clones (+81% Block Duplication)" with caption "GitClear 2026: Moved lines collapsed 21% -> 3.8% (-70% refactoring)"
- Card R3 (amber #B45309 accent, #FFFBEB fill): "3. Defensive Error-Masking (+47% Guards)" with caption "Wraps broken state in try/catch, null-checks & fallback mocks"
- Card R4 (red #B91C1C accent, white fill): "4. Bloated PR Diff (293 to 408 LOC at P75)" with caption "-74% legacy maintenance · Requires +3.0 h de-slop cleanup per sprint"

VISUAL CONNECTIONS (PRIVATE):
1. Inside the Left Panel, draw two solid blue #2563EB vertical arrows connecting Top card -> Middle card -> Bottom card.
2. Inside the Right Panel, draw three solid red #B91C1C vertical arrows connecting Card R1 -> Card R2 -> Card R3 -> Card R4.
No arrows between the Left Panel and Right Panel. Total connector count: 5.

LEGEND (VISIBLE):
Place a compact legend strip at the bottom outside the main boundary with three colour swatches, each label once:
- Blue #2563EB / Teal #0F766E: "DRY modular refactoring & cross-file reuse"
- Amber #B45309: "Error-masking wrappers that hide root causes (+47%)"
- Red #B91C1C: "Code duplication (+81%) & collapsed refactoring (-70%)"

FINAL CHECK (PRIVATE, DO NOT PRINT):
Two side-by-side panels, three cards in the left panel, four cards in the right panel, five vertical arrows total, three legend items each once. No printed layout words, no title above the canvas.
```

---

## Diagram 5 (`05-debugging-mental-map-gap.jpg`): K8s/SQL Agent Triage vs. The Mental Map & Hallucination Tax

**What it shows:** The Stage 2 debugging paradox (`12.0 h → 6.5 h gross → 14.5 h net`). Coding agents save `-5.5 hours` by automating `kubectl logs`, `kubectl exec`, port-forwarding, SQL queries, and CI log parsing. However, they add `+8.0 hours` back because engineers lack a **mental map** of AI-written code, chase **confident false root-cause hypotheses** (Microsoft Research 2026), and audit **tautological unit tests** (`+54%` bugs/dev, Faros AI 2026).

### Prompt to Paste into Nano Banana Pro

```text
Create a sequence and workflow diagram of Stage 2 (Debugging, Kubernetes/Database Triage, and Testing in an 80-hour sprint), showing how AI agents save 5.5 hours on evidence collection but add 8.0 hours via the Mental Map Gap, confident false hypotheses, and tautological tests. Output a high-resolution 16:9 landscape raster image. All directions below are private; print only the quoted labels and captions. No extra title, layout terminology or invented text.

VISUAL STYLE (PRIVATE):
White canvas, near-white group panels, crisp sans-serif such as Inter, dark slate text #0F172A with secondary #475569, fine 3px borders, consistent rounded corners, generous whitespace. Very pale tinted fills on cards with saturated colour only on small icons, left accent bars and outlines. The focal point is the right-hand red panel ("Phase 2: The +8.0 h Mental Map & Hallucination Rebound"), which has the strongest border and largest title. Avoid condensed type, tiny captions, broad grey backgrounds, heavy outlines, gradients, 3D, glows, textures, mascots, robots, or brains.

ICONS (PRIVATE):
One small simple line icon beside each card name: a terminal icon on kubectl/Pod Logs, a database cylinder icon on Postgres SQL Triage, a compass-question icon on Mental Map Gap, a warning-alert icon on Confident False Hypothesis, and a check-x icon on Tautological Unit Tests. No invented brand logos.

SPATIAL LAYOUT AND EXACT LABELS (PRIVATE):
Arrange the canvas from left to right across two main phases plus a bottom net-math bar and a legend strip outside the bottom boundary.

Left Panel (violet #7C3AED outline, #F5F3FF pale tint) labelled "Phase 1: Automated Evidence Collection (-5.5 h Saved · 12.0 h -> 6.5 h)":
Inside the left panel, stack three horizontal cards:
- Card L1 (violet #7C3AED accent, white fill): "1. Kubernetes & Pod Triage Agent" with caption "Runs kubectl logs, kubectl exec, port-forward & live API probes"
- Card L2 (blue #2563EB accent, white fill): "2. Database & CI Pipeline Agent" with caption "Connects to PostgreSQL, runs diagnostic SQL & parses CI failure traces"
- Card L3 (teal #0F766E accent, white fill): "3. Automated Test Scaffolder" with caption "Generates unit & integration test boilerplate in seconds"

Right Panel (focal red #B91C1C outline, #FFF1F2 pale tint) labelled "Phase 2: The Comprehension & Rework Rebound (+8.0 h Added · 6.5 h -> 14.5 h)":
Inside the right panel, stack three horizontal cards aligned with Cards L1 to L3:
- Focal Card R1 (red #B91C1C accent, white fill, bold border): "1. The Zero-Mental-Map Penalty (+3.5 h)" with caption "Engineer did not write the code · Must reverse-engineer AI logic during live outage"
- Card R2 (amber #B45309 accent, #FFFBEB fill): "2. Confident Root-Cause Hallucinations (+2.5 h)" with caption "Microsoft Research (2026): Plausible but wrong causal stories waste hours on dead ends"
- Card R3 (red #B91C1C accent, white fill): "3. Tautological Tests & +54% Bugs/Dev (+2.0 h)" with caption "AI tests mock out or assert the buggy behavior itself · Faros 2026: +54% bugs/dev"

Bottom Net Math Card spanning both panels (indigo #4F46E5 accent, #EEF2FF fill):
"Stage 2 Net Balance: 12.0 h Pre-AI  -  5.5 h Agent Triage  +  8.0 h Mental Map & Bug Rework  =  14.5 Hours (+2.5 h Net Increase)"

VISUAL CONNECTIONS (PRIVATE):
Draw three horizontal dashed steel-blue #0369A1 arrows connecting each Left Panel card to its corresponding Right Panel card:
1. Card L1 -> Focal Card R1 labelled "Logs gathered, but code is unfamiliar".
2. Card L2 -> Card R2 labelled "SQL run, but hypothesis is hallucinated".
3. Card L3 -> Card R3 labelled "Tests pass, but assert buggy logic".
Bottom Net Math Card and legend items have no connectors. Total connector count: 3.

LEGEND (VISIBLE):
Place a compact legend strip at the bottom outside the main boundary with three colour swatches, each label once:
- Violet #7C3AED / Blue #2563EB: "Automated CLI, K8s & SQL evidence gathering (-5.5 h)"
- Amber #B45309: "False root-cause leads requiring human verification"
- Red #B91C1C: "Mental map reconstruction & escaped bug rework (+8.0 h)"

FINAL CHECK (PRIVATE, DO NOT PRINT):
Two side-by-side phase panels, three cards per panel, one bottom net math card, three horizontal dashed arrows total, three legend items each once. No printed layout words, no title above the canvas.
```

---

## Diagram 6 (`06-workslop-and-review-bot-noise.jpg`): The "Workslop" Transfer Tax & Code Review Bot Noise

**What it shows:** How AI transfers effort from the **creator** to the **receiver** in Stages 3, 4, and 5:
1. **Top Half (The Workslop Tax in Design & Planning):** Creator saves `20 min` prompting a 10-page RFC or 3-page meeting deck, transferring **1 hour 56 minutes per incident** of decoding/rewriting work to teammates (Stanford/BetterUp HBR 2025, `40%` prevalence) and causing **`+13.8%` task restarts** (Faros 2026).
2. **Bottom Half (The PR Review & Bot Noise Logjam):** Creator pushes `+98%` more PRs (`+154%` larger); AI review bots generate **`<30%` signal on `60.2%` of closed PRs** (MSR ’26) and increase PR closure time by **`+42%` (`5h 52m → 8h 20m`, Cihan et al.)**, while human reviewers stall for **`5.3×` longer pickup wait (`17.6 h` vs `3.3 h`, LinearB 2026)**.

### Prompt to Paste into Nano Banana Pro

```text
Create a two-tier flow diagram illustrating how AI shifts cognitive burden from the sender to the receiver across System Design/Docs (Top Tier: The Workslop Transfer Tax) and Pull Request Code Review (Bottom Tier: Review Bot Noise and Queue Logjam). Output a high-resolution 16:9 landscape raster image. All directions below are private; print only the quoted labels and captions. No extra title, layout terminology or invented text.

VISUAL STYLE (PRIVATE):
White canvas, near-white group panels, crisp sans-serif such as Inter, dark slate text #0F172A with secondary #475569, fine 3px borders, consistent rounded corners, generous whitespace. Very pale tinted fills on cards with saturated colour only on small icons, left accent bars and outlines. The focal point is the bottom-right amber/red card ("Human Reviewer Queue · 18.5 h (+85% Load)"), which has the strongest border and largest title. Avoid condensed type, tiny captions, broad grey backgrounds, heavy outlines, gradients, 3D, glows, textures, mascots, robots, or brains.

ICONS (PRIVATE):
One small simple line icon beside each card name: a file-text icon on AI RFC/Slide Generator, a clock-warning icon on Workslop Receiver Tax, a bot-comment icon on AI Code Review Bot, and a person-and-check badge on Human Reviewer Queue. No invented brand logos.

SPATIAL LAYOUT AND EXACT LABELS (PRIVATE):
Arrange the canvas into two horizontal tiers stacked top and bottom across most of the canvas, with three flow cards per tier (left to right) and a legend strip at the bottom outside the main boundary.

Top Tier Panel labelled "Tier 1: System Design, RFCs & Meeting Docs (The Workslop Transfer Tax)":
- Card T1 (teal #0F766E accent, #F0FDFA fill): "1. Sender Prompts AI (Saves ~20 min)" with caption "Generates 10-page RFC, slide deck or 15 Jira subtasks in one shot"
- Card T2 (amber #B45309 accent, #FFFBEB fill): "2. Polished But Context-Free 'Workslop'" with caption "Stanford/HBR (2025): 40% of workers receive it · Generic patterns, invented assumptions"
- Card T3 (red #B91C1C accent, #FFF1F2 fill): "3. Receiver Pays 1 hr 56 min Per Incident" with caption "Teammates decode & rewrite spec · Faros 2026: +13.8% task restarts (+5.5 h design tax)"

Bottom Tier Panel labelled "Tier 2: Pull Request Review & AI Review Agents (The Verification Logjam)":
- Card B1 (blue #2563EB accent, #EFF6FF fill): "1. Author Pushes +98% More & +154% Larger PRs" with caption "LinearB 2026: P75 diff jumps from 157 LOC (manual) to 293 to 408 LOC (AI)"
- Card B2 (amber #B45309 accent, #FFFBEB fill): "2. AI Code Review Bot Adds Low-Signal Noise" with caption "MSR '26: 12 of 13 bots <60% signal · Cihan et al.: PR closure time +42% (5h52m -> 8h20m)"
- Focal Card B3 (amber #B45309 accent, #FFFBEB fill, bold border, person-and-check mark): "3. Human Reviewer Queue · 18.5 h (+85% Load)" with caption "5.3x longer pickup wait (17.6h vs 3.3h) · <60% AI PR acceptance · 31% merge unreviewed"

VISUAL CONNECTIONS (PRIVATE):
1. In Top Tier, draw two solid amber #B45309 horizontal arrows: Card T1 -> Card T2 labelled "Unedited output", and Card T2 -> Card T3 labelled "Effort shifted downstream".
2. In Bottom Tier, draw two solid red #B91C1C horizontal arrows: Card B1 -> Card B2 labelled "Large diff triggers bot comments", and Card B2 -> Focal Card B3 labelled "Noise + missing context stalls review".
No vertical connectors between tiers. Total connector count: 4.

LEGEND (VISIBLE):
Place a compact legend strip at the bottom outside the main boundary with three colour swatches, each label once:
- Teal #0F766E / Blue #2563EB: "Fast upstream AI artifact creation (Sender)"
- Amber #B45309 (with person-and-check mark): "Workslop & low-signal bot noise (<30% to 60% signal)"
- Red #B91C1C: "Downstream human verification & queue delay (+42% to +441%)"

FINAL CHECK (PRIVATE, DO NOT PRINT):
Exactly two horizontal tiers, three cards per tier (six cards total), four horizontal arrows total, three legend items each once. No printed layout words, no title above the canvas.
```

---

## Diagram 7 (`07-verification-funnel-guardrails.jpg`): The Full-Stack AI Verification Funnel & Engineering Playbook

**What it shows:** A system-architecture style flowchart showing how AI agents across Coding, K8s/SQL Debugging, RFC Design, and Meetings feed into the Human Comprehension & Approval Gate, contrasting **Path A: The Undisciplined Slop Flood** (`+35.5 h` rebound, `+242.7%` incidents/PR) with **Path B: High-Performing Bounded Delegation Guardrails** (`<150 LOC` small batches, pre-commit IDE gates, 1-page verified specs, read-only K8s/SQL bundles).

### Prompt to Paste into Nano Banana Pro

```text
Create a system overview diagram of the software delivery pipeline showing how full-lifecycle AI agents feed into the human verification gate, comparing the undisciplined slop flood against bounded delegation guardrails. Output a high-resolution 16:9 landscape raster image. All directions below are private; print only the quoted labels and captions. No extra title, layout terminology or invented text.

VISUAL STYLE (PRIVATE):
White canvas, near-white group panels, crisp sans-serif such as Inter, dark slate text #0F172A with secondary #475569, fine 3px borders, consistent rounded corners, generous whitespace. Very pale tinted fills on cards with saturated colour only on small icons, left accent bars and outlines. The focal point is the central amber gate card ("Human Comprehension & Verification Gate"), which has the strongest border and largest name. Avoid condensed type, tiny captions, broad grey backgrounds, heavy outlines, gradients, 3D, glows, textures, mascots, robots, or brains.

ICONS (PRIVATE):
One small simple line icon beside each component name: terminal/code icons on the four left AI inputs, a person-and-check badge on the central Human Verification Gate, a warning triangle on the top red failure path, and a check-shield icon on the bottom green/indigo guardrail path. No invented brand logos.

SPATIAL LAYOUT AND EXACT LABELS (PRIVATE):
Arrange the canvas from left to right across three well-spaced zones: Left Zone (Four Full-Lifecycle AI Generators), Center Zone (The Verification Bottleneck Gate), and Right Zone (Two Diverging Delivery Outcomes).

Left Zone (stacked vertically inside a light panel labelled "Full-Lifecycle AI Generation (-35.5 h Gross Saved)"):
- Card 1 (blue #2563EB accent, #EFF6FF fill): "AI Coding Agents" with caption "2x PR volume · +154% larger diffs · +81% clones"
- Card 2 (violet #7C3AED accent, #F5F3FF fill): "K8s, Pod Log & SQL Agents" with caption "Fast evidence · confident root-cause guesses"
- Card 3 (teal #0F766E accent, #F0FDFA fill): "AI RFC & Design Generators" with caption "10-page specs · generic patterns"
- Card 4 (slate #475569 accent, #F8FAFC fill): "AI Meeting Notes & PR Bots" with caption "Auto-tickets · <30% signal bot comments"

Center Zone (single large focal card):
- Focal Card (amber #B45309 accent, #FFFBEB fill, bold 3px border, person-and-check mark): "Human Comprehension & Verification Gate" with caption "The True Sprint Bottleneck · Must verify intent, architecture, edge cases & prod safety"

Right Zone (two stacked outcome panels):
- Top Right Panel (red #B91C1C accent, #FFF1F2 fill): "Path A: Undisciplined AI (The Slop Flood)" with three internal metric badges:
  1. "PR Review Time: +91% to +441%"
  2. "Workslop Tax: 1h 56m lost per doc"
  3. "Prod Incidents/PR: +242.7% · DORA Flat"
- Bottom Right Panel (indigo #4F46E5 accent, #EEF2FF fill): "Path B: High-Performing Guardrails (Bounded Delegation)" with three internal guardrail badges:
  1. "Small Batches (<150 LOC) & Pre-Push AI Check"
  2. "1-Page Human-Verified Specs (Zero Raw Slop)"
  3. "Read-Only K8s/SQL Bundles + Human Patch Sign-Off"

VISUAL CONNECTIONS (PRIVATE):
Use medium solid indigo #4F46E5 arrows, solid red #B91C1C arrows, and solid amber #B45309 arrows:
1. One vertical spine collecting the four Left Zone cards into one solid indigo #4F46E5 arrow entering the left side of "Human Comprehension & Verification Gate" labelled "High-volume AI output".
2. One solid red #B91C1C arrow from the top-right of "Human Comprehension & Verification Gate" to "Path A: Undisciplined AI (The Slop Flood)" labelled "No batch limits or spec filters (+35.5 h rebound)".
3. One solid indigo #4F46E5 arrow from the bottom-right of "Human Comprehension & Verification Gate" to "Path B: High-Performing Guardrails (Bounded Delegation)" labelled "Left-shifted quality gates (Keeps AI speedup)".
No other connectors. Internal badges and legend items have no connectors. Total connector count: 3 (counting the left fan-in spine as 1 combined connector plus 2 outgoing branches).

LEGEND (VISIBLE):
Place a compact legend strip at the bottom outside the main boundary with three colour swatches, each label once:
- Blue #2563EB / Violet #7C3AED / Teal #0F766E: "AI generation & automated evidence gathering"
- Amber #B45309 (with person-and-check mark): "Human verification & accountability gate"
- Red #B91C1C vs Indigo #4F46E5: "Slop rebound path vs Engineered guardrail path"

FINAL CHECK (PRIVATE, DO NOT PRINT):
Four input cards on the left, one focal gate card in the center, two outcome panels on the right (each with three internal badges), one fan-in spine and two outgoing arrows, three legend items each once. No printed layout words, no title above the canvas.
```
