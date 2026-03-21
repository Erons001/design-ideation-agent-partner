# Skill 05 - Post-Convergence Handoff

## Purpose
When the designer selects a final concept direction, generate a handoff package that bridges the low-fi concept to hi-fi execution. Serves two audiences simultaneously: the designer moving into hi-fi, and the broader team (PM, developer, stakeholders) who need to understand what was decided and why.

## Trigger
Activates when the user signals convergence:
- "I want to go with concept [N]"
- "Let's develop [concept name]"
- "This one - [description]"

If the user combines elements from multiple concepts, ask one clarifying question to establish the primary direction before proceeding.

## Output

### Part 1 - Design principles
Named principles derived from the chosen concept and the structured brief.

Format:
DESIGN PRINCIPLES - [Concept name]
1. [Principle name]: [One-line explanation of what this means in practice]
2. [Principle name]: [One-line explanation]
3. [Principle name]: [One-line explanation]
4. [Principle name]: [One-line explanation]

Aim for 3-5 principles. They must be specific to this concept - not generic design platitudes.
"Progressive disclosure" is not a principle unless you explain what it means for THIS product and THIS user.

### Part 2 - Design spec

#### Typography scale and hierarchy
- Primary heading: size, weight, usage context
- Secondary heading: size, weight, usage context
- Body text: size, weight, line height
- Labels and captions: size, weight
- Interactive text (buttons, links): size, weight, treatment

#### Spacing and layout grid
- Base unit (e.g. 8px)
- Column grid: number of columns, gutter, margin
- Key spacing values: component padding, section spacing, element gaps
- Any layout constraints from the brief (e.g. mobile single-column)

#### Interaction states
For every interactive element identified in the wireframe:
- Default
- Hover
- Focus (keyboard)
- Active / pressed
- Error
- Empty / zero state
- Disabled (if applicable)

#### Component suggestions
Based on the wireframe layout:
- Component name
- Variant notes (e.g. "button - primary, secondary, destructive")
- Complexity flags (e.g. "this input likely needs inline validation")

#### Accessibility considerations
- Minimum contrast ratios to maintain
- Focus order recommendation
- ARIA labels needed for non-obvious interactive elements
- Motion considerations (reduced motion alternatives)
- Touch target minimums if mobile

#### Motion and transition guidance
- Page/screen transitions: type and duration
- Component-level transitions: which elements animate, how, and why
- Loading states: skeleton screens vs spinners vs progressive load
- Motion principle: what should motion communicate in this product?

## Rules
- Every design principle must connect to the structured brief or chosen concept rationale
- Specs are directional, not prescriptive - frame as recommended direction unless brief has hard constraints
- If a design system was provided in Skill 01, reference it in component suggestions and spacing values
- Principles section must be readable by a PM or stakeholder
- Spec section is for the designer and developer - use appropriate language for each

## Handoff
This is the final output of the agent workflow. After this, the designer proceeds to hi-fi in Figma.