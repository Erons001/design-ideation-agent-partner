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

### Rule 3 — Essential questions (no-document path)

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

Q3 — What platform? (multi-select)
- Mobile (iOS / Android)
- Web (desktop)
- Web (responsive)
- Cross-platform

### Rule 4 — Never generate wireframes on a vague brief
If the brief is too thin, ask one more focused question.

### Rule 5 — Always produce the structured brief before passing to the next skill
Output the brief and ask the user to confirm before proceeding.

## Structured brief output format

DESIGN BRIEF
------------
Problem:      [what is broken, slow, confusing, or missing]
Users:        [who they are, their context, comfort level]
Success:      [what changes for the user if this is done well]
Constraints:  [platform, design system, tech limits, business rules]
Flow scope:   [the specific screen or flow being ideated]
Screen size:  [e.g. 390x844 mobile, 1440x900 desktop]
Scope type:   [SINGLE SCREEN or WORKFLOW]

## Document format handling

| Document type    | What to look for                                            |
|------------------|-------------------------------------------------------------|
| PRD              | Problem statement, user stories, acceptance criteria, scope |
| Project brief    | Goals, audience, success metrics, constraints               |
| Initiative doc   | Business motivation, user impact, scope boundaries          |
| Starts With Why  | Core purpose, who it serves, belief statements              |
| Free text        | Extract intent, infer platform and user type if not stated  |

## Handoff
Once the structured brief is confirmed, pass it to:
- Skill 04 (Competitive Analysis) — always runs first
- Skill 02 (Wireframe Generation) — after Skill 04 completes