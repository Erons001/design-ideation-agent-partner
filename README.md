# Design Ideation Agent Partner

An AI-powered design ideation agent that helps designers, PMs, and teams generate divergent low-fi wireframe concepts grounded in JTBD, mental models, and design systems.

## Why this exists

Ideation takes too long. The quality of design output is directly tied to the depth and breadth of the ideation process - more ideas, explored more thoroughly, lead to better outcomes. This agent helps designers generate more ideas faster while staying grounded in problem context, user needs, JTBD, and design systems.

## What it does

Takes any design context as input and produces:
- 4-6 divergent low-fi wireframe concepts, each with a distinct UI and UX direction
- Full rationale per concept (framework applied, key decisions, trade-offs, best fit)
- A complete design handoff package when the designer converges on a direction

## The 5 skills

| # | Skill | Purpose |
|---|---|---|
| 01 | Context Ingestion | Extracts a structured brief from any document or free text |
| 02 | Wireframe Generation | Generates 4-6 divergent low-fi concepts grounded in JTBD or mental models |
| 03 | Concept Rationale | Named, traceable rationale per concept |
| 04 | Competitive Analysis | Optional - researches competitor patterns to inform ideation |
| 05 | Post-Convergence Handoff | Named design principles + full spec when direction is chosen |

## Input types

- Document-led: Upload or paste any context document (PRD, project brief, initiative doc, Starts With Why, or any strategic doc)
- Feature/flow-led: Describe a feature or flow in free text
- Problem-led: Describe a problem - the agent reframes via JTBD before generating

## Output surfaces

- Claude.ai artifact - Rendered HTML wireframes in a conversational interface
- Figma plugin - Wireframes inside Figma with structured Q&A and export to hi-fi frames

## UX frameworks applied

- Jobs To Be Done (JTBD): What job is the user hiring this feature to do?
- Mental model alignment: What does the user already expect this to behave like?

## Repository structure

design-ideation-agent-partner/
  skills/
    01-context-ingestion/SKILL.md
    02-wireframe-generation/SKILL.md
    03-concept-rationale/SKILL.md
    04-competitive-analysis/SKILL.md
    05-post-convergence-handoff/SKILL.md
  orchestrator/
    ORCHESTRATOR.md
  docs/
    ARCHITECTURE.md
  README.md

## Claude Project
This agent lives in a Claude Project at claude.ai. The project system prompt contains the full orchestration context so every conversation has complete awareness of all 5 skills, input types, frameworks, and build decisions.

## GitHub repo
https://github.com/Erons001/design-ideation-agent-partner