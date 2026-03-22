# Skill 02 — Wireframe Generation

## Purpose
Generate 4-6 divergent low-fi wireframe concepts from the structured brief produced by Skill 01. Every concept must cover both a UI direction (layout, structure, hierarchy) and a UX direction (interaction model, flow, mental model). Concepts must represent genuinely different approaches — not variations of the same layout.

## Core principle
Every concept traces back to:
- The structured brief (problem, users, success, constraints)
- A named UX framework: JTBD or mental model alignment
- An identifiable design pattern or convention

## Divergence strategy
Assign each concept one distinct angle — no repeats:

| Angle          | Question to answer                                    |
|----------------|-------------------------------------------------------|
| Progressive    | What if the user is guided step by step?              |
| Minimal        | What is the absolute least we can show?               |
| Power user     | What if the user wants everything upfront?            |
| Unconventional | What would a non-obvious interaction model look like? |
| Mobile-first   | What if constraints forced radical simplification?    |
| Familiar       | What mental model does the user already have?         |

## JTBD framing
Answer before generating: "What job is the user hiring this feature to do?"
The job is the progress the user is trying to make, not the feature itself.
Each concept answers the same job differently.

## Mental model alignment framing
Answer before generating: "What does the user already know that this should feel like?"
Map each concept to a different reference model the user already carries.

---

## SVG WIREFRAME STANDARD

### Output
A SINGLE SVG file containing ALL concepts side by side on one canvas.
Output using the create_file tool, named: wireframes-[flow]-[date].svg

### Canvas
- Background: #FFFFFF
- Concepts in a horizontal row, 80px gap between artboards
- Mobile artboard: 390 x 844px
- Desktop artboard: 1440 x 900px
- Canvas width: (artboard_width x num_concepts) + (80 x num_gaps) + 120px total padding
- Canvas height: artboard_height + 120px (64px above for label, 56px below)

### Concept label above each artboard
- Name: font-size 13, font-weight 600, fill #111111, centered
- Framework tag: font-size 11, fill #999999, centered, 20px below name
- 24px gap between tag and top of artboard

### Artboard
- fill #F7F7F7, stroke #E2E2E2, stroke-width 1, rx 12

---

## WIREFRAME VISUAL RULES

### What wireframes communicate
Layout, hierarchy, and interaction model ONLY. Not content. Not copy.

### The golden rule
Each artboard shows ONE primary screen. No mini-screens. No secondary states. No annotation text inside artboards.

### Level of detail
Include:
- All primary UI zones (nav bar, content sections, CTA zone)
- Key interactive elements with short labels (max 3 words each)
- Hierarchy through size and visual weight of shapes
- Icons in appropriate positions to imply element purpose
- Progress indicator where the flow is multi-step
- Trust/security element where context calls for it

Do NOT include:
- Actual copy or content text
- More than 3 words on any element label
- Multiple screen states in one artboard
- Annotation arrows or commentary text
- Emoji anywhere in the SVG

### Shape palette
| Element                  | Fill    | Stroke          | Notes              |
|--------------------------|---------|-----------------|--------------------|
| Screen background        | #F7F7F7 | none            | artboard fill      |
| Navigation bar           | #EBEBEB | none            | full width, 56px   |
| Section container / card | #E8E8E8 | none            | rx 8               |
| Input field              | #DEDEDE | #C8C8C8 1px     | rx 6, 48px tall    |
| Primary CTA button       | #CACACA | none            | rx 10, 52px tall   |
| Secondary button         | #F0F0F0 | #D0D0D0 1px     | rx 8               |
| Image / media placeholder| #D8D8D8 | none            | rx 8               |
| Dashed upload zone       | #E8E8E8 | #D0D0D0 1px dash| rx 10              |
| Progress bar track       | #E0E0E0 | none            | 3px tall           |
| Progress bar fill        | #AAAAAA | none            | 3px tall           |
| Trust / info row         | #EEEEEE | none            | rx 6, 36px tall    |
| Divider                  | none    | #E8E8E8 0.5px   | horizontal line    |
| Step circle — active     | #AAAAAA | none            | r=5                |
| Step circle — inactive   | #E0E0E0 | none            | r=5                |
| Avatar / icon block      | #E0E0E0 | none            | circle or sq rx 8  |

### Text rules
Two text roles only inside artboards:

Screen title: font-size 16-18, font-weight 600, fill #1A1A1A
Element label: font-size 11-12, fill #888888 — max 3 words, standard UI vocabulary
Supporting label: font-size 11, fill #AAAAAA or #BBBBBB — for sub-labels and helper text

### Icon usage
Use Lucide Icons open source SVG paths (https://lucide.dev). Never emoji.

Icon rules:
- Size: 16px inline, 20-24px card icons, 32-64px hero/upload zones
- stroke: #AAAAAA active, #BBBBBB inactive — stroke-width 2, linecap round, linejoin round, fill none
- Wrap in: g transform="translate(x,y) scale(s)"

Common icon paths:
camera:       M23 19a2 2 0 0 1-2 2H3a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h4l2-3h6l2 3h4a2 2 0 0 1 2 2zM12 17a4 4 0 1 0 0-8 4 4 0 0 0 0 8z
user:         M20 21v-2a4 4 0 0 0-4-4H8a4 4 0 0 0-4 4v2M12 11a4 4 0 1 0 0-8 4 4 0 0 0 0 8z
shield:       M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z
lock:         M19 11H5a2 2 0 0 0-2 2v7a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-7a2 2 0 0 0-2-2zM7 11V7a5 5 0 0 1 10 0v4
arrow-right:  M5 12h14M12 5l7 7-7 7
chevron-right:M9 18l6-6-6-6
check-circle: M22 11.08V12a10 10 0 1 1-5.93-9.14M22 4 12 14.01l-3-3
id-card:      M3 6a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2v12a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z
search:       M11 17.25a6.25 6.25 0 1 1 0-12.5 6.25 6.25 0 0 1 0 12.5zM16 16l4.5 4.5
bell:         M18 8A6 6 0 0 0 6 8c0 7-3 9-3 9h18s-3-2-3-9M13.73 21a2 2 0 0 1-3.46 0
home:         M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2zM9 22V12h6v10
settings:     M12 15a3 3 0 1 0 0-6 3 3 0 0 0 0 6z

### Navigation bar
Every screen gets a nav bar:
- Full-width rect, height 56px, fill #EBEBEB, rx 12 at top only (clip bottom corners with additional rect)
- Centered screen name label: font-size 13, font-weight 500, fill #444444
- No status bar, no back arrows, no icons in nav

### Layout zones (top to bottom)
1. Nav bar — 56px
2. Progress indicator (if multi-step) — 24px track + 16px dots row = 40px total
3. Content zone — primary UI elements stacked with 16px gaps
4. CTA zone — bottom 120px: primary button (52px) + optional secondary link

### Multi-step flows
Show first screen only. Use step dots below nav bar for context:
- Circles r=5, #AAAAAA active, #E0E0E0 inactive, 12px apart, horizontally centered

---

## OUTPUT FORMAT

Show text summary first:
CONCEPTS OVERVIEW
-----------------
Brief: [one-line summary]

1. [Name] — [UI direction] / [UX direction] / [Framework]
2. [Name] — [UI direction] / [UX direction] / [Framework]
3. [Name] — [UI direction] / [UX direction] / [Framework]
4. [Name] — [UI direction] / [UX direction] / [Framework]

Then output SVG via create_file tool.
Then provide Skill 03 rationale immediately after.

---

## RULES
- Exactly 4-6 concepts
- One unique divergence angle per concept — no repeats
- No repeated layout structures
- One screen per artboard — primary screen only
- If Skill 04 ran: at least one concept must diverge from the dominant competitive pattern
- Always show brief summary so user can verify grounding before reviewing

## HANDOFF
- Skill 03 (Concept Rationale) — always
- Skill 05 (Post-Convergence Handoff) — when user selects final direction