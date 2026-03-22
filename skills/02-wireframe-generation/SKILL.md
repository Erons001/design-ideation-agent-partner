# Skill 02 — Wireframe Generation

## Purpose
Generate exactly 4 divergent low-fi wireframe concepts from the structured brief and competitive analysis. Every concept must be rooted in a clear design hypothesis — a reasoned position on what will work for this specific user in this specific context.

## Scope determines output format

### SINGLE SCREEN
4 concepts = 4 different ways to design the same screen.
Each artboard shows ONE screen. Divergence is in layout, hierarchy, and interaction model.

### WORKFLOW
4 concepts = 4 different ways to structure the same multi-screen journey.
Each concept shows a MINI FLOW of 2-3 key screens connected by arrows.
Divergence is in how the journey is structured: what is split vs combined, what gates what, how many steps, how the user enters and exits.

## Core principle
Every concept traces back to:
- The structured brief (problem, users, success, constraints)
- The competitive analysis — FOLLOW, CHALLENGE, BORROW must each appear across the 4 concepts
- A named UX framework: JTBD or mental model alignment
- A specific insight about this user's psychology, context, or expectation

Concepts that are just different layouts are not acceptable. Every concept needs a why.

## Divergence angles — assign one per concept, no repeats

| Angle          | Single screen meaning                           | Workflow meaning                                  |
|----------------|-------------------------------------------------|---------------------------------------------------|
| Progressive    | Information revealed as user scrolls or acts    | Journey split into many small focused steps       |
| Minimal        | Absolute least shown on screen                  | Fewest screens possible — maximum collapsing      |
| Power user     | Everything visible at once                      | Non-linear — user can jump between steps          |
| Unconventional | Non-obvious layout or interaction model         | Unexpected sequencing or entry point              |
| Familiar       | Maps to a known UI pattern the user already has | Mirrors a familiar journey from another domain    |
| Hub and spoke  | Central screen, actions branch off it           | Central status hub with branching sub-flows       |

## Competitive directives — required
From Skill 04: FOLLOW, CHALLENGE, BORROW must each map to at least one concept.
State which directive maps to which concept in the overview.

## JTBD and mental model framing
JTBD: "What job is the user hiring this feature to do?" Each concept answers the same job differently.
Mental model: "What does the user already know that this should feel like?" Each concept maps to a different reference model.

---

## PRE-GENERATION THINKING — REQUIRED BEFORE DRAWING ANY WIREFRAME

Before producing any SVG, work through the following for all 4 concepts. This is the design reasoning the wireframe must visually express. A wireframe that cannot be explained by this reasoning should not be generated.

For each of the 4 concepts, answer before starting:

1. DESIGN HYPOTHESIS
   "If [specific user type] [specific belief or behaviour], then [design approach] will [outcome] because [reason]."
   This must be falsifiable. If it cannot be proven wrong, rewrite it.

2. PSYCHOLOGICAL PRINCIPLE
   Name the specific principle and show exactly how the layout or flow decision expresses it.
   Not just naming it — show how a specific design decision embodies it.
   Choose from: completion bias, loss aversion, progressive commitment, familiarity effect, autonomy bias, cognitive load reduction, social proof, reciprocity, endowment effect, anchoring, Zeigarnik effect, scarcity, authority, default bias, peak-end rule, chunking.

3. SPECIFIC FRICTION ADDRESSED
   The exact moment of hesitation, confusion, or drop-off this concept targets.
   Name the moment specifically — not "reduces friction."

4. THE BET THIS CONCEPT MAKES
   What assumption about the user does this concept make that the other 3 do not?
   If two concepts share the same bet, replace one before generating.

5. COMPETITIVE POSITION
   Which directive — FOLLOW, CHALLENGE, or BORROW — does this concept respond to, and exactly how?

Once all 4 hypotheses are established and genuinely distinct, generate the SVG.
Every major layout decision must be traceable to the reasoning above.

---

## SVG WIREFRAME STANDARD

### Platform — never assume
Use the platform confirmed in the structured brief. Never default to mobile.
- Mobile: 390 x 844px artboards
- Desktop: 1440 x 900px artboards
- Responsive: generate BOTH mobile and desktop artboards per concept — 8 total, grouped in pairs

### Output
A SINGLE SVG file with ALL 4 concepts on one canvas.
Output via create_file tool named: wireframes-[flow]-[date].svg

### SINGLE SCREEN canvas — mobile
- 4 artboards in a horizontal row, 80px gap between
- Canvas width: (390 x 4) + (80 x 3) + 120px = 1920px
- Canvas height: 844 + 120px = 964px

### SINGLE SCREEN canvas — desktop
- 4 artboards in a horizontal row, 80px gap between
- Canvas width: (1440 x 4) + (80 x 3) + 120px = 6120px
- Canvas height: 900 + 120px = 1020px

### SINGLE SCREEN canvas — responsive (mobile + desktop)
- 8 artboards — mobile/desktop pairs, 40px gap within pair, 80px between concept groups
- Mobile first, desktop second in each pair
- Canvas width: ((390 + 40 + 1440) x 4) + (80 x 3) + 120px = 7800px
- Canvas height: 900 + 120px = 1020px (desktop height is taller, use that)

### WORKFLOW canvas — mobile
- 4 concept rows stacked vertically, 60px gap between rows
- Each row: 2-3 mini-screens (220x476px) side by side with flow arrows (32px, stroke #CCCCCC 1.5px)
- Concept labels sit to the LEFT in a 200px column
- Canvas width: 200 + (220 x 3) + (32 x 2) + 80px = ~1024px
- Canvas height: (476 x 4) + (60 x 3) + 180px = ~2264px

### WORKFLOW canvas — desktop
- 4 concept rows stacked vertically, 60px gap between rows
- Each row: 2-3 mini-screens (480x270px) side by side with flow arrows
- Concept labels to the LEFT in a 200px column
- Canvas width: 200 + (480 x 3) + (40 x 2) + 80px = ~1800px
- Canvas height: (270 x 4) + (60 x 3) + 180px = ~1440px

### Artboard
- fill #F7F7F7, stroke #E2E2E2, stroke-width 1, rx 12 (full) or rx 6 (mini workflow)

### Concept label
- Name: font-size 13, font-weight 600, fill #111111
- Angle + framework: font-size 11, fill #999999
- Competitive position tag: font-size 10, fill #BBBBBB (FOLLOW / CHALLENGE / BORROW)

---

## WIREFRAME VISUAL RULES — STRICT

### What wireframes communicate
Layout, hierarchy, and interaction model ONLY. Not content. Not copy.

### The golden rule
Single screen: ONE screen per artboard. No secondary states, no annotation text.
Workflow: 2-3 mini-screens per row. Key steps only — no annotation text between screens.

### Level of detail
Include:
- All primary UI zones (nav, content sections, CTA)
- Key interactive elements with short labels (max 3 words)
- Icons where they imply element purpose (Lucide only, no emoji)
- Progress indicator for multi-step flows
- Trust/security element where context calls for it

Do NOT include:
- Actual copy or content text
- More than 3 words on any label
- Annotation text, arrows with explanations, commentary
- Emoji anywhere in the SVG
- Mock content or placeholder copy

### Shape palette
| Element                   | Fill    | Stroke         | Notes              |
|---------------------------|---------|----------------|--------------------|
| Screen background         | #F7F7F7 | none           | artboard fill      |
| Navigation bar — mobile   | #EBEBEB | none           | full width, 56px   |
| Navigation bar — desktop  | #EBEBEB | none           | full width, 64px   |
| Sidebar (desktop only)    | #EEEEEE | none           | 240px wide         |
| Section container / card  | #E8E8E8 | none           | rx 8               |
| Input field               | #DEDEDE | #C8C8C8 1px    | rx 6, 48px tall    |
| Primary CTA — mobile      | #CACACA | none           | rx 10, 52px, full width |
| Primary CTA — desktop     | #CACACA | none           | rx 10, 52px, 200-280px wide |
| Secondary button          | #F0F0F0 | #D0D0D0 1px    | rx 8               |
| Image / media placeholder | #D8D8D8 | none           | rx 8               |
| Dashed upload zone        | #E8E8E8 | #D0D0D0 dashed | rx 10              |
| Progress bar track        | #E0E0E0 | none           | 3px tall           |
| Progress bar fill         | #AAAAAA | none           | 3px tall           |
| Trust / info row          | #EEEEEE | none           | rx 6, 36px tall    |
| Divider                   | none    | #E8E8E8 0.5px  | horizontal line    |
| Step dot — active         | #AAAAAA | none           | r=5                |
| Step dot — inactive       | #E0E0E0 | none           | r=5                |
| Flow arrow (workflow)     | none    | #CCCCCC 1.5px  | horizontal + head  |

### Icon usage
Lucide Icons SVG paths only (https://lucide.dev). Never emoji.
stroke-width 2, linecap round, fill none. Wrap in g transform="translate(x,y) scale(s)"

Common icon paths:
camera:        M23 19a2 2 0 0 1-2 2H3a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h4l2-3h6l2 3h4a2 2 0 0 1 2 2zM12 17a4 4 0 1 0 0-8 4 4 0 0 0 0 8z
user:          M20 21v-2a4 4 0 0 0-4-4H8a4 4 0 0 0-4 4v2M12 11a4 4 0 1 0 0-8 4 4 0 0 0 0 8z
shield:        M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z
lock:          M19 11H5a2 2 0 0 0-2 2v7a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-7a2 2 0 0 0-2-2zM7 11V7a5 5 0 0 1 10 0v4
arrow-right:   M5 12h14M12 5l7 7-7 7
chevron-right: M9 18l6-6-6-6
check-circle:  M22 11.08V12a10 10 0 1 1-5.93-9.14M22 4 12 14.01l-3-3
search:        M11 17.25a6.25 6.25 0 1 1 0-12.5 6.25 6.25 0 0 1 0 12.5zM16 16l4.5 4.5
id-card:       M3 6a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2v12a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z
landmark:      M3 22V12M21 22V12M12 22V12M2 12l10-9 10 9M5 12v-2M19 12v-2
bell:          M18 8A6 6 0 0 0 6 8c0 7-3 9-3 9h18s-3-2-3-9M13.73 21a2 2 0 0 1-3.46 0
home:          M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2zM9 22V12h6v10

### Navigation bar
Mobile full: height 56px, fill #EBEBEB, screen name font-size 13, font-weight 500, fill #444444
Desktop full: height 64px, fill #EBEBEB, screen name font-size 14, font-weight 500, fill #444444
Mini (workflow): height 32px, fill #EBEBEB, screen name font-size 8, font-weight 500

### Text roles
Screen title: font-size 15-18 (mobile full) / 18-22 (desktop full) / 9 (mini), font-weight 600, fill #1A1A1A
Element label: font-size 11-12 (full) / 7 (mini), fill #888888, max 3 words
Supporting text: font-size 11 (full) / 7 (mini), fill #AAAAAA

---

## OUTPUT FORMAT

CONCEPTS OVERVIEW
-----------------
Brief: [one-line summary]
Scope: [SINGLE SCREEN or WORKFLOW]
Platform: [Mobile / Desktop / Responsive]
Competitive insight: [dominant pattern + main gap in one line]

1. [Name] — [angle] / [framework] / [FOLLOW or CHALLENGE or BORROW or original]
2. [Name] — [angle] / [framework] / [competitive position]
3. [Name] — [angle] / [framework] / [competitive position]
4. [Name] — [angle] / [framework] / [competitive position]

Then SVG file via create_file.
Then Skill 03 rationale immediately after.

---

## RULES
- Exactly 4 concepts — never more, never fewer
- Platform always taken from brief — never assumed, never defaulted to mobile
- Each concept uses a different divergence angle — no repeats
- No repeated layout or flow structures
- FOLLOW and CHALLENGE directives must each appear in at least one concept
- Pre-generation thinking must be completed before any SVG is drawn
- Single screen: one screen per artboard only
- Workflow: 2-3 mini-screens per row, connected by flow arrows
- Always show brief summary above concepts

## HANDOFF
- Skill 03 (Concept Rationale) — always
- Skill 05 (Post-Convergence Handoff) — when user selects final direction