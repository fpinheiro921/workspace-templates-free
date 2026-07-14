# Idea Generator

How to generate newsletter ideas that don't feel repetitive. Uses `_PATTERNS/10-magical-ways.md`.

## The method

Never "what should I write about this week?" — that's a wrong question that leads to blank-page paralysis.

Right question: "Given my pillars + my audience, what angle should I take this week?"

## The 10-angles rotation

For each content pillar you have (from `CONTEXT/newsletter-brief.md`), you can produce 10 distinct newsletters using the 10 angles:

| Angle | Format |
|---|---|
| Tips | `7 tips for {outcome}` |
| Stats | `3 stats that prove {claim}` |
| Steps | `The 5-step process to {outcome}` |
| Lessons | `8 lessons from {experience}` |
| Benefits | `10 benefits of {practice}` |
| Reasons | `5 reasons {common belief} is wrong` |
| Mistakes | `6 mistakes beginners make with {topic}` |
| Examples | `12 examples of {principle} in action` |
| Questions | `7 questions to ask before {decision}` |
| Personal Stories | `What I learned from {experience}` |

**3 pillars × 10 angles = 30 potential newsletters.** That's 7+ months of weekly content, all distinct.

## Weekly idea generation ritual (15 min)

1. Open `90-day-calendar.md`
2. Look at next week's slot — what pillar + theme?
3. Use LLM generator (`PROMPTS/generators/idea-to-outline.md`) with pillar + angle input
4. Get 10 headline candidates
5. Pick the 1 with highest gut response AND clearest tangible outcome
6. Write headline into calendar cell for next week

## Idea bank

Running list of pre-validated angles. Build this over time. Tag each by pillar + angle.

| Idea | Pillar | Angle | Status |
|---|---|---|---|
| | | | queued / drafted / published / retired |

## Red flags on an idea

- Can you state the tangible outcome for the reader in one sentence? If not, the idea isn't ready.
- Would your competitors (from `competitive-analysis.md`) cover this exact angle? If yes, find a different angle.
- Do you actually have information advantage on this? (See `CONTEXT/newsletter-brief.md`.) If not, skip or go research.

## Credits

10 Magical Ways — Nicolas Cole. See `_PATTERNS/attribution-rules.md`.
