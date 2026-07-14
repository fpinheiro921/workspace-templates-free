# PUBLISHING/

Course Module 2. The actual act of making and shipping newsletters, week after week.

## Read order

1. `idea-generator.md` — how to generate ideas (uses `_PATTERNS/10-magical-ways.md`)
2. `90-day-calendar.md` — rolling quarterly plan
3. `writing-templates.md` — 5 proven newsletter structures
3b. `slide-template.md` — S.L.I.D.E 5-step authority/conversion template (supplementary)
4. `subject-lines.md` — 6-piece headline + 8 patterns
5. `hooks.md` — opening moves (references `_PATTERNS/hook-library-core.md`)
6. `pinned-newsletter.md` — your cornerstone welcome post
7. `analytics.md` — post-publish tracking
8. `repurposing.md` — 1 newsletter → 5+ short-form pieces
9. `mirror-ritual.md` — monthly deconstruction of winning newsletters

## Pipeline

```
idea → outline → draft → scheduled → published → analytics
                           ↑
                    Two-Pass Review
                    (_PATTERNS/two-pass-review.md)
```

## Rules

- Every draft uses ONE of the 5 templates in `writing-templates.md` — pick before drafting, not during
- Every newsletter has 5 subject-line variants generated before scheduling
- Every newsletter has a repurposing plan (at least: 3 tweets + 1 LinkedIn)
- Every published piece gets an analytics entry within 7 days

## Cascade behavior

- When user says "let's write this week's newsletter", Cascade:
  1. Pulls the topic from `90-day-calendar.md`
  2. Asks which template to use
  3. Runs `PROMPTS/generators/idea-to-outline.md`
  4. After user approves outline, runs `PROMPTS/generators/outline-to-draft.md`
  5. Runs `PROMPTS/generators/subject-line-generator.md` (5 variants)
  6. Runs Two-Pass Review
  7. Moves draft to `SCHEDULED/` only after user confirms
