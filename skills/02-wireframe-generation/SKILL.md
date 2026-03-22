# Skill 02 — Wireframe Generation

## Purpose
Generate 4-6 divergent low-fi wireframe concepts from the structured brief produced by Skill 01. Every concept must cover both a UI direction (layout, structure, hierarchy) and a UX direction (interaction model, flow, mental model). Concepts must represent genuinely different approaches — not variations of the same layout.

## Core principle
Every concept traces back to:
- The structured brief (problem, users, success, constraints)
- A named UX framework: JTBD or mental model alignment
- An identifiable design pattern or convention

Random or generic layouts are not acceptable output.

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
- The job is the progress the user is trying to make, not the feature itself
- Each concept answers the same job differently

## Mental model alignment framing
Answer before generating: "What does the user already know that this should feel like?"
- Map each concept to a different reference model the user already carries

---

## SVG WIREFRAME STANDARD

### Output
A SINGLE SVG file containing ALL concepts side by side on one canvas.
Output using the create_file tool named: wireframes-[flow]-[date].svg

### Canvas
- Background: #FFFFFF
- Concepts arranged in a horizontal row, 80px gap between artboards
- Mobile artboard: 390 x 844px
- Desktop artboard: 1440 x 900px
- Canvas width: (artboard width x number of concepts) + (80 x number of gaps) + 80px padding each side
- Canvas height: artboard height + 120px (60px above for label, 60px below for padding)

### Concept label (above each artboard)
- Concept name: font-size 13, font-weight 600, fill #111111, centered above artboard
- Framework tag: font-size 11, fill #999999, centered, 18px below name
- 24px gap between tag and top of artboard

### Artboard
- fill #F7F7F7, stroke #E2E2E2, stroke-width 1, rx 12

---

## WIREFRAME VISUAL RULES — STRICT

### What wireframes communicate
Layout, hierarchy, and interaction model ONLY.
Not content. Not copy. Not detailed UI states.

### Level of detail
Wireframes should show enough structure to communicate the UX direction clearly — not so much that they read like a finished design or spec document.

Include:
- All primary UI zones (nav, content sections, CTA)
- Key interactive elements labelled (inputs, buttons, selectors)
- Hierarchy through size and visual weight of shapes
- Icons in appropriate positions to imply element purpose
- Progress indicators where the flow is multi-step
- A trust/security element where the context calls for it (e.g. financial, healthcare)

Do not include:
- Actual copy or content text
- More than 3 words on any label
- Secondary or edge-case states
- Decorative detail
- Multiple screen states within one artboard

### The golden rule — less is more
Each artboard shows ONE primary screen.
Show only the essential structure of that screen.
No mini-screens. No secondary states. No annotation text inside the artboard.

### Shape rules
| Element | Fill | Stroke | Notes |
|---|---|---|---|
| Screen background | #F7F7F7 | none | artboard fill |
| Navigation bar | #EBEBEB | none | full width, 56px tall |
| Section container / card | #E8E8E8 | none | rx 8 |
| Input field | #DEDEDE | #C8C8C8 1px | rx 6, 48px tall |
| Primary CTA button | #CACACA | none | rx 8, 52px tall, full width |
| Secondary button | #F0F0F0 | #D0D0D0 1px | rx 8 |
| Image / media placeholder | #D8D8D8 | none | rx 8 |
| Progress bar track | #E8E8E8 | none | 4px tall |
| Progress bar fill | #C0C0C0 | none | 4px tall |
| Divider | none | #E8E8E8 0.5px | horizontal line |

### Icon usage
Use open source SVG icon paths from Lucide Icons (https://lucide.dev). Embed icons as inline SVG path elements — never use emoji.

Icon rules:
- Size: 16px for inline UI icons, 20px for card icons, 32-48px for hero/empty-state icons
- Stroke colour: #AAAAAA for inactive, #888888 for active, #BBBBBB for disabled
- stroke-width: 2, stroke-linecap: round, stroke-linejoin: round, fill: none
- Wrap in: g transform="translate(x,y) scale(s)"

Common icons to use:
| UI element        | Lucide icon    | Path |
|-------------------|----------------|------|
| Camera / upload   | camera         | M23 19a2 2 0 0 1-2 2H3a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h4l2-3h6l2 3h4a2 2 0 0 1 2 2zM12 17a4 4 0 1 0 0-8 4 4 0 0 0 0 8z |
| ID / document     | id-card        | M3 6a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2v12a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z |
| Face / selfie     | user           | M20 21v-2a4 4 0 0 0-4-4H8a4 4 0 0 0-4 4v2M12 11a4 4 0 1 0 0-8 4 4 0 0 0 0 8z |
| Bank / finance    | landmark       | M3 22V12M21 22V12M12 22V12M2 12l10-9 10 9M5 12v-2M19 12v-2 |
| Security / trust  | shield         | M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z |
| Lock              | lock           | M19 11H5a2 2 0 0 0-2 2v7a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-7a2 2 0 0 0-2-2zM7 11V7a5 5 0 0 1 10 0v4 |
| Search            | search         | M11 17.25a6.25 6.25 0 1 1 0-12.5 6.25 6.25 0 0 1 0 12.5zM16 16l4.5 4.5 |
| Checkmark         | check-circle   | M22 11.08V12a10 10 0 1 1-5.93-9.14M22 4 12 14.01l-3-3 |
| Arrow forward     | arrow-right    | M5 12h14M12 5l7 7-7 7 |
| Chevron           | chevron-right  | M9 18l6-6-6-6 |
| Settings / config | settings       | M12.22 2h-.44a2 2 0 0 0-2 2v.18a2 2 0 0 1-1 1.73l-.43.25a2 2 0 0 1-2 0l-.15-.08a2 2 0 0 0-2.73.73l-.22.38a2 2 0 0 0 .73 2.73l.15.1a2 2 0 0 1 1 1.72v.51a2 2 0 0 1-1 1.74l-.15.09a2 2 0 0 0-.73 2.73l.22.38a2 2 0 0 0 2.73.73l.15-.08a2 2 0 0 1 2 0l.43.25a2 2 0 0 1 1 1.73V20a2 2 0 0 0 2 2h.44a2 2 0 0 0 2-2v-.18a2 2 0 0 1 1-1.73l.43-.25a2 2 0 0 1 2 0l.15.08a2 2 0 0 0 2.73-.73l.22-.39a2 2 0 0 0-.73-2.73l-.15-.08a2 2 0 0 1-1-1.74v-.5a2 2 0 0 1 1-1.74l.15-.09a2 2 0 0 0 .73-2.73l-.22-.38a2 2 0 0 0-2.73-.73l-.15.08a2 2 0 0 1-2 0l-.43-.25a2 2 0 0 1-1-1.73V4a2 2 0 0 0-2-2zM12 15a3 3 0 1 0 0-6 3 3 0 0 0 0 6z |
| Notification      | bell           | M18 8A6 6 0 0 0 6 8c0 7-3 9-3 9h18s-3-2-3-9M13.73 21a2 2 0 0 1-3.46 0 |
| Home              | home           | M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2zM9 22V12h6v10 |
| Profile           | circle-user    | M18.39 14.56C16.71 13.7 14.53 13 12 13s-4.71.7-6.39 1.56A2.27 2.27 0 0 0 4 16.72V20h16v-3.28a2.27 2.27 0 0 0-1.61-2.16zM12 12a4 4 0 1 0 0-8 4 4 0 0 0 0 8z |

SVG icon snippet example:
g transform="translate(32,24) scale(0.67)" fill="none" stroke="#888888" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
  path d="M23 19a2 2 0 0 1-2 2H3a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h4l2-3h6l2 3h4a2 2 0 0 1 2 2zM12 17a4 4 0 1 0 0-8 4 4 0 0 0 0 8z"

| Avatar / icon placeholder | #D0D0D0 | none | circle |

### Text rules
Use ONLY these two text roles inside artboards:

Screen title (one per screen)
- font-size 15, font-weight 600, fill #1A1A1A

Element label (inside or directly below a shape)
- font-size 11, font-weight 400, fill #888888
- Maximum 3 words. Use common UI vocabulary: "Search", "Continue", "Upload ID", "Full name", "Nav bar", "Hero image", "CTA"

### What is NOT allowed
- No annotation text (no arrows with explanations, no after tapping X notes)
- No emoji anywhere in the SVG
- No inline commentary or copy-style text
- No mock content (no fake names, no placeholder copy)
- No colour beyond the grey palette above
- No shadows, no gradients, no decorative elements
- No status bar details (no clock, battery, signal icons)
- No multi-screen flows within a single artboard

### Navigation bar
Every mobile screen gets a simple nav bar at the top:
- Full-width rect, height 56px, fill #EBEBEB, positioned at y=0 within artboard
- One centered label: the screen name (font-size 13, font-weight 500, fill #555555)
- No back arrows, no icons, no status bar

### Layout structure
Use only these zones within the artboard (stack vertically):
1. Nav bar (56px)
2. Optional progress indicator (24px) — rect track + rect fill
3. Content zone (flexible) — the primary UI elements
4. CTA zone (bottom 100px) — button(s) only

Within the content zone, use large shape blocks to represent UI regions:
- A tall rect = a card, a list, a form section, a media area
- A wide short rect = a tab bar, a filter row, a label row
- Stack them with 16px gaps

### Showing flow or steps
If a concept is multi-step, show ONLY the first screen.
Add a simple step indicator below the nav bar:
- 3-5 small circles (r=4), fill #C0C0C0 for active, #E8E8E8 for inactive, 10px apart
- No text labels on the circles

---

## OUTPUT FORMAT

First, show the concepts overview in text:
CONCEPTS OVERVIEW
-----------------
Brief: [one-line summary of the design brief]

1. [Name] — [UI direction] / [UX direction] / [Framework]
2. [Name] — [UI direction] / [UX direction] / [Framework]
3. [Name] — [UI direction] / [UX direction] / [Framework]
4. [Name] — [UI direction] / [UX direction] / [Framework]

Then output the SVG file via create_file.
Then provide concept rationale (Skill 03 output) immediately after.

---

## RULES
- Generate exactly 4-6 concepts
- Each concept uses a different divergence angle
- No repeated layout structures
- One screen per artboard — the primary/entry screen only
- If Skill 04 ran: at least one concept must deliberately diverge from the dominant pattern
- Always show the brief summary so the user can verify grounding

## HANDOFF
Pass selected concept and metadata to:
- Skill 03 (Concept Rationale) — always
- Skill 05 (Post-Convergence Handoff) — when user selects final direction