# Orchestrator

## Purpose
The orchestrator is the decision layer of the Design Ideation Agent. It sequences the skills, manages conversation state, decides when to ask clarifying questions, and listens for signals that trigger the next phase.

## Orchestration flow

User input
    |
[Evaluate input completeness]
    | - if insufficient context
[Ask clarifying questions] - structured choices only, not open text
    |
[Skill 01 - Context Ingestion]
    |
[Show structured brief to user for confirmation]
    |
[Check: competitive analysis toggled?]
    |-- YES: [Skill 04 - Competitive Analysis] --> pass pattern library to Skill 02
    |-- NO:  proceed directly to Skill 02
    |
[Skill 02 - Wireframe Generation]
    |
[Skill 03 - Concept Rationale]
    |
[Present all concepts + rationale to user]
    |
[Listen for convergence signal]
    |
[Skill 05 - Post-Convergence Handoff]

## When to ask clarifying questions
Ask when:
- The input is too vague to extract the four signals (problem, users, success, constraints)
- Platform or user type is genuinely ambiguous
- Competitive analysis toggle status is unclear
- The user's convergence signal references multiple concepts

Do NOT ask when:
- A full document is provided - extract silently
- A signal can be reasonably inferred from context
- The question would not meaningfully change the output

Always use structured choices (single-select, multi-select) over open text.
Maximum 3 questions before proceeding to generation.

## Prompt types the agent handles

Document-led:
  User uploads or pastes a context document. Agent extracts brief silently and confirms it.
  Example: "Generate ideation concepts for this initiative doc"

Feature/flow-led:
  User describes a feature or flow in free text. Agent asks only essential missing questions.
  Example: "I need ideas for a mobile onboarding flow for a B2B SaaS product"

Problem-led:
  User describes a problem. Agent reframes via JTBD before generating.
  Example: "Users are dropping off before completing signup - I need ideas to fix this"

Too vague - requires one question before proceeding:
  Example: "Give me some wireframe ideas"
  Agent: "What feature or flow are you designing for?" [single-select with options + free text]

## State the orchestrator maintains
- Structured brief (from Skill 01)
- Competitive analysis toggle status
- Pattern library (from Skill 04, if run)
- Generated concepts list (from Skill 02)
- Selected concept (after user convergence)
- Full conversation history (injected on every API call)

## Mid-workflow clarification
The orchestrator can ask questions at any point - not just at the start. If Skill 02 identifies the brief is too thin to make concepts genuinely divergent, it surfaces one focused question before generating.

Always use structured choice widgets. Open text is reserved for the initial prompt only and the optional "add context" escape hatch on any question.

## Figma plugin behaviour
In the Figma plugin, all clarifying questions must be rendered as structured choice widgets - not open text fields. The plugin maintains the full conversation thread in state and injects it on every API call. This is what gives Claude continuity across the session.