# Skill 04 — Competitive Analysis

## Purpose
Research how competitors and leading products have solved the same or similar design problem. This skill runs ALWAYS — it is not optional. Its output directly informs Skill 02, ensuring every wireframe concept is grounded in real industry patterns.

## When this skill runs

**ALWAYS — this skill is not optional and does not require user confirmation.**
It runs automatically immediately after Skill 01 confirms the brief, before Skill 02 generates anything.
Do not ask the user if they want competitive analysis. Just run it.

## Research scope
Search for:
1. Direct competitors — products solving the same problem for the same users
2. Adjacent patterns — products in different categories solving a similar interaction problem
3. Best-in-class references — products widely recognised as leading UX in this domain

For each, identify:
- The dominant layout or flow pattern used
- The primary UX model (progressive, minimal, dashboard, wizard, hub-and-spoke, etc.)
- What the pattern optimises for (speed, trust, discoverability, completion rate, etc.)
- Any notable divergences from the norm

## Output format

PATTERN LIBRARY — [Feature/Flow]
---------------------------------
Dominant pattern:
[Description of the most common approach — be specific about layout, step count, information structure]

Notable examples:
- [Product]: [What they do, how they structure it, what it optimises for]
- [Product]: [What they do, how they structure it, what it optimises for]
- [Product]: [What they do, how they structure it, what it optimises for]

Conventions users will likely expect:
[3-5 specific patterns users will already be familiar with]

Gaps and opportunities:
[Where existing solutions fall short — be specific about what user need is unaddressed]

Directives for Skill 02:
- FOLLOW: [What at least one concept must closely mirror — because users expect it]
- CHALLENGE: [What at least one concept must subvert — to address the gap identified]
- BORROW: [An adjacent pattern from a different domain worth exploring as an unconventional concept]


## Research quality rules

### Cite real products only
Never use generic descriptions like "most apps do X" or "common practice is Y".
Every claim must reference a specific, named product.
If you cannot name a product, do not make the claim.

### Be specific about structure
Do not say "uses a step-by-step approach."
Say "uses a 4-screen wizard with progress bar at top — screen 1 collects email, screen 2 sets password, screen 3 verifies phone, screen 4 shows success state."

### Distinguish between mobile and desktop patterns
If the research covers both, note differences explicitly.
Do not conflate mobile and desktop conventions.

### Flag outdated patterns
If a pattern appears in products that are more than 3 years old and newer products have moved away from it, flag it:
"This pattern was dominant in 2021-2022 but has largely been replaced by [newer approach] in more recent products."

### FOLLOW / CHALLENGE / BORROW must be actionable
Bad: "FOLLOW — use a clean layout"
Good: "FOLLOW — use a 3-step wizard with persistent progress bar at top, as used by Stripe Identity, Veriff, and Jumio. Users attempting KYC verification on mobile already expect this structure."

Bad: "CHALLENGE — make it simpler"
Good: "CHALLENGE — remove the upfront explanation screen that all competitors show before the first data request. Research shows this delays action without meaningfully improving trust for users who have already decided to proceed."

Bad: "BORROW — use a familiar pattern from another domain"
Good: "BORROW — adapt the delivery tracking model used by DHL and Fedex. Users understand a sequential tracker with status per milestone. Applied here: 3 milestone cards (ID, selfie, bank link), each showing locked/unlocked/complete state."

## Rules
- Always cite real, identifiable products — no generic descriptions
- Cap at 5 products researched — depth over breadth
- Flag patterns more than 3 years old showing signs of being superseded
- The three directives must be specific and actionable — not generic platitudes

## Handoff
Pass the full pattern library and the three directives to Skill 02.
Skill 02 must reference the directives explicitly in the concepts overview.