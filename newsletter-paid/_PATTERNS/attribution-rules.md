# Attribution Rules

## What it is

Rules for how templates in this workspace adapt, cite, and paraphrase content from paid courses and public-domain frameworks. Protects the user legally, ethically, and from shipping something that could damage relationships with course creators whose work inspires the templates.

## When to reference

Every template that adapts content from external courses, books, or paid products. That's:
- creator-studio (Dickie Bush / Cole / others)
- newsletter-paid (Dickie Bush)
- ghostwriter-practice (Dickie Bush / Nick Cole / PGA)
- fullstack-writer (FSW curriculum)
- Any future writer template

## The 4 rules

### Rule 1 — Paraphrase, don't copy

Never ship a verbatim prompt, framework description, or example from a paid course.

**OK:** Keeping the framework structure (e.g. "6 pieces of an irresistible headline: HOW MANY / THE WHAT / THE HOW / THE WHO / THE WHY / TWIST THE KNIFE") — frameworks are not copyrightable in most jurisdictions.

**NOT OK:** Copying the exact explanatory text, examples, or prompt-body language used by the course.

**How to paraphrase well:**
1. Read the source once
2. Close the source
3. Write the pattern in your own words, using your own examples
4. Re-open the source only to verify you got the framework structure right, not the phrasing

### Rule 2 — Credit in every template README

Every template that uses `_PATTERNS/` content sourced from paid courses must include this section in its `README.md`:

```markdown
## Credits & Influences

This template adapts craft patterns from:

- **Dickie Bush** & **Nicolas Cole** — Category Newsletter Creator, Ghostwriter GPT, Full Stack Writer curricula
- **Ship 30 for 30** — writing-online fundamentals
- **Premium Ghostwriting Academy (PGA)** — service-business playbooks

All frameworks are paraphrased; original IP belongs to respective authors.

If you want the originals, buy the courses:
- [Category Newsletter Creator](https://typeshare.co/newsletter-creator)
- [Ghostwriter GPT](https://www.premiumghostwritingacademy.com/)
- [Full Stack Writer](https://www.premiumghostwritingacademy.com/)
- [Ship 30 for 30](https://www.ship30for30.com/)
```

(Verify URLs are current when shipping; they change.)

### Rule 3 — Private study references stay private

These files are **private to this workstation**:
- `H:\WORKSPACE TEMPLATES\_tools\extracted\` — 349 raw extractions from course PDFs/DOCXs
- `H:\WORKSPACE TEMPLATES\WRITING-COURSES-FRAMEWORKS.md` — detailed study notes with verbatim-adjacent content

**Never commit these to a public repo.**

If templates root ever becomes public (e.g. open-sourced on GitHub), add to `.gitignore`:
```
_tools/extracted/
WRITING-COURSES-FRAMEWORKS.md
WRITING-COURSES-INSIGHTS.md
```

`_PATTERNS/` itself can be public — it only contains paraphrased frameworks, properly credited.

### Rule 4 — Cascade auto-detects drift

When Cascade is asked to draft or iterate on a prompt, generator, or framework in a writer template, she should compare the output to what she knows about the source course and **surface** if the output feels too close to verbatim.

**Example Cascade response:**
> "The prompt I drafted for `short-form-generator.md` still reuses phrases from the Ghostwriter GPT Module 5 prompt (e.g. 'declarative perspective distilled'). Suggestion: rewrite Rule 1 as 'a single paragraph that crystallizes one strong opinion or insight' — same meaning, different words."

User decides whether to accept the paraphrase or keep the closer wording.

## What's safely public domain

These do NOT need Dickie Bush / Nick Cole attribution (though a general "classic direct response" mention is nice):

- **PAS** (Problem / Agitate / Solve) — generations of copywriters
- **AIDA** (Attention / Interest / Desire / Action) — E. St. Elmo Lewis, 1898
- **BAB** (Before / After / Bridge) — generic
- **4Cs** (Clear / Concise / Compelling / Credible) — generic
- **10 Magical Ways** list itself (Tips/Stats/Steps/…) — the labels are generic; the specific packaging ("10 Magical Ways") is Cole's framing and should be credited

**Public-domain frameworks can be described in detail without paraphrase obligation.**

## What's borderline

- **The 6-piece irresistible headline** (HOW MANY + THE WHAT + THE HOW + THE WHO + THE WHY + TWIST THE KNIFE) — specific framing is Cole's. Credit him. The underlying observation that great headlines have number + topic + approach + audience + outcome is generic.
- **The 9-step sales script** — the overall arc (Intro / Agenda / Recap / Qualify / Mirror / Offer / Price / Objections / Close) is standard consultative selling. The specific step names + language are Cole's. Credit + paraphrase the phrasing.
- **The Offer Stack 10 variables** — specific structure is Cole's. Credit + paraphrase.

## What's clearly Cole / Bush IP — paraphrase hard

- Prompt bodies verbatim
- Specific examples ("Newsletter Autopilot Package at $3,500/mo" deliverable list)
- "Big 3 Faulty Beliefs" exact phrasing
- "Client Constellation" metaphor
- "10 Magical Ways" label
- "Free Consulting Method"
- "Premium Ghostwriting Academy" / "PGA" terminology
- "The Ghostwriter Income Staircase" (5 levels)

Credit in README + paraphrase in content.

## How to apply

When Cascade is authoring a new generator, file, or section in a writer template:

1. Identify: is the source a paid course or public-domain?
2. If paid course: paraphrase hard, credit in README
3. If public-domain: describe freely, light credit is polite
4. If borderline: paraphrase + credit — err on the side of caution
5. Before committing, scan for direct quotes from the source

## Iteration log

- 2026-04-18: created
