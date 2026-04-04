# Skill 02 — Wireframe Generation

## Purpose
Generate exactly 4 divergent HIGH-FIDELITY wireframe concepts from the structured brief and competitive analysis. All 4 concepts use the same design system. Concepts differ in layout and UX direction — NOT in visual language.

## What high-fi wireframes are
High-fi wireframes use real design system tokens: actual brand colours, correct typography weights and sizes, proper component shapes with shadows and states, real spacing. They look like a finished design — missing only final content.

NOT mid-fi (greyscale shapes). NOT lo-fi (grey blocks). HIGH-FI with real colour and typography.

## Design system consistency — CRITICAL
All 4 concepts MUST use the same visual language:
- Same colour tokens (primary, neutrals, semantic)
- Same typography scale and font
- Same border radius values
- Same shadow styles
- Same component shapes

Concepts diverge in: layout structure, information hierarchy, interaction model, flow sequencing.
Concepts do NOT diverge in: colours, fonts, spacing, component styling.

All 4 concepts should feel like they belong to the same product.

---

## Default design system — Untitled UI
Use when no design system is provided.

### Colours
Primary:       #7F56D9 (buttons, active states, links, progress fills)
Primary hover: #6941C6
Primary light: #F9F5FF (badge fills, subtle backgrounds)
Primary border:#D6BBFB

Gray-900: #101828 (headings, primary text)
Gray-700: #344054 (secondary text, labels)
Gray-600: #475467 (body text)
Gray-500: #667085 (placeholder, captions)
Gray-400: #98A2B3 (icons, inactive)
Gray-300: #D0D5DD (input borders, card borders)
Gray-200: #EAECF0 (dividers, subtle borders)
Gray-100: #F2F4F7 (hover backgrounds, icon containers)
Gray-50:  #F9FAFB (page background, input hover)
White:    #FFFFFF (card bg, input bg, screen bg)

Success:  #039855
Error:    #D92D20
Warning:  #DC6803

### Typography — Inter
Screen/page title:  24px, 700, gray-900
Section heading:    20px, 600, gray-900
Card title:         16px, 600, gray-900
Body:               16px, 400, gray-600
Input label:        14px, 500, gray-700
Placeholder:        16px, 400, gray-500
Caption/helper:     14px, 400, gray-500
Button (large):     16px, 600, #FFFFFF or gray-700
Button (standard):  14px, 600
Badge:              12px, 500
Nav title (mobile): 16px, 600, gray-900

### Spacing (4px base)
Screen edge padding: 16px mobile, 40px desktop
Element gaps:        16-20px
Section gaps:        32-48px
Card padding:        24px
Input padding:       10px 14px
Button padding (lg): 10px 18px
Button padding (sm): 8px 14px

### Border radius
Input/Button: 8px
Card:         16px
Badge/Avatar: 9999px (pill)
Icon block:   12px
Modal:        16px
Nav bar:      0 (full width, no radius)

### Shadows
Card default: 0px 1px 3px rgba(16,24,40,0.10), 0px 1px 2px rgba(16,24,40,0.06)
Card hover:   0px 4px 8px rgba(16,24,40,0.10), 0px 2px 4px rgba(16,24,40,0.06)
Focus ring:   0px 0px 0px 4px rgba(159,122,237,0.24)

---

## Component library — Untitled UI

### Nav bar (mobile)
Height 56px, bg #FFFFFF, border-bottom 1px #EAECF0
Back: chevron-left, 20px, stroke #344054, left 16px
Title: centered, 16px 600, #101828
Right action (optional): icon or text button, right 16px

### Nav bar (desktop)
Height 64px, bg #FFFFFF, border-bottom 1px #EAECF0
Logo left, nav links center/left, actions right

### Primary button (mobile full-width)
Height 48px, bg #7F56D9, radius 8px, text #FFFFFF 16px 600
Shadow: 0 1px 2px rgba(16,24,40,0.05)
Hover: #6941C6 / Disabled: bg #D0D5DD text #667085

### Primary button (standard)
Height 44px, padding 10px 18px, bg #7F56D9, radius 8px, text #FFFFFF 14px 600

### Secondary button
Height 44px, bg #FFFFFF, border 1px #D0D5DD, radius 8px, text #344054 14px 600
Hover: bg #F9FAFB

### Ghost/text button
No bg, no border, text #6941C6 14px 600, hover bg #F9F5FF

### Input field
Height 44px, bg #FFFFFF, border 1px #D0D5DD, radius 8px, padding 10px 14px
Placeholder: 16px 400 #667085
Label above: 14px 500 #344054, 6px gap below label
Focus: border #7F56D9, shadow focus-ring
Error: border #F04438, helper text #D92D20 14px below
Helper text: 14px #667085, 6px below input

### Card (default)
bg #FFFFFF, border 1px #EAECF0, radius 16px, padding 24px
Shadow: card default

### Badge (pill)
Primary: bg #F4EBFF, text #6941C6, 12px 500, padding 2px 10px, radius 9999px
Gray: bg #F2F4F7, text #344054
Success: bg #ECFDF3, text #027A48
Error: bg #FEF3F2, text #B42318

### Progress bar
Track: 8px tall, bg #EAECF0, radius 9999px
Fill: bg #7F56D9, radius 9999px
Labels: 14px 500 #344054 above-left, 14px #667085 above-right

### Step indicator (dots)
Active: 8px circle, bg #7F56D9
Inactive: 8px circle, bg #EAECF0
Completed: 8px circle, bg #D6BBFB
Spacing: 8px between dots

### List row / tracker item — 4-zone layout (NEVER overlap zones)
Zone 1 — number badge (leftmost, 36-40px circle):
  Active: bg #7F56D9, number #FFFFFF 14px 600
  Inactive: bg #EAECF0, number #98A2B3 14px 600
  Contains ONLY the number — NO icon overlay

Zone 2 — icon block (8-12px right of Zone 1, 40x40px, radius 10px):
  Active: bg #F4EBFF, icon stroke #7F56D9, 20px Lucide path
  Inactive: bg #F2F4F7, icon stroke #98A2B3

Zone 3 — text (12px right of Zone 2):
  Title: 14px 600, #101828 (active) / #98A2B3 (inactive)
  Sub: 14px 400, #667085
  Meta: 12px 400, #98A2B3

Zone 4 — action (far right, vertically centered):
  Active: chevron-right, stroke #98A2B3
  Inactive: lock icon, stroke #D0D5DD

Row: height 72-88px, bg #FFFFFF (active) / #F9FAFB (inactive), border 1px #EAECF0, radius 12px
Connector between rows: dashed vertical line from bottom of Zone 1 to top of next, stroke #D0D5DD 1px dashed

### Upload / media zone
bg #F9FAFB, border 2px dashed #D0D5DD, radius 12px
Icon container: 56px, bg #F2F4F7, radius 12px, icon 32px stroke #98A2B3
Primary label: 16px 500 #344054, 12px below container
Sub label: 14px #667085

### Trust / security row
bg #F9FAFB, border 1px #EAECF0, radius 8px, height 44px, padding 0 16px
Left icon: lock or shield, 16px, stroke #667085
Text: 14px #475467

### Bottom tab bar (mobile)
Height 64px, bg #FFFFFF, border-top 1px #EAECF0
Active: icon #7F56D9, label 12px 600 #6941C6
Inactive: icon #98A2B3, label 12px 500 #667085

### Divider
1px solid #EAECF0

---

## Scope determines output format

SINGLE SCREEN: 4 different ways to design one screen. One full artboard per concept row.
WORKFLOW: 4 different ways to structure a multi-screen journey. 2-3 mini-screens per row with flow arrows.

## Divergence angles — one per concept, no repeats
Progressive / Minimal / Power user / Unconventional / Familiar / Hub and spoke

## Competitive directives — required
FOLLOW, CHALLENGE, BORROW from Skill 04 must each appear in at least one concept.

## Pre-generation thinking — required
For each concept before drawing:
1. Design hypothesis: "If [user] [belief], then [approach] will [outcome] because [reason]"
2. Psychological principle + how the layout expresses it
3. Exact friction this concept addresses
4. The bet this makes about the user that the other 3 don't
5. FOLLOW, CHALLENGE, or BORROW?

---

## SVG output specification

Single SVG file, all 4 concepts, via create_file.
Named: wireframes-[flow]-[date].svg

### Universal canvas — vertical stack (always)
4 concept rows stacked vertically. One concept per row.
Each row: notes panel (left, 220px) + screen(s) (right, 24px gap)
40px padding all sides. 56px gap between rows. 20px label above each row.

### Artboard sizes — exact values, no exceptions

MOBILE:   393 x 852px  (iPhone 14/15 standard viewport)
DESKTOP:  1440 x 900px (standard desktop viewport — always full size, never thumbnail)

Mobile mini (workflow):  222 x 480px  (56% of 393x852)
Desktop mini (workflow): 810 x 506px  (56% of 1440x900)

RESPONSIVE — when user selects responsive or both:
Generate BOTH a mobile AND a desktop artboard for each concept.
Each concept row contains: notes panel + mobile artboard + [gap] + desktop artboard
Label each artboard: "Mobile — 393×852" and "Desktop — 1440×900"
Canvas width must accommodate both artboards side by side.

### Canvas dimensions
Single screen mobile:
  Width = 40 + 240 + 28 + 393 + 40 = 741px
  Height = 40 + 4(20+852) + 3(56) + 40 = ~3,732px

Workflow mobile (2 mini per row):
  Width = 40 + 220 + 24 + 220 + 32 + 220 + 40 = 796px
  Height = 40 + 4(20+476) + 3(56) + 40 = ~2,200px

### Artboard
fill #FFFFFF (white — not grey), stroke #E2E2E2, stroke-width 1, rx 12 (full) / rx 6 (mini)

### Notes panel
bg #F9FAFB, border 1px #EAECF0, radius 10px, 16px internal padding
Content top to bottom — full text, never truncate, wrap with tspan:
1. Concept name: 12px 600 #101828
2. Angle pill: bg #F4EBFF, text #6941C6, 10px 600, radius 9999px
3. Framework: 10px #98A2B3 label + 10px 500 #344054 value
4. Job/Model: 10px #98A2B3 label + 10px #344054 value (wrap text)
5. Divider: 1px #EAECF0
6. Pattern: 10px #98A2B3 label + 10px 500 #344054 value (neutral, no colour coding)
7. Divider: 1px #EAECF0
8. Hypothesis: 9px italic #98A2B3 label + 9px #BBBBBB body (wrap text, full)



### Responsive — both mobile and desktop per concept

When platform = responsive, each concept row contains:
  [Notes panel 220px] + [24px gap] + [Mobile artboard 393x852] + [48px gap] + [Desktop artboard 1440x900]

Label above mobile artboard: "Mobile 393×852" — 9px, #98A2B3
Label above desktop artboard: "Desktop 1440×900" — 9px, #98A2B3

Canvas width = 40 + 220 + 24 + 393 + 48 + 1440 + 40 = 2205px
Canvas height = 40 + 4(20 + 900) + 3(56) + 40 = ~3,868px  (desktop drives row height)


### Notes panel — text overflow prevention (critical)

SVG does not auto-wrap text. Every text field in the notes panel MUST use tspan elements for wrapping.
The panel width is fixed at 220px with 16px internal padding on each side = 188px usable text width.

Rules to prevent overflow:
- Maximum ~26 characters per line at font-size 10px
- Maximum ~30 characters per line at font-size 9px
- Maximum ~22 characters per line at font-size 12px
- Every multi-word value MUST be split into lines using tspan dy="12" (or dy="11" for 9px text)
- The panel height MUST be calculated from actual content height, not assumed to equal screen height
- Panel height = sum of all text line heights + spacing + top/bottom padding (16px each)
- If calculated panel height < screen height, set panel height = screen height
- Never let a text element extend beyond x = (panel_left + panel_width - 16px)

Pattern field specifically — often the longest value:
- Split at natural break points: after the em-dash "—" or after FOLLOW/CHALLENGE/BORROW
- Example: "FOLLOW — step wizard" fits on one line
- Example: "CHALLENGE — removes account gate before first step" must split:
  Line 1: "CHALLENGE — removes"
  Line 2: "account gate before"
  Line 3: "first step"

Hypothesis field — always multi-line:
- Split every 28-30 characters at word boundaries
- Use dy="11" for 9px font
- Allow as many lines as needed — panel height expands to fit

### Flow arrows (workflow)
Stroke #D0D5DD, stroke-width 1.5, arrowhead: small filled triangle fill #D0D5DD
Vertically centered at 50% of screen height

### Concept label
"CONCEPT N" — 10px 600, fill #D0D5DD, letter-spacing 1, above notes panel left edge

### Icon usage
Lucide SVG paths (https://lucide.dev)
stroke-width 1.8, stroke-linecap round, stroke-linejoin round, fill none
Standard: stroke #667085 / Inactive: #98A2B3 / Brand/active: #7F56D9 / Emphasis: #344054

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
landmark:      M3 22V12M21 22V12M12 22V12M2 12l10-9 10 9M5 12v-2M19 12v-2

---

## Output format

CONCEPTS OVERVIEW
-----------------
Brief: [one-line]
Scope: [SINGLE SCREEN or WORKFLOW]
Design system: [Untitled UI / user system name]
Competitive insight: [dominant pattern + main gap]

1. [Name] — [angle] / [framework] / [FOLLOW or CHALLENGE or BORROW or original]
2-4: same

SVG file via create_file.
Skill 03 rationale immediately after.

---

## Rules
- Exactly 4 concepts
- All 4 use the same design system visually — white backgrounds, purple CTAs, Inter font
- Each concept uses a different divergence angle
- No repeated layout structures
- FOLLOW and CHALLENGE must each appear in at least one concept
- White artboard backgrounds (#FFFFFF)
- All text in SVG: full text, wrap with tspan, never truncate or use ellipsis

## Handoff
Skill 03 (always) / Skill 05 (when user selects final direction)