# Design Ideation Agent Partner

An AI-powered design ideation agent that helps designers, PMs, and teams generate divergent high-fidelity wireframe concepts grounded in JTBD, mental models, and design systems.

## Why this exists

Ideation takes too long. The quality of design output is directly tied to the depth and breadth of the ideation process. This agent helps designers generate more ideas faster while staying grounded in problem context, user needs, JTBD, and design systems.

## What it does

Give it any design context — a PRD, project brief, problem statement, or description. It will:

1. Extract a structured design brief and confirm platform
2. Ask about your design system (Figma link, .md file, or use Untitled UI as default)
3. Run competitive analysis automatically (no toggle needed)
4. Generate exactly 4 divergent high-fidelity wireframe concepts as a downloadable SVG
5. Deliver full rationale per concept (hypothesis, bet, scenario, trade-off, validation question)
6. Produce a complete design handoff package when you pick a direction

## What high-fidelity means

All concepts use the same design system — either yours or Untitled UI by default. Concepts use real colours, real typography, real component shapes. They look like a finished design direction, not grey blocks. The divergence is in layout structure and UX direction, not visual style.

---

## How to use it

### Option 1 — Claude Project (recommended, no code required)

1. Go to claude.ai and sign in
2. Click Projects in the left sidebar
3. Click New project
4. Open docs/PROJECT-INSTRUCTIONS.md in this repo
5. Copy the full contents
6. In your project, click + next to Instructions and paste
7. Save — the agent is active in every conversation in the project

Start a conversation:

With a document: "Here's our PRD — generate ideation concepts for the checkout flow"
With a description: "I need ideas for a mobile onboarding flow for a B2B SaaS product"
With a problem: "Users are dropping off during KYC verification. I need wireframe concepts."

Wireframes are delivered as a single SVG file you can download and open in Figma.

---

### Option 2 — Clone and customise

git clone https://github.com/Erons001/design-ideation-agent-partner
cd design-ideation-agent-partner
code .

Customise any SKILL.md file to change agent behaviour, then set up your Claude Project.

---

### Option 3 — Use individual skills

Each SKILL.md is a standalone system prompt. Copy any skill and inject as a system message in your own API calls or tools.

---

## Input types

| Type | Example |
|---|---|
| Document-led | Paste PRD, brief, initiative doc, Starts With Why |
| Feature/flow-led | "I need ideas for a mobile checkout flow" |
| Problem-led | "Users drop off during KYC — I need concepts to fix this" |

---

## The 5 skills

| # | Skill | What it does |
|---|---|---|
| 01 | Context Ingestion | Extracts brief, classifies scope, confirms platform, asks about design system |
| 02 | Wireframe Generation | Generates exactly 4 high-fi concepts using your design system or Untitled UI |
| 03 | Concept Rationale | Deep rationale with hypothesis, bet, scenario, validation question, trade-off |
| 04 | Competitive Analysis | Always runs — researches competitors, outputs FOLLOW/CHALLENGE/BORROW directives |
| 05 | Post-Convergence Handoff | Design principles + full spec mapped to your design system tokens |

---

## Default design system — Untitled UI

When no design system is provided, all wireframes use Untitled UI:
- Primary: #7F56D9 (buttons, active states, links)
- Font: Inter
- Base unit: 4px
- Card radius: 16px, Input/Button radius: 8px

Untitled UI community file: https://www.figma.com/community/file/1020079203222914671

---

## Design system sharing

To use your own design system, share one of:
- A Figma file link — the agent reads your tokens, styles, and components directly
- A .md or .txt file — paste your token values and component specs

---

## Repository structure

design-ideation-agent-partner/
  skills/
    01-context-ingestion/SKILL.md
    02-wireframe-generation/SKILL.md
    03-concept-rationale/SKILL.md
    04-competitive-analysis/SKILL.md
    05-post-convergence-handoff/SKILL.md
  docs/
    ARCHITECTURE.md
    PROJECT-INSTRUCTIONS.md
  orchestrator/
    ORCHESTRATOR.md
  README.md

---

## Cost

- Hosting: free (Vercel or Claude.ai)
- Claude account: free tier available, Pro recommended
- API usage: ~$0.03 per full session when using the API