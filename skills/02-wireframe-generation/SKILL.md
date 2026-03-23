# Skill 02 — Wireframe Generation

## Purpose
Generate exactly 4 divergent mid-fi wireframe concepts from the structured brief and competitive analysis. Every concept must be rooted in a clear design hypothesis — a reasoned position on what will work for this specific user in this specific context.

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

### Output
A SINGLE SVG file with ALL 4 concepts on one canvas.
Output via create_file tool named: wireframes-[flow]-[date].svg
Fidelity: mid-fi — real typography scale, real component shapes, greyscale only

---

### Universal canvas layout — always vertical stack

Regardless of whether the scope is SINGLE SCREEN or WORKFLOW, the canvas always uses this structure:

- 4 concept rows stacked vertically, one per concept
- Each row contains: [Notes panel] + [Screen(s) horizontally]
- Rows separated by 48px vertical gap
- Canvas has 40px padding on all sides

This makes the board easy to read top to bottom — one concept per row, screens reading left to right within each row.

---

### Row anatomy

Each concept row has two zones side by side:

ZONE 1 — Notes panel (left side)
- Width: 220px
- Height: matches the screen height for that row
- Background: #F0F0F0, rx 8
- Contains all UX framework annotations for this concept (see Notes panel spec below)
- 16px internal padding

ZONE 2 — Screen(s) (right side)
- SINGLE SCREEN: one artboard
- WORKFLOW: 2-3 mini-screens connected by flow arrows, arranged left to right
- 24px gap between notes panel and first screen
- 32px gap between screens within a workflow row

Total row width = 220px (notes) + 24px (gap) + screen zone width
Total row height = screen height + 16px top margin (for concept number label above)

---

### Artboard sizes

Mobile full size:    390 x 844px
Desktop full size:   1440 x 900px
Mobile mini (workflow):  220 x 476px  (56% scale)
Desktop mini (workflow): 540 x 338px  (37% scale)

For SINGLE SCREEN rows: use full size artboard
For WORKFLOW rows: use mini size artboards (2-3 per row)

---

### Canvas dimensions

SINGLE SCREEN mobile:
- Row width: 220 + 24 + 390 = 634px
- Row height: 844px
- Canvas width: 634 + 80px padding = 714px
- Canvas height: (844 x 4) + (48 x 3) + 80px padding = 3,700px

SINGLE SCREEN desktop:
- Row width: 220 + 24 + 1440 = 1684px
- Canvas width: 1684 + 80px padding = 1764px
- Canvas height: (900 x 4) + (48 x 3) + 80px = 3,824px

WORKFLOW mobile (2 mini-screens per concept):
- Row width: 220 + 24 + 220 + 32 + 220 = 716px
- Row height: 476px
- Canvas width: 716 + 80px = 796px
- Canvas height: (476 x 4) + (48 x 3) + 80px = 2,128px

WORKFLOW mobile (3 mini-screens per concept):
- Row width: 220 + 24 + 220 + 32 + 220 + 32 + 220 = 968px
- Canvas width: 968 + 80px = 1048px

---

### Concept number label
Above each row, show:
- "Concept [N]" — font-size 11, font-weight 600, fill #999999, positioned at x=40, y=(row_y - 6)
- This floats just above the notes panel + screens

---

### Notes panel spec

The notes panel is a key part of the SVG — it makes the wireframe board self-explanatory without needing a separate document.

Content (top to bottom, 16px internal padding, 6px line spacing):

IMPORTANT: Never truncate any text in the notes panel. All text must be shown in full.
SVG does not auto-wrap text — use tspan elements with dy attributes to wrap long values across multiple lines.
The notes panel height will flex to fit its content — calculate actual height needed before drawing.

1. Concept name
   font-size 12, font-weight 600, fill #1A1A1A
   e.g. "One Step at a Time"

2. Divergence angle pill
   Small rect: fill #E0E0E0, rx 10, height 20px, width fits text + 16px padding
   font-size 10, fill #555555
   e.g. "Progressive"

3. UX Framework
   font-size 10, fill #888888, label "Framework:"
   font-size 10, font-weight 500, fill #444444, value e.g. "JTBD"

4. Job / Model (one line, wraps to max 200px width)
   font-size 10, fill #888888, label "Job / Model:"
   font-size 10, fill #444444, value — the specific job or mental model (max 2 lines, truncate with … if needed)

5. Divider line
   stroke #DDDDDD, 0.5px, full width of panel

6. Competitive position
   font-size 10, fill #888888, label "Pattern:"
   font-size 10, fill #444444, value — FOLLOW / CHALLENGE / BORROW + one-word descriptor
   e.g. "FOLLOW — step wizard"
   e.g. "CHALLENGE — removes account gate"
   e.g. "BORROW — delivery tracker model"
   All text in the pattern row uses fill #444444 — no colour coding, no coloured labels

7. Design hypothesis — show in full, never truncate
   font-size 9, fill #AAAAAA, italic style
   Wrap text across multiple lines using tspan elements — SVG does not auto-wrap
   Each line maximum 26 characters — break at word boundaries using tspan dy="12"
   Show the complete hypothesis — do not use ellipsis or cut off mid-sentence

---

### Flow arrows (workflow rows only)
Between mini-screens within a row:
- Horizontal line: stroke #CCCCCC, stroke-width 1.5
- Arrowhead at right end: simple filled triangle, 6x8px, fill #CCCCCC
- Vertically centered at 50% of screen height

---

### Artboard spec
- fill #F7F7F7, stroke #E2E2E2, stroke-width 1
- rx 12 for full size, rx 6 for mini

## WIREFRAME VISUAL RULES — MID-FI

### What mid-fi wireframes are
Mid-fi sits between lo-fi (grey blocks only) and hi-fi (final polished design).
Mid-fi wireframes show real visual hierarchy, real component shapes, real typography sizing, and real spacing — but remain fully greyscale with no colour decisions.

The goal: a designer or PM can look at the wireframe and understand the actual experience — not just the layout structure.

### What mid-fi communicates
- Real typography scale — heading sizes, body sizes, label sizes create visible hierarchy
- Real component shapes — buttons look like buttons, inputs look like inputs, cards have proper corner radii and depth cues
- Real spacing — padding and margins reflect actual design intent
- Real icons — Lucide SVG paths at appropriate sizes, positioned correctly
- Real interaction states implied — primary vs secondary vs text-link hierarchy is visible
- Still greyscale — no colour. Dark fills (#111111 to #333333) for primary elements, mid-grey (#777777 to #AAAAAA) for secondary, light grey (#DDDDDD to #F5F5F5) for backgrounds and containers

### What mid-fi does NOT include
- No colour fills (no blues, greens, reds — greyscale only)
- No final copy or real content text — use representative labels
- No detailed illustrations or decorative elements
- No multiple interaction states per element — show default state only
- No brand-specific styling decisions

---

### Typography scale (mid-fi)

Use real font sizes to create visible hierarchy. Every text element must use the correct size for its role.

| Role | font-size | font-weight | fill |
|---|---|---|---|
| Screen / page title | 20-24px | 700 | #111111 |
| Section heading | 17-18px | 600 | #1A1A1A |
| Body / description | 13-14px | 400 | #555555 |
| Label (above input) | 12px | 500 | #333333 |
| Input placeholder | 13px | 400 | #AAAAAA |
| Caption / helper text | 11px | 400 | #888888 |
| Button label (primary) | 15px | 600 | #FFFFFF or #111111 |
| Button label (secondary) | 14px | 500 | #333333 |
| Text link | 13px | 400 | #333333 (underline) |
| Nav title | 15-16px | 600 | #111111 |
| Badge / tag | 11px | 500 | #555555 |

---

### Component shapes (mid-fi)

Render each component to look like the real thing — not a labelled grey block.

NAV BAR
- Mobile: full width, 56px tall, fill #FAFAFA, bottom border 1px #EEEEEE
- Desktop: full width, 64px tall, fill #FAFAFA, bottom border 1px #EEEEEE
- Back arrow: actual SVG chevron-left path, stroke #222222, 20x20px
- Nav title: centered, 15px, font-weight 600, fill #111111
- Right action (if any): text button or icon, right-aligned

INPUT FIELD
- Height: 48px (mobile), 44px (desktop)
- Fill: #FFFFFF, stroke: #DDDDDD 1px, rx: 8
- Label above: 12px, font-weight 500, fill #333333, 8px gap below label
- Placeholder text: 13px, fill #AAAAAA, 16px left padding
- Focus state (if showing): stroke #555555 1.5px
- Error state (if showing): stroke #CC0000 1px, helper text below in #CC0000

PRIMARY BUTTON
- Height: 52px (mobile full-width), 44px (desktop or inline)
- Fill: #111111, rx: 10
- Label: 15px, font-weight 600, fill #FFFFFF, centered
- Optional right arrow icon: arrow-right path, stroke #FFFFFF

SECONDARY BUTTON
- Height: 48px
- Fill: #FFFFFF, stroke: #CCCCCC 1px, rx: 10
- Label: 14px, font-weight 500, fill #333333

TEXT LINK / TERTIARY ACTION
- No background, no border
- 13px, fill #333333, text-decoration underline
- Centered or left-aligned depending on context

CARD / CONTAINER
- Fill: #FFFFFF, stroke: #EEEEEE 1px, rx: 12
- Inner padding: 16-20px
- Optional subtle shadow implied by stroke contrast against #F5F5F5 background

SECTION CONTAINER (on-screen grouping)
- Fill: #F5F5F5 or #F9F9F9, rx: 12
- No stroke — differentiated by fill alone

UPLOAD / MEDIA ZONE
- Fill: #F9F9F9, stroke: #DDDDDD 1.5px dashed, rx: 12
- Large icon centered (camera, upload — Lucide path, stroke #CCCCCC, 40-48px)
- Primary label below icon: 13px, fill #888888
- Sub-label: 11px, fill #BBBBBB

PROGRESS BAR
- Track: height 4px, fill #F0F0F0, rx 2
- Fill: height 4px, fill #333333, rx 2 (width = % complete)
- Step count label: 11px, fill #AAAAAA, above left
- Percentage label: 11px, fill #AAAAAA, above right

STEP INDICATOR (dots)
- Active dot: r=6, fill #111111 with inner white dot r=2.5
- Inactive dot: r=5, fill none, stroke #DDDDDD 1.5px
- Connector line between dots: stroke #EEEEEE 1px

LIST ROW / TRACKER ITEM
- Container: fill #F5F5F5, rx 10, padding 16px
- Left icon or number circle: 32-36px circle, fill #E8E8E8 (inactive) or #333333 (active)
- Title: 13px, font-weight 600, fill #1A1A1A (active) or #AAAAAA (inactive)
- Sub-label: 12px, fill #AAAAAA
- Meta label (time, status): 11px, fill #BBBBBB
- Right chevron: chevron-right path, stroke #CCCCCC

TRUST / INFO ROW
- Fill: #F5F5F5, rx 8, 40px tall
- Left icon: 16px, Lucide path, stroke #888888
- Text: 12px, fill #555555


LIST ROW / TRACKER ITEM — LAYOUT RULE (critical — prevents element overlap)
Each tracker row has four distinct horizontal zones. Never overlap them:

Zone 1 — Step number badge (leftmost)
  Circle, r=18-20, left edge at 12-16px from card left
  Contains ONLY the step number — no icon overlay
  Active: fill #222222, number fill #FFFFFF
  Inactive: fill #DDDDDD, number fill #AAAAAA

Zone 2 — Icon block (separate from number badge, 8-12px gap to its right)
  Square rect, 32-36px, rx 8
  Fill #E4E4E4 (active) or #EEEEEE (inactive)
  Icon centered inside: 20-24px, stroke #888888 (active) or #BBBBBB (inactive)
  Do NOT overlay the icon on the number circle

Zone 3 — Text block (to the right of icon block, 8px gap)
  Title: 13px, font-weight 600, fill #111111 (active) or #AAAAAA (inactive)
  Subtitle: 11-12px, fill #AAAAAA
  Meta (time, status): 11px, fill #BBBBBB
  Stack vertically with 14-16px line spacing

Zone 4 — Action element (far right, vertically centered)
  Active row: chevron-right icon, stroke #CCCCCC
  Inactive row: lock icon, stroke #DDDDDD
  Or: action button if row is interactive

Total row height: 88-96px
Inter-row connector: dashed vertical line from bottom of Zone 1 circle to top of next row's circle


BADGE / PILL
- Fill: #EEEEEE, rx 12, height 24px, padding 0 12px
- Label: 11px, font-weight 500, fill #555555

DIVIDER
- Horizontal line, stroke #F0F0F0, stroke-width 1

BOTTOM SHEET / COLLAPSED ROW
- Fill: #F5F5F5, rx 8, height 40px
- Label: 12px, fill #888888, left-aligned with 16px padding
- Expand icon (+): fill #AAAAAA, right-aligned

---

### Icon usage (mid-fi)

Use Lucide Icons SVG paths (https://lucide.dev). All icons:
- stroke-width: 1.8 (slightly lighter than lo-fi for refined feel)
- stroke-linecap: round, stroke-linejoin: round, fill: none
- Wrap in g transform="translate(x,y) scale(s)"

Size guidance:
- Nav icons: 20x20px (scale 0.83)
- Inline UI icons: 16x16px (scale 0.67)
- Card/list icons: 20-24px (scale 0.83-1.0)
- Hero/upload zone icons: 40-48px (scale 1.67-2.0)
- stroke colour: #888888 standard, #CCCCCC placeholder/inactive, #222222 active/emphasis

Common icon paths:
camera:        M23 19a2 2 0 0 1-2 2H3a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h4l2-3h6l2 3h4a2 2 0 0 1 2 2zM12 17a4 4 0 1 0 0-8 4 4 0 0 0 0 8z
chevron-left:  M15 18l-6-6 6-6
chevron-right: M9 18l6-6-6-6
arrow-right:   M5 12h14M12 5l7 7-7 7
shield:        M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z
lock:          M19 11H5a2 2 0 0 0-2 2v7a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-7a2 2 0 0 0-2-2zM7 11V7a5 5 0 0 1 10 0v4
check-circle:  M22 11.08V12a10 10 0 1 1-5.93-9.14M22 4 12 14.01l-3-3
user:          M20 21v-2a4 4 0 0 0-4-4H8a4 4 0 0 0-4 4v2M12 11a4 4 0 1 0 0-8 4 4 0 0 0 0 8z
id-card:       M3 6a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2v12a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z
search:        M11 17.25a6.25 6.25 0 1 1 0-12.5 6.25 6.25 0 0 1 0 12.5zM16 16l4.5 4.5
bell:          M18 8A6 6 0 0 0 6 8c0 7-3 9-3 9h18s-3-2-3-9M13.73 21a2 2 0 0 1-3.46 0
home:          M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2zM9 22V12h6v10
landmark:      M3 22V12M21 22V12M12 22V12M2 12l10-9 10 9M5 12v-2M19 12v-2

---

### Screen background
- Mobile screen bg: #FFFFFF (white, not grey)
- Desktop content area bg: #FFFFFF
- Page/app bg behind screens: #F5F5F5

### Artboard
- fill #FFFFFF, stroke #E2E2E2, stroke-width 1, rx 12 (full), rx 6 (mini)

### Layout zones (mid-fi, top to bottom)
1. Nav bar — 56px mobile, 64px desktop
2. Progress/step indicator if multi-step — 48px
3. Content zone — components with real spacing (16-24px gaps between elements)
4. Secondary content / supporting info
5. CTA zone — bottom 120px: primary button + optional text link below

### Spacing in mid-fi
- Screen edge padding: 20px (mobile), 40px (desktop)
- Gap between form elements: 20px
- Gap between sections: 32px
- Card internal padding: 16-20px
- Button height: 52px (mobile primary), 44px (desktop or secondary)

---

## OUTPUT FORMAT## OUTPUT FORMAT

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

### Desktop wireframe rules (additional)
- Nav bar: full width, 64px tall, fill #EBEBEB
- Sidebar (if layout calls for it): 240px wide, full height, fill #EEEEEE
- Content area: remaining width after sidebar, max 1200px centered
- Desktop CTAs: not necessarily full-width — 200-280px wide, left-aligned or inline
- Desktop inputs: typically 40-50% width, not full-width like mobile
- More whitespace — desktop layouts breathe more than mobile

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