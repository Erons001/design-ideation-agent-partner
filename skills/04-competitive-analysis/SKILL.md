# Skill 04 — Competitive Analysis

## Purpose
Research how competitors and leading products have solved this design problem. Produce a pattern library with three actionable directives that Skill 02 uses to position the 4 concepts relative to the market.

## When this skill runs
ALWAYS — not optional. Runs automatically after Skill 01 confirms the brief. Do not ask the user. Just run it.

## Research scope
1. Direct competitors — same problem, same users
2. Adjacent patterns — different category, similar interaction problem
3. Best-in-class references — widely recognised leading UX in this domain

For each: dominant layout or flow pattern, primary UX model, what it optimises for, notable divergences.

## Output format

PATTERN LIBRARY — [Feature/Flow]
---------------------------------
Dominant pattern:
[Most common approach — specific about layout, step count, information structure]

Notable examples:
- [Product]: [What they do, how structured, what it optimises for]
- [Product]: [What they do, structure, optimisation]
- [Product]: [What they do, structure, optimisation]

Conventions users will likely expect:
[3-5 specific patterns users already know from other products]

Gaps and opportunities:
[Where solutions fall short — specific about which user need is unaddressed]

Directives for Skill 02:
FOLLOW:    [Specific pattern to mirror — named product, specific structure, reason users expect it]
CHALLENGE: [Specific convention to subvert — named convention, specific gap it addresses]
BORROW:    [Adjacent pattern from different domain — named product, specific mechanism to adapt]

## Research quality rules

Cite real products only — never "most apps do X."
Be specific about structure — not "step-by-step" but "4-screen wizard, screen 1 collects email, screen 2 sets password..."
Distinguish mobile from desktop conventions.
Flag patterns older than 3 years that newer products have moved away from.

## Directive quality standard

Bad: "FOLLOW — use a clean layout"
Good: "FOLLOW — use a 3-step wizard with persistent progress bar at top, as used by Stripe Identity, Veriff, and Jumio. Users attempting KYC on mobile already expect this structure."

Bad: "CHALLENGE — make it simpler"
Good: "CHALLENGE — remove the upfront explanation screen all competitors show before the first data request. This delays action for users who have already decided to proceed."

Bad: "BORROW — use a familiar pattern from another domain"
Good: "BORROW — adapt the delivery tracking model used by DHL and Fedex. 3 milestone cards (ID, selfie, bank link), each showing locked/unlocked/complete state. No competitor currently uses this."

## Rules
- Always cite real, identifiable products
- Cap at 5 products — depth over breadth
- Separate observation from opinion — recommendation section only
- FOLLOW, CHALLENGE, BORROW must each be specific and actionable

## Handoff
Pass full pattern library and all three directives to Skill 02.
Skill 02 must reference the directives in the concepts overview.