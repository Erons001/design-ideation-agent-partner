# Skill 01 — Context Ingestion

## Purpose
Extract a structured design brief from any input — a context document, free text, or a conversational interview. This brief is the foundation every other skill builds on. Output format is always identical regardless of input type.

## Input types
- Document-led: PRD, project brief, initiative doc, Starts With Why doc, or any strategic document
- Feature/flow-led: Free text describing a feature or flow without a document
- Problem-led: A problem statement without a specified solution direction
- No input: A vague prompt with minimal context

## The four signals
Always extract these four before proceeding:

1. Problem — What specific problem or friction is being addressed?
2. Users — Who are the primary users? What is their context and emotional state?
3. Success — What does a good outcome look like for the user?
4. Constraints — Platform, design system, business rules, technical limitations?

## Design scope classification — CRITICAL
Before outputting the brief, classify the design scope as either SINGLE SCREEN or WORKFLOW.

SINGLE SCREEN: The design involves one screen or interface in isolation.
Examples: empty state, settings page, profile screen, dashboard, search results, product detail page.

WORKFLOW: The design involves two or more connected screens that form a sequential or branching user journey.
Examples: checkout flow, sign up flow, onboarding, KYC verification, password reset, booking flow, payment flow.

The classification must appear in the brief. It changes how Skill 02 generates wireframes:
- Single screen: 4 concepts explore different layouts and interaction models for that one screen
- Workflow: 4 concepts explore different flow structures — how screens are sequenced, what is split vs combined, what gates what

If the scope is ambiguous, classify as WORKFLOW if two or more steps or states are implied.

## Behaviour rules

### Rule 1 — Extract silently from documents
If a document is provided, extract all four signals without asking questions. Only ask if a signal is genuinely absent.

### Rule 2 — Ask only essential questions when context is missing
When no document is provided, ask max 3 structured choice questions before proceeding. Infer everything else.

### Rule 3 — Platform must always be confirmed — never assumed

CRITICAL: Never default to mobile or assume a platform. Mobile is not the default. Desktop is not the default. There is no default — platform must always be confirmed with the user. If the user has not explicitly stated the platform, always ask before proceeding. This is a required question regardless of how much other context was provided.

Platform question (always ask if not stated):
"What platform are you designing for?"
- Mobile (iOS / Android) — 390 x 844px artboard
- Web — desktop (1440 x 900px artboard)
- Web — responsive (generate both mobile and desktop artboards)
- Cross-platform app — specify primary platform

If the user says "responsive" or "both", generate artboards for both mobile and desktop for each concept.

### Rule 4 — Essential questions (no-document path)

When no document is provided, ask these in order. Stop as soon as you have enough to proceed.

Q1 — What are you designing? (single-select)
- A new feature for an existing product
- A new product or flow from scratch
- A redesign of an existing flow
- Something else

Q2 — Who is the primary user? (single-select)
- General consumer
- Business buyer (B2B)
- Internal team / ops user
- Mixed audience

Q3 — What platform? (always ask — never assume)
- Mobile (iOS / Android)
- Web — desktop
- Web — responsive (mobile + desktop)
- Cross-platform

Q4 — Do you have a design system to use? (always ask — one question, no pressure)
- Yes — I'll share it now (Figma link, file, or paste the tokens/components)
- Yes — but I'll share it later
- No — proceed without one

If the user says yes and shares it: extract the key tokens and components immediately. See "Design system handling" section below.
If the user says yes but will share later: note it in the brief and proceed. They can share it at any point.
If the user says no: proceed without it. Never ask again.

### Rule 5 — Never generate wireframes on a vague brief
If the brief is too thin, ask one more focused question.

### Rule 6 — Always produce the structured brief before passing to the next skill
Output the brief and ask the user to confirm before proceeding.

## Structured brief output format

DESIGN BRIEF
------------
Problem:      [what is broken, slow, confusing, or missing]
Users:        [who they are, their context, comfort level]
Success:      [what changes for the user if this is done well]
Constraints:  [platform, design system, tech limits, business rules]
Flow scope:   [the specific screen or flow being ideated]
Platform:     [Mobile / Desktop / Responsive / Cross-platform — always confirmed with user, never assumed]
Screen size:  [390x844 for mobile | 1440x900 for desktop | both if responsive]
Scope type:   [SINGLE SCREEN or WORKFLOW]

## Document format handling

| Document type    | What to look for                                            |
|------------------|-------------------------------------------------------------|
| PRD              | Problem statement, user stories, acceptance criteria, scope |
| Project brief    | Goals, audience, success metrics, constraints               |
| Initiative doc   | Business motivation, user impact, scope boundaries          |
| Starts With Why  | Core purpose, who it serves, belief statements              |
| Free text        | Extract intent, infer platform and user type if not stated  |

## Design system handling

When a design system is provided — in any format — extract and store these signals:

| Signal | What to look for |
|---|---|
| Base spacing unit | e.g. 8px, 4px — the foundation of the grid |
| Colour tokens | Primary, secondary, neutral, semantic (error, success, warning) — token names not hex values |
| Typography scale | Heading sizes, body sizes, label sizes — token names and sizes |
| Component library | List of available components — Button variants, Input variants, Card types, Navigation patterns |
| Border radius | Default corner radius tokens |
| Shadow / elevation | If the system uses elevation or shadow tokens |
| Grid / layout | Column count, gutter, margin |
| Constraints | Anything the system explicitly restricts — e.g. "never use custom colours outside the palette" |

Accepted formats:
- Figma file link — extract styles and components via Figma context
- Pasted token JSON — parse key/value pairs
- Pasted markdown or text spec — extract the signals above
- Screenshot or image of a design system page — read what is visible
- Verbal description — e.g. "we use 8px base unit, Material Design components, our primary is blue"

After extracting, add to the brief:

DESIGN SYSTEM
-------------
Source:       [Figma / JSON / text / verbal / none]
Base unit:    [e.g. 8px]
Colours:      [token names — e.g. primary-500, neutral-100, error-600]
Typography:   [token names and sizes — e.g. heading-xl: 32px, body-md: 16px]
Components:   [available components relevant to this flow]
Grid:         [columns, gutter, margin]
Constraints:  [anything explicitly restricted by the system]

If no design system is provided, omit this section entirely from the brief.

## Handoff
Once the structured brief is confirmed, pass it to:
- Skill 04 (Competitive Analysis) — always runs first
- Skill 02 (Wireframe Generation) — after Skill 04 completes, receives full brief including design system context if provided
- Skill 05 (Post-Convergence Handoff) — receives design system context to produce precise implementation spec