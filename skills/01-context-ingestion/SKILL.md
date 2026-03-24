# Skill 01 — Context Ingestion

## Purpose
Extract a structured design brief from any input. Classify scope. Confirm platform. Ask about design system. This brief is the foundation every other skill builds on.

## The four signals
1. Problem — what is broken, slow, confusing, or missing?
2. Users — who are they, context, emotional state?
3. Success — what changes for the user if done well?
4. Constraints — platform, design system, tech limits, business rules?

## Scope classification

SINGLE SCREEN if all true: one screen in isolation, no sequential progression, brief mentions page/screen/dashboard/empty state/settings/profile.
WORKFLOW if any true: sequence of steps, collects info across screens, defined start/end state, brief mentions flow/journey/steps/onboarding/checkout/sign up/verification/booking/payment/reset.
When in doubt: WORKFLOW.
Classification goes in brief output. Determines how Skill 02 generates wireframes.

## Platform rule — always ask, never assume
CRITICAL: No default platform. Ask every time if not stated:
"What platform are you designing for?"
- Mobile (iOS / Android) — 390 x 844px
- Web — desktop (1440 x 900px)
- Web — responsive (both)
- Cross-platform — specify primary

## Design system question — ask once, never again
After platform is confirmed:
"Do you have a design system?
- Yes — share a Figma link (https://figma.com/file/...) and I will read your tokens and components directly
- Yes — share a .md or .txt file with your tokens and specs
- No — I will use Untitled UI as the default design system
- I will decide later — I will use Untitled UI for now"

If No or later: use Untitled UI automatically, no further questions.
If Figma link: extract colours, typography, components, spacing from the file.
If .md/.txt file: extract tokens and component specs.
Never ask about design system more than once.

## Behaviour rules

### Rule 1 — Extract silently from documents
If a document is provided, extract all four signals without asking. Only ask if a signal is genuinely absent.

### Rule 2 — Essential questions when no document
Ask max 3 structured choice questions. Infer everything else.

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

### Rule 3 — Never generate on a vague brief
If brief is too thin, ask one more focused question.

### Rule 4 — Always output brief and confirm before proceeding

## Structured brief output format

DESIGN BRIEF
------------
Problem:        [what is broken or missing]
Users:          [who they are, context, comfort level]
Success:        [what changes if done well]
Constraints:    [platform, design system, limits]
Flow scope:     [specific screen or flow]
Platform:       [Mobile / Desktop / Responsive — confirmed with user, never assumed]
Screen size:    [390x844 mobile | 1440x900 desktop | both if responsive]
Scope type:     [SINGLE SCREEN or WORKFLOW]
Design system:  [Untitled UI (default) | user's system name + source]

DESIGN SYSTEM (if provided)
----------------------------
Source:       [Figma link / .md file / Untitled UI default]
Font:         [Font family]
Base unit:    [e.g. 4px]
Primary:      [Main brand colour token and hex]
Neutrals:     [Key grey token names and hex values]
Radius:       [Default border radius tokens]
Shadows:      [Key shadow tokens]
Components:   [Available components relevant to this flow]

If using Untitled UI, auto-populate from built-in Untitled UI token specification.

## Document formats handled
PRD / project brief / initiative doc / Starts With Why / free text — extract the four signals from any of these without asking the user what type it is.

## Handoff
Confirmed brief passes to:
- Skill 04 (Competitive Analysis) — always runs first
- Skill 02 (Wireframe Generation) — after Skill 04, receives full brief + design system
- Skill 05 (Post-Convergence Handoff) — receives design system for precise spec