# Skill 02 — Wireframe Generation

## Purpose
Generate exactly 4 divergent low-fi wireframe concepts from the structured brief and competitive analysis. Every concept must explore a meaningfully different approach — not variations of the same idea.

## Scope determines output format

### SINGLE SCREEN
4 concepts = 4 different ways to design the same screen.
Each artboard shows ONE screen. Divergence is in layout, hierarchy, and interaction model.

### WORKFLOW
4 concepts = 4 different ways to structure the same multi-screen journey.
Each concept artboard shows a MINI FLOW of 2-3 key screens connected by arrows.
Divergence is in how the journey is structured: what is split vs combined, what gates what, how many steps, what the entry and exit look like.

## Core principle
Every concept traces back to:
- The structured brief (problem, users, success, constraints)
- The competitive analysis directives — FOLLOW, CHALLENGE, BORROW must each appear in at least one concept
- A named UX framework: JTBD or mental model alignment

## Divergence angles — assign one per concept, no repeats

| Angle          | Single screen meaning                           | Workflow meaning                                  |
|----------------|-------------------------------------------------|---------------------------------------------------|
| Progressive    | Information revealed as user scrolls or acts   | Journey split into many small focused steps       |
| Minimal        | Absolute least shown on screen                  | Fewest screens possible — maximum collapsing      |
| Power user     | Everything visible at once                      | Non-linear — user can jump between steps          |
| Unconventional | Non-obvious layout or interaction model         | Unexpected sequencing or entry point              |
| Familiar       | Maps to a known UI pattern the user already has | Mirrors a familiar journey from another domain    |
| Hub and spoke  | Central screen, actions branch off it           | Central status hub with branching sub-flows       |

## Competitive analysis — required integration
Review the FOLLOW, CHALLENGE, and BORROW directives from Skill 04 before generating.
- At least one concept must follow the dominant pattern (FOLLOW directive)
- At least one concept must address the identified gap (CHALLENGE directive)
- At least one concept may borrow the adjacent pattern (BORROW directive)
State which competitive directive maps to which concept in the overview.

## JTBD framing
Answer before generating: "What job is the user hiring this feature to do?"
Each concept answers the same job differently.

## Mental model alignment framing
Answer before generating: "What does the user already know that this should feel like?"
Map each concept to a different reference model the user already carries.

---

## PRE-GENERATION THINKING — REQUIRED BEFORE DRAWING ANY WIREFRAME

Before producing any SVG, work through the following for all 4 concepts. This thinking is what the wireframe must visually express. A wireframe that cannot be explained by this reasoning should not be generated.

For each of the 4 concepts, answer before starting:

1. What is the design hypothesis?
   Format: "If [user type] [specific belief or behaviour], then [design approach] will [outcome] because [reason]."

2. What psychological principle does this concept use, and how does the specific layout or flow decision express it?
   Not just naming a principle — show how a specific design decision embodies it.

3. What is the exact friction this concept addresses — the specific moment of hesitation, confusion, or drop-off in the user's current experience?

4. What bet is this concept making about the user that the other 3 are not?
   If two concepts share the same bet, replace one before generating.

5. Which competitive directive does this concept respond to — FOLLOW, CHALLENGE, or BORROW — and exactly how does the layout or flow reflect that position?

Once all 4 concept hypotheses are established and are genuinely distinct, generate the SVG. Every major layout decision should be traceable to the reasoning above.

---

## SVG WIREFRAME STANDARD

### Output
A SINGLE SVG file with ALL 4 concepts on one canvas.
Output via create_file tool named: wireframes-[flow]-[date].svg

### SINGLE SCREEN canvas
- 4 artboards in a horizontal row, 80px gap between
- Mobile: 390x844px per artboard | Desktop: 1440x900px
- Canvas width: (artboard_width x 4) + (80 x 3) + 120px padding
- Canvas height: artboard_height + 120px

### WORKFLOW canvas
- 4 concept rows stacked vertically, 60px gap between rows
- Each row shows 2-3 mini-screens side by side with flow arrows
- Mini-screen size: 220x476px (mobile) — approx 56% of full size
- Flow arrow between screens: 32px wide, stroke #CCCCCC 1.5px, horizontal with arrowhead
- Canvas width: (220 x 3) + (32 x 2) + 280px (label column left + padding) = ~940px
- Canvas height: (476 x 4) + (60 x 3) + 180px = 2264px
- Concept label and tags sit to the LEFT of each flow row in a 200px column

### Artboard / mini-screen
- fill #F7F7F7, stroke #E2E2E2, stroke-width 1, rx 12 (full size) or rx 6 (mini)

---

## WIREFRAME VISUAL RULES — STRICT

### What wireframes communicate
Layout, hierarchy, and interaction model ONLY. Not content. Not copy.

### The golden rule
Single screen: ONE screen per artboard. No secondary states.
Workflow: 2-3 mini-screens per row. Key steps of the flow only — no annotation text between screens.

### Level of detail
Include:
- All primary UI zones (nav, content sections, CTA)
- Key interactive elements with short labels (max 3 words)
- Icons where they imply element purpose
- Progress indicator for multi-step flows
- Trust/security element where context calls for it

Do NOT include:
- Actual copy or content text
- More than 3 words on any label
- Annotation text or commentary inside artboards
- Emoji anywhere in the SVG
- Mock content (no fake names, no placeholder copy)

### Shape palette
| Element                   | Fill    | Stroke         | Notes              |
|---------------------------|---------|----------------|--------------------|
| Screen background         | #F7F7F7 | none           | artboard fill      |
| Navigation bar            | #EBEBEB | none           | full width, 56px   |
| Section container / card  | #E8E8E8 | none           | rx 8               |
| Input field               | #DEDEDE | #C8C8C8 1px    | rx 6, 48px tall    |
| Primary CTA button        | #CACACA | none           | rx 10, 52px tall   |
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
Full size — height 56px, fill #EBEBEB, screen name font-size 13, font-weight 500, fill #444444
Mini (workflow) — height 32px, fill #EBEBEB, screen name font-size 8, font-weight 500

### Text roles
Screen title: font-size 15-18 (full) or 9 (mini), font-weight 600, fill #1A1A1A
Element label: font-size 11-12 (full) or 7 (mini), fill #888888, max 3 words
Supporting text: font-size 11 (full) or 7 (mini), fill #AAAAAA

---

## OUTPUT FORMAT

CONCEPTS OVERVIEW
-----------------
Brief: [one-line summary]
Scope: [SINGLE SCREEN or WORKFLOW]
Competitive insight: [one-line summary of dominant pattern and main gap]

1. [Name] — [angle] / [framework] / [FOLLOW / CHALLENGE / BORROW / original]
2. [Name] — [angle] / [framework] / [competitive position]
3. [Name] — [angle] / [framework] / [competitive position]
4. [Name] — [angle] / [framework] / [competitive position]

Then SVG file via create_file.
Then Skill 03 rationale immediately after.

---

### Desktop wireframe rules (additional)
- Nav bar: full width, 64px tall, fill #EBEBEB
- Sidebar (if layout calls for it): 240px wide, full height, fill #EEEEEE
- Content area: remaining width after sidebar
- Max content width: 1200px, centered with auto margins
- Desktop CTAs: not necessarily full-width — can be 200-280px wide, left-aligned or inline
- Desktop inputs: typically 50% width or less, not full-width like mobile

## RULES
- Exactly 4 concepts — never more, never fewer. If you find yourself generating a 5th, stop and replace the weakest concept instead.
- Each concept uses a different divergence angle
- No repeated layout or flow structures
- Competitive FOLLOW and CHALLENGE directives must each appear in at least one concept
- Single screen: one screen per artboard only
- Workflow: 2-3 mini-screens per row, connected by flow arrows
- Always show brief summary above concepts

## HANDOFF
- Skill 03 (Concept Rationale) — always
- Skill 05 (Post-Convergence Handoff) — when user selects final direction