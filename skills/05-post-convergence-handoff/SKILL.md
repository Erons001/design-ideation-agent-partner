# Skill 05 — Post-Convergence Handoff

## Purpose
When the designer selects a final concept, generate a complete handoff package for hi-fi execution. Serves the designer moving to hi-fi and the broader team (PM, developer, stakeholders).

## Trigger
- "I want to go with concept [N]"
- "Let's develop [concept name]"
- "This one"
If user combines elements, ask one clarifying question to establish primary direction first.

## Output

### Part 1 — Design Principles (3-5)
Named principles specific to THIS product and THIS user. Not generic platitudes.

Format: "[Principle name] — [what this means in practice]: do [X], not [Y]."

Example:
Bad: "Progressive disclosure — reveal information gradually."
Good: "Disclose before you ask — show the legal reason for each data request before the input field appears. Do not ask for data without first stating why. This user associates unsolicited data requests with fraud risk."

Rules:
- Must connect to the brief or chosen concept rationale
- Must be actionable — state what to do and what NOT to do
- Must be specific to this product and user
- 3-5 only — fewer is too thin, more is noise

---

### Part 2 — Design Spec

#### WITH USER-PROVIDED DESIGN SYSTEM — precise implementation spec

Map directly to actual tokens. Never invent token names.
Flag explicitly any UI element the wireframe needs that the system does not cover.

TYPOGRAPHY
- Map every text role to a token: [token name] — [size, weight, colour]
- Flag any text role without a token

SPACING AND GRID
- Base unit, grid columns/gutter/margin, component padding, section spacing — all from tokens

INTERACTION STATES (for each interactive element)
Default / Hover / Focus / Active / Error / Empty state / Disabled
Reference design system component variants. Flag any state the system does not provide.

COMPONENT SUGGESTIONS
- [Component name from library]: [variant, configuration]
- Flag: [UI element with no existing component — needs custom design]

ACCESSIBILITY
- Verify specific token pairs meet WCAG AA (4.5:1 body, 3:1 large/UI)
- Focus order, ARIA labels, touch targets, motion considerations

MOTION AND TRANSITIONS
- Reference design system motion tokens if they exist
- Page transitions, component animations, loading states, motion principle

---

#### WITH UNTITLED UI DEFAULT — Untitled UI implementation spec

TYPOGRAPHY — Untitled UI / Inter
- Screen titles:   24px / 700 / #101828
- Section heads:   20px / 600 / #101828
- Card titles:     16px / 600 / #101828
- Body:            16px / 400 / #475467
- Input labels:    14px / 500 / #344054
- Captions:        14px / 400 / #667085
- Button labels:   14px / 600 / #FFFFFF (primary) or #344054 (secondary)
- Badges:          12px / 500

SPACING — Untitled UI (4px base)
Mobile: 16px screen edges, 16-20px element gaps, 32-48px section gaps
Desktop: 40px screen edges, 1280px max content width, 24-32px element gaps
Input height: 44px, Button height: 44px standard / 48px mobile full-width
Card padding: 24px, Input padding: 10px 14px, Button padding: 10px 18px

INTERACTION STATES — Untitled UI
Primary button: default #7F56D9 / hover #6941C6 / disabled bg #D0D5DD text #667085
Secondary button: default bg #FFFFFF border #D0D5DD / hover bg #F9FAFB
Input: default border #D0D5DD / focus border #7F56D9 shadow 0 0 0 4px rgba(159,122,237,0.24) / error border #F04438
For each interactive element in the wireframe: Default / Hover / Focus / Active / Error / Empty / Disabled

COMPONENT SUGGESTIONS — Untitled UI
- Button/Primary, Button/Secondary, Button/Ghost
- Input/Default, Input/Destructive, Textarea/Default
- Card/Default, Card/Feature (top accent)
- Badge/Primary (#F4EBFF/#6941C6), Badge/Gray, Badge/Success, Badge/Error, Badge/Warning
- Avatar XS–2XL
- Progress Bar, Step Indicator
- Top Nav, Bottom Tab Bar
- Modal/Default, Drawer/Bottom
Flag any UI element not in Untitled UI — needs custom design.

ACCESSIBILITY — Untitled UI
- gray-900 on white, gray-700 on gray-50: both pass WCAG AA
- #7F56D9 on white: passes 4.5:1
- Always show focus ring: 0 0 0 4px rgba(159,122,237,0.24)
- Touch targets minimum 44x44px
- Follow prefers-reduced-motion — provide non-animated fallbacks

MOTION — Untitled UI
- Page transitions: 200ms ease-out, opacity + translateY(8px) to 0
- Component appear: 150ms ease, opacity + scale(0.98) to 1
- Hover states: 100ms ease
- Loading: skeleton screens matching Untitled UI card shapes
- Motion principle: [derive from chosen concept rationale]

---

## Rules
- Principles must connect to brief and chosen concept rationale
- With user's system: map to actual tokens, flag all gaps
- With Untitled UI: map to Untitled UI tokens by name
- Principles readable by PM/stakeholder without design background
- Spec for designer and developer — appropriate language for each
- Never invent token names not in the provided system

## Handoff
Final output. Designer proceeds to hi-fi in Figma.