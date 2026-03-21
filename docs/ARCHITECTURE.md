# Architecture

## Overview
The Design Ideation Agent Partner is an orchestrated AI agent with 5 skills. It takes any design context as input and produces divergent low-fi wireframe concepts with full rationale, followed by a design handoff package when the designer converges on a direction.

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

## How skills work at runtime
Skills are markdown prompt files. At runtime, the relevant skill prompt is injected as a system message into each Anthropic API call. Claude has no persistent memory between calls - the skill is always injected fresh.

Flow:
  User input
    --> Agent reads relevant SKILL.md
    --> API call: system = SKILL.md content, messages = conversation history
    --> Claude responds according to skill instructions
    --> Output passed to next skill as context in next API call

## Output surfaces

Figma plugin:
- Conversational panel with structured choice widgets for Q&A
- Low-fi wireframe concepts rendered inside the plugin
- Full conversation thread maintained in plugin state
- Export to Figma frames for hi-fi development

Claude.ai artifact:
- Rendered HTML wireframes in a conversational interface
- Full orchestration loop runs inside the artifact
- Conversation history maintained in artifact state

## Data flow between skills

Raw input (any format)
  --> Skill 01 --> Structured brief
  --> Skill 04 --> Pattern library (optional, if toggled)
  --> Skill 02 --> 4-6 low-fi wireframe concepts
  --> Skill 03 --> Rationale per concept
  --> [User selects direction]
  --> Skill 05 --> Design principles + full design spec

## Persistence
By default nothing persists between sessions. All state lives in the conversation thread, which is passed as context on every API call.

For the Figma plugin, session state can be stored using Figma plugin storage API (key-value, scoped to plugin and user).

## UX frameworks applied
- Jobs To Be Done (JTBD): What job is the user hiring this feature to do?
- Mental model alignment: What does the user already expect this to behave like?

Both are applied in Skill 02 and Skill 03. Every generated concept is anchored to one of these frameworks.

## Build order
1. Skill 01 - Context Ingestion (all other skills depend on its output)
2. Skill 02 - Wireframe Generation
3. Skill 03 - Concept Rationale
4. Skill 04 - Competitive Analysis (optional)
5. Skill 05 - Post-Convergence Handoff