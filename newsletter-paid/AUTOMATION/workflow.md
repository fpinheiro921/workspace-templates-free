# Workflow — Your Automation Stack

The tools that make your newsletter run without your daily intervention.

## The minimum viable stack

### Required
- **Newsletter platform** (Substack / Beehiiv / Ghost / Kit — decided in `POSITIONING/platform-choice.md`)
- **Welcome sequence** — built in-platform (see `welcome-sequence.md`)
- **Analytics dashboard** — platform native is usually enough at <10k subs

### Recommended (by stage)

| Stage | Tool | Purpose |
|---|---|---|
| 1k+ subs | Stripe / Lemonsqueezy (if monetizing outside platform) | Payments |
| 1k+ subs | SparkLoop (if not on Beehiiv) | Referral tracking + cross-publication rec |
| 1k+ subs | Calendly / SavvyCal | Discovery calls (if services lane active) |
| 5k+ subs | A sponsorship marketplace (Passionfruit, Paved) | Passive inbound sponsors |
| 5k+ subs | Feedbin / Readwise for reading inputs | Research + swipe file inputs |
| 10k+ subs | Notion / Coda for content planning (beyond `90-day-calendar.md`) | Team collab if you have help |

### NOT recommended

- **Zapier / Make.com at <1k subs** — adds complexity before you need it
- **Custom GPTs / AI agents for writing** — use generators in `PROMPTS/` directly; don't build agent architecture
- **Separate CRM at <5k subs** — a markdown table in a file is fine

## The weekly workflow

```
Sunday 30min — Review `90-day-calendar.md`, run `idea-generator.md` for next week's angle
Monday 90min — Draft using one of 5 templates
Tuesday 30min — Two-pass review (craft + voice)
Wednesday 15min — Subject-line variants + preview text
Thursday 8am — Publish (you hit the button, not Cascade)
Thursday 9am — Run repurposing-prompt, draft derivatives
Friday 30min — Engagement on tier-1 publishers' content + schedule derivatives
48h post-publish — Analytics entry
7d post-publish — Analytics update
```

Total: ~4 hours/week for a single weekly newsletter + derivatives.

## Platform-specific automation setup

See `platform-templates.md` for the platform-by-platform setup guide.

## Cascade behavior

- When user asks "should I automate X?", check:
  - Is X repetitive (>3x per month)?
  - Does it require judgment you'd want to preserve?
  - Will automation actually save time (accounting for setup + maintenance)?
- Refuse to propose Zapier setups at <1k subs — too much infra for the value.

## Iteration log

- <date>: <what tool added or removed>
