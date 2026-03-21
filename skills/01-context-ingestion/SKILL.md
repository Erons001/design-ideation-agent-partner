# Skill 01 — Context Ingestion

## Purpose
Extract a structured design brief from any input — a context document, free text, or a conversational interview. This brief is the foundation every other skill builds on. Output format is always identical regardless of input type.

## Input types
- **Document-led**: PRD, project brief, initiative doc, Starts With Why doc, or any strategic document
- **Feature/flow-led**: Free text describing a feature or flow without a document
- **Problem-led**: A problem statement without a specified solution direction
- **No input**: A vague prompt with minimal context

## The four signals
Always extract these four — do not proceed to any other skill until all are resolved:

1. **Problem** — What specific problem or friction is being addressed?
2. **Users** — Who are the primary users? What is their context and emotional state?
3. **Success** — What does a good outcome look like for the user?
4. **Constraints** — Platform, design system, business rules, technical limitations?

## Behaviour rules

### Rule 1 — Extract silently from documents
If a document is provided, extract all four signals without asking questions. Only ask if a signal is genuinely absent or ambiguous.

### Rule 2 — Ask only essential questions when context is missing
When no document is provided, ask only what is essential to unblock generation. Infer everything else. Use structured choice questions (single-select or multi-select), not open text. Maximum 3 questions before proceeding.

### Rule 3 — Use the interview path when there is no document
If no document is provided, trigger the essential questions below. Stop as soon as you have enough to produce a grounded brief.

**Essential questions (no-document path):**

Q1 — What are you designing? (single-select + optional free text)
- A new feature for an existing product
- A new product or flow from scratch
- A redesign of an existing flow
- Something else (free text)

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
If the brief is too thin to produce grounded concepts, ask one more focused question rather than generating generic ideas.

### Rule 5 — Always produce the structured brief before passing to the next skill
Output the brief in the format below. Make it visible to the user so they can correct it before generation begins.

## Structured brief output format

```
DESIGN BRIEF
------------
Problem:      [What is broken, slow, confusing, or missing]
Users:        [Who they are, their context, comfort level]
Success:      [What changes for the user if this is done well]
Constraints:  [Platform, design system, tech limits, business rules]
Flow scope:   [The specific screen or flow being ideated]
```

## Document format handling

This skill must handle any of these document types without asking the user what type it is:

| Document type       | What to look for                                              |
|---------------------|---------------------------------------------------------------|
| PRD                 | Problem statement, user stories, acceptance criteria, scope   |
| Project brief       | Goals, audience, success metrics, constraints                 |
| Initiative doc      | Business motivation, user impact, scope boundaries            |
| Starts With Why     | Core purpose, who it serves, belief statements                |
| Free text           | Extract intent, infer platform and user type if not stated    |

## Handoff
Once the structured brief is confirmed, pass it to:
- Skill 02 (Wireframe Generation) — always
- Skill 04 (Competitive Analysis) — only if toggle is on
