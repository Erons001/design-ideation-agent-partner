# Skill 03 — Concept Rationale

## Purpose
For each of the 4 wireframe concepts, produce a deep, named rationale that gives the designer genuine clarity on what the concept is doing, why it works, who it works for, and what it risks. This is not a description of the layout. It is the design thinking that makes the concept actionable.

A good rationale answers: "Why would a real designer choose this direction over the others?"

---

## Output format per concept

CONCEPT [N] — [Name]

DESIGN HYPOTHESIS
One sentence in this format:
"If [specific user type] [specific belief, behaviour, or emotional state], then [specific design approach] will [expected outcome] because [the underlying reason]."

Good example: "If first-time fintech users are anxious about sharing personal data, then leading with a transparent explanation of why each piece of information is legally required — before asking for anything — will increase completion rates because trust is established before commitment is requested."

Bad example: "Users will trust this design more because it looks cleaner." — This is not a hypothesis. It cannot be tested and it does not name a specific user behaviour.

---

UX FRAMEWORK
[JTBD or Mental model alignment]

If JTBD:
Job: [The specific progress the user is trying to make — not the feature, but the outcome they want]
How this concept delivers the job differently: [What unique answer this concept gives compared to the other 3]

If Mental model alignment:
Reference model: [The specific product, experience, or system the user already knows that this maps to]
Why that model fits: [Why this reference model reduces cognitive load or builds trust for this specific user]

---

PSYCHOLOGICAL PRINCIPLE
[Name the specific principle and explain exactly how the design expresses it]

Name one from: completion bias, loss aversion, progressive commitment, familiarity effect, autonomy bias, cognitive load reduction, social proof, reciprocity, the endowment effect, anchoring, the Zeigarnik effect, scarcity, authority, default bias, the peak-end rule, chunking.

Then explain specifically:
"This concept uses [principle] by [specific design decision], which means the user [specific behavioural response that follows from the principle]."

Do not just name the principle. Show exactly how the layout or flow decision expresses it.

---

SPECIFIC FRICTION ADDRESSED
Name the exact moment of hesitation, confusion, or drop-off this concept targets.

Not "reduces friction" — name the friction:
"The drop-off point this concept addresses: when [specific thing happens in the current or common experience], users [specific negative behaviour — abandon, hesitate, make errors, feel anxious]. This concept prevents this by [specific mechanism the layout or flow creates]."

---

THE BET THIS CONCEPT MAKES
Every concept makes a different assumption about the user. State it clearly.

"This concept bets that [specific assumption about the user's motivation, mental state, or behaviour]. If that assumption is wrong — if users actually [the alternative behaviour] — then this concept will underperform because [specific consequence]."

This section exists to help the designer understand the risk of each concept and choose based on what they know about their actual users — not based on which concept looks best.

All 4 concepts must make different bets. If two concepts share the same bet, one of them is a variation, not a distinct concept.

---

COMPETITIVE POSITION
State how this concept responds to the competitive analysis.

"This concept [follows / challenges / borrows from] [specific pattern from the competitive analysis]. It [does / does not] deviate in [specific way] because [reason tied to the brief and the gap identified]."

Reference the actual FOLLOW, CHALLENGE, or BORROW directive from Skill 04.

---

A CONCRETE SCENARIO
Write one specific user moment using this concept. Make it real.

Requirements:
- Give the user a name
- Give them a specific location and device
- Give them an emotional state and a time constraint
- Describe exactly what they see when they land on this screen or start this flow
- Show what they do and what happens as a result
- 4-6 sentences

Do not write: "A user opens the app and sees the screen."
Write: "Tunde, a 34-year-old small business owner in Lagos, opens the app on his Android phone while waiting for a client meeting to start. He has 3 minutes. He needs to send a payment before the meeting begins. He sees one field — the amount — and a large 'Send' button. No navigation, no balance summary, no account menu. He types the amount, selects the recipient from his recent contacts, and hits Send. Done in 45 seconds."

---

WHAT SUCCESS LOOKS LIKE
Describe 2-3 specific, observable outcomes that would indicate this concept is working. Things that could actually be measured in a usability test or seen in analytics.

Not "users complete the flow." Specifics:
- [Specific measurable behaviour or metric]
- [Specific thing a usability test participant does or says]
- [Specific drop in error rate, hesitation time, or support contact rate]

---

VALIDATION QUESTION
The single most important question to answer before committing to this concept.

Must be specific to the bet this concept makes — not a generic usability question:
"The key thing to learn from testing this concept: [specific question about the assumption this concept makes that the others do not]."

---

TRADE-OFF
What this concept explicitly sacrifices to achieve its goal. Be honest.

"This concept optimises for [X] at the cost of [Y]. Designers who choose this direction should accept that [specific consequence that is real and non-trivial]."

Do not write small trade-offs. Every concept has a real cost:
- A minimal concept sacrifices discoverability and support for anxious users
- A power user concept sacrifices accessibility for first-timers
- A progressive concept sacrifices speed for users who already know what they want
- A familiar concept sacrifices differentiation and innovation

---

## Rules

All 4 hypotheses must be falsifiable — specific enough to be proven wrong.
All 4 bets must be genuinely different from each other.
All 4 scenarios must name a real person in a real moment.
All 4 trade-offs must name a real, non-trivial cost.
Every section must connect back to the structured brief.

## Handoff
When the user selects a concept, pass the full rationale — especially the hypothesis, the bet, the scenario, and the trade-off — to Skill 05 as context for design principles and spec.
## Quality check before outputting rationale

Before finalising each concept's rationale, verify:

1. Is the hypothesis falsifiable? Can it be proven wrong by a specific test?
   If not → rewrite it with a specific user, specific belief, and specific expected outcome

2. Are all 4 bets genuinely different from each other?
   If two concepts share the same bet → replace the weaker one with a different angle

3. Does the scenario name a real person with a real context?
   If it says "a user opens the app" → rewrite with a name, location, device, emotional state, and time constraint

4. Does the trade-off name a real, non-trivial cost?
   If it says "slightly less efficient" → rewrite with the specific user segment that will be worse off and why

5. Does the validation question target the specific bet this concept makes?
   If it is a generic usability question → rewrite it as a question only this concept can answer

