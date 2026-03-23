# Skill 05 — Post-Convergence Handoff

## Purpose
When the designer selects a final concept direction, generate a handoff package that bridges the low-fi concept to hi-fi execution. Serves two audiences: the designer moving into hi-fi, and the broader team (PM, developer, stakeholders) who need to understand what was decided and why.

## Trigger
Activates when the user signals convergence:
- "I want to go with concept [N]"
- "Let's develop [concept name]"
- "This one — [description]"

If the user combines elements from multiple concepts, ask one clarifying question to establish the primary direction before proceeding.

---

## Output

### Part 1 — Design Principles

3-5 named principles (see quality rules below) derived from the chosen concept and the structured brief. Each principle has a name and a single-line explanation specific to this product and this user — not generic platitudes.

Format:
DESIGN PRINCIPLES — [Concept name]
1. [Principle name]: [What this means in practice for THIS product and THIS user]
2. [Principle name]: [Explanation]
3. [Principle name]: [Explanation]

"Progressive disclosure" is not a principle unless you explain what it means for this specific product and user. "Trust before commitment" IS a principle if you explain: "Show the regulatory reason for each data request before asking for it — users in this context associate data sharing with risk."

---

### Part 2 — Design Spec

The spec has two modes depending on whether a design system was provided in Skill 01.

---

IF A DESIGN SYSTEM WAS PROVIDED — produce a precise implementation spec that maps directly to the system:

TYPOGRAPHY
Map directly to design system tokens — do not invent sizes or weights.
- Screen titles: use [token name] — [size, weight]
- Section headings: use [token name] — [size, weight]
- Body copy: use [token name] — [size, line-height]
- Labels and captions: use [token name] — [size]
- Button labels: use [token name] — [size, weight]
- Flag any text role the design system does not have a token for — needs custom design

SPACING AND LAYOUT GRID
Map directly to design system spacing tokens and grid.
- Base unit: [from design system — e.g. 8px]
- Grid: [columns, gutter, margin — from design system]
- Component internal padding: [token — e.g. space-4 = 32px]
- Section spacing: [token — e.g. space-6 = 48px]
- Element gaps: [token]

INTERACTION STATES
For each interactive element in the wireframe:
Default / Hover / Focus (keyboard) / Active / Error / Empty state / Disabled
Reference design system component variants where they exist — e.g. "Button/Primary/Disabled"
Flag any state the design system does not provide — needs custom design

COMPONENT SUGGESTIONS
Reference actual components from the design system library by name.
- [Component name from library]: [which variant, any configuration notes]
- [Component name]: [variant, notes]
Flag — [any UI element in the wireframe that has no existing component — needs to be built]

ACCESSIBILITY
- Colour contrast: verify [specific token pairs from the design system] meet WCAG AA
- Focus order: [recommended tab sequence for this screen or flow]
- ARIA labels: [specific elements that need labels — non-obvious interactive elements]
- Touch targets: [flag any component that may be below 44px on mobile]
- Motion: [note if design system has reduced-motion preference — if not, recommend one]

MOTION AND TRANSITIONS
- Page/screen transitions: [type and duration — reference design system motion tokens if they exist]
- Component animations: [which elements animate, how, duration]
- Loading states: [skeleton vs spinner — reference design system patterns if available]
- Motion principle: [what motion should communicate in this product]

---

IF NO DESIGN SYSTEM WAS PROVIDED — produce directional guidance the designer can use as a starting point:

TYPOGRAPHY
- Primary heading: [recommended size and weight]
- Secondary heading: [recommended size and weight]
- Body: [recommended size, weight, line-height]
- Labels/captions: [recommended size, weight]
- Interactive text: [recommended size, weight, treatment]
- Recommendation: establish a type scale before moving to hi-fi

SPACING AND LAYOUT GRID
- Recommended base unit: 8px
- Grid: [columns, gutter, margin for the target platform]
- Component padding: [recommended values]
- Section spacing: [recommended values]
- Recommendation: define spacing tokens before developer handoff

INTERACTION STATES
For each interactive element: Default / Hover / Focus / Active / Error / Empty state / Disabled
Recommendation: document all states before developer handoff — missing states cause implementation gaps

COMPONENT SUGGESTIONS
- [Component name]: [variants needed, complexity notes]
- [Component name]: [notes]
- Recommendation: define these as reusable components in a design system before handoff

ACCESSIBILITY
- Minimum contrast: 4.5:1 for body text, 3:1 for large text and UI components (WCAG AA)
- Focus order: [recommended tab sequence]
- ARIA labels: [specific elements that need labels]
- Touch targets: minimum 44x44px on mobile
- Motion: offer reduced-motion alternatives for all animations

MOTION AND TRANSITIONS
- Page transitions: [type and duration]
- Component animations: [which elements, how, duration]
- Loading states: [skeleton screens vs spinners — recommendation]
- Motion principle: [what motion should communicate in this product]

---

## Rules

- Every design principle must connect to the structured brief or the chosen concept rationale
- With a design system: spec must reference actual tokens and component names — never invent values
- With a design system: explicitly flag any UI element or state the system does not cover — these are gaps the designer must fill before developer handoff
- Without a design system: specs are directional recommendations, not fixed rules
- Principles section must be readable by a PM or stakeholder without design background
- Spec section is for the designer and developer — language should be appropriate for each
- Never invent token names that were not in the provided design system

## Handoff
This is the final output of the agent workflow. After this, the designer proceeds to hi-fi in Figma.
## Design principle quality rules

### Principles must be specific to this product and this user
Bad: "Progressive disclosure — reveal information gradually."
Good: "Disclose before you ask — show the legal reason for each data request before the input field appears. This user associates unsolicited data requests with fraud risk."

Bad: "Trust signals — build user confidence."
Good: "Anchor every step with evidence — place a regulation badge and encryption note at the top of each verification screen. This user has low baseline trust in fintech apps."

### Each principle must be actionable
A designer reading the principle should know what to do and what not to do.
Format: "[Principle name] — [what this means in practice]: [do this], not [do that]."

### Principles must connect to the chosen concept's rationale
Every principle should be traceable to either:
- The design hypothesis of the chosen concept
- The job or mental model the concept addresses
- A specific friction the concept was designed to resolve

### Aim for 3-5 principles
Fewer than 3 is too thin — the designer doesn't have enough guidance.
More than 5 is noise — the designer can't hold them all in mind while designing.

