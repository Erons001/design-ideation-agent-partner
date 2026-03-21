# Skill 02 - Wireframe Generation

## Purpose
Generate 4-6 divergent low-fi wireframe concepts from the structured brief produced by Skill 01. Every concept must cover both a UI direction (layout, structure, hierarchy) and a UX direction (interaction model, flow, mental model). Concepts must represent genuinely different approaches - not variations of the same layout.

## Core principle
Every concept must trace back to:
- The structured brief (problem, users, success, constraints)
- A named UX framework: JTBD or mental model alignment
- An identifiable design pattern or convention

Random or generic layouts are not acceptable output.

## Divergence strategy
Before generating, assign each concept one distinct angle:

| Angle | Question to answer |
|---|---|
| Progressive | What if the user is guided step by step? |
| Minimal | What is the absolute least we can show? |
| Power user | What if the user wants everything upfront? |
| Unconventional | What would a non-obvious interaction model look like? |
| Mobile-first | What if constraints forced radical simplification? |
| Familiar | What mental model does the user already have? |

Each concept takes ONE angle. Do not blend angles within a single concept.

## JTBD framing
Before generating, answer: "What job is the user hiring this feature to do?"
- The job is the progress the user is trying to make, not the feature itself
- Each concept answers the same job differently
- Example: For checkout, the job is "complete this quickly without second-guessing myself." One concept addresses this via radical reduction, another via trust signals, another via saved defaults.

## Mental model alignment framing
Before generating, answer: "What does the user already know that this should feel like?"
- Map each concept to a different reference model the user already carries
- Example: For onboarding - one concept feels like a setup wizard, another like a welcome letter, another like a product tour

## Low-fi wireframe format
Render each wireframe in plain HTML using only:
- Grey-filled rectangles for containers, cards, image placeholders
- Single-weight lines for dividers and borders
- Bold text for headings, regular weight for labels and body copy
- Labelled placeholder blocks for content areas
- Simple arrows or dotted lines for flow indicators
- NO colour beyond grey, NO icons, NO imagery, NO decorative styling

Every wireframe must include:
1. A screen title or flow label
2. Clear layout hierarchy (primary, secondary, tertiary zones)
3. Labelled interactive elements (buttons, inputs, links)
4. If multi-step: show 2-3 key steps with numbered progression indicators

## Output format per concept

CONCEPT [N] - [Name]
UX Framework:  [JTBD / Mental model alignment]
UI Direction:  [One-line description of layout approach]
UX Direction:  [One-line description of interaction/flow approach]
Job / Model:   [The specific job addressed OR the mental model mapped to]

[Low-fi wireframe HTML follows]

## Rules
- Generate exactly 4-6 concepts
- Each concept uses a different divergence angle
- No repeated layout structures across concepts
- If Skill 04 ran: at least one concept must deliberately diverge from the dominant competitive pattern found
- Always show the structured brief summary above all concepts so the user can verify grounding

## Handoff
Pass selected concept and metadata to:
- Skill 03 (Concept Rationale) - always
- Skill 05 (Post-Convergence Handoff) - when user selects final direction