# Design Ideation Agent Partner

An AI-powered design ideation agent that helps designers, PMs, and teams generate divergent low-fi wireframe concepts grounded in JTBD, mental models, and design systems.

## Why this exists

Ideation takes too long. The quality of design output is directly tied to the depth and breadth of the ideation process — more ideas, explored more thoroughly, lead to better outcomes. This agent helps designers generate more ideas faster while staying grounded in problem context, user needs, JTBD, and design systems.

## What it does

Give it any design context — a PRD, a project brief, a problem statement, or just a description of what you're building. It will:

1. Extract a structured design brief from your input
2. Optionally research competitor patterns
3. Generate 4-6 divergent low-fi wireframe concepts as a downloadable SVG file
4. Provide full rationale per concept (framework, key decisions, trade-offs, best fit)
5. Deliver a complete design handoff package when you pick a direction

---

## How to use it

### Option 1 — Claude Project (recommended, no code required)

The fastest way. Works in any Claude conversation.

**You need:** A Claude account (free or Pro)

**Steps:**

1. Go to [claude.ai](https://claude.ai) and sign in
2. Click the Projects icon in the left sidebar
3. Click **New project** and give it a name (e.g. "Design Ideation Agent")
4. Open [docs/PROJECT-INSTRUCTIONS.md](./docs/PROJECT-INSTRUCTIONS.md) in this repo
5. Copy the full contents of that file
6. In your new project, click **+** next to Instructions and paste the copied text
7. Save — the agent is now active

**To run a session:**

Start a new conversation inside the project and type any of these:

```
# With a document
"Here's our PRD — generate ideation concepts for the checkout flow"

# With a description
"I need ideas for a mobile onboarding flow for a B2B SaaS product"

# With a problem
"Users are dropping off before completing KYC verification. I need wireframe concepts to fix this"
```

The agent will guide you from there. Wireframes are delivered as a single SVG file you can download and open in Figma.

---

### Option 2 — Clone and customise

For teams who want to adapt the agent to their own design system, frameworks, or workflow.

**You need:** Git, a text editor, a Claude account

**Steps:**

```bash
# 1. Clone the repo
git clone https://github.com/Erons001/design-ideation-agent-partner

# 2. Open in your editor
cd design-ideation-agent-partner
code .
```

**To customise:**
- Edit any file in `skills/` to change agent behaviour
- `skills/01-context-ingestion/SKILL.md` — change what questions are asked
- `skills/02-wireframe-generation/SKILL.md` — change wireframe format, icon library, or palette
- `skills/03-concept-rationale/SKILL.md` — change rationale structure
- `skills/05-post-convergence-handoff/SKILL.md` — change what the design spec covers

Then follow Option 1 to set up your Claude Project using your customised `docs/PROJECT-INSTRUCTIONS.md`.

---

### Option 3 — Use individual skills directly

Each SKILL.md file is a standalone system prompt. Copy any individual skill and inject it as a system message in your own API calls, tools, or workflows — no need to use the full agent.

**Example — using Skill 05 (Post-Convergence Handoff) standalone:**
```
System prompt: [contents of skills/05-post-convergence-handoff/SKILL.md]
User message: Here is the chosen concept: [paste concept]
```

---

## Input types

| Type | Example |
|---|---|
| Document-led | Paste a PRD, project brief, initiative doc, or Starts With Why doc |
| Feature/flow-led | "I need ideas for a mobile checkout flow" |
| Problem-led | "Users drop off during KYC — I need wireframe concepts to fix this" |

---

## The 5 skills

| # | Skill | What it does |
|---|---|---|
| 01 | Context Ingestion | Extracts a structured brief from any input |
| 02 | Wireframe Generation | Generates 4-6 divergent low-fi concepts as SVG |
| 03 | Concept Rationale | Named, traceable rationale per concept |
| 04 | Competitive Analysis | Optional — researches competitor patterns |
| 05 | Post-Convergence Handoff | Design principles + full spec when direction is chosen |

---

## Wireframe output

Wireframes are delivered as a single SVG file with all concepts on one canvas. Each concept shows:
- One primary screen per artboard
- Full layout structure with labelled UI zones
- Lucide open source icons (no emoji)
- Clean grey palette — no colour, no decoration
- Concept name and UX framework tag above each artboard

The SVG file can be downloaded from the Claude chat, opened in any SVG viewer, or imported directly into Figma.

---

## Frameworks used

**Jobs To Be Done (JTBD)**
What job is the user hiring this feature to do? Each concept answers the same job differently.

**Mental model alignment**
What does the user already know that this should feel like? Each concept maps to a different reference model the user already carries.

---

## Repository structure

```
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
    PROJECT-INSTRUCTIONS.md
  README.md
```

---

## Cost

- **Hosting:** Free (Claude.ai handles everything)
- **Claude account:** Free tier available, Pro recommended (~$20/month)
- **API usage:** Zero — uses Claude's built-in interface, no API key needed for Options 1 and 2

---

## Contributing

Skills are markdown files — easy to read, easy to edit. If you improve a skill, open a PR. The goal is to make the agent more grounded, more useful, and more accurate over time.