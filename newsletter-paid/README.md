# Newsletter Paid

Operating system for running a **paid newsletter** (Substack / Beehiiv / Ghost / Kit) as a real business.

Cascade = positioning coach + writing partner + growth strategist + monetization advisor.

---

## What this template is

- Complete workflow from blank page → paid subscribers
- 5 sections map 1:1 to Dickie Bush's Category Newsletter Creator curriculum (Positioning → Publishing → Automation → Growth → Monetization)
- Opinionated: forces you to pick a niche + platform before drafting anything
- Ships with 3 reusable LLM prompt generators + 5 newsletter templates

## What this template is NOT

- Not a free-only newsletter tool — if you don't intend to monetize, use `creator-studio/` instead (lighter, broader content focus)
- Not a replacement for the course — this is workflow scaffolding; the strategic insights still come from Dickie's actual curriculum
- Not a posting automation tool — Cascade drafts, you publish

---

## First steps

1. **Fill `CONTEXT/newsletter-brief.md`** — niche, platform, stage (0-1 / 1-10k / 10k+), revenue target
2. **Make the 4 positioning decisions** in order:
   - `POSITIONING/free-vs-paid.md` — revenue model
   - `POSITIONING/platform-choice.md` — Substack / Beehiiv / Ghost / Kit
   - `POSITIONING/niche-framework.md` — niche (via 6-way framework in `_PATTERNS/positioning-framework.md`)
   - `POSITIONING/naming.md` + `POSITIONING/description.md`
3. **Run competitive analysis** — `POSITIONING/competitive-analysis.md`
4. **Draft monetization thesis** — `CONTEXT/monetization-thesis.md` (which lanes at which stage)
5. **Seed 12 weeks of ideas** in `PUBLISHING/90-day-calendar.md`
6. **Write your pinned cornerstone newsletter** — `PUBLISHING/pinned-newsletter.md`

Then start drafting via `DRAFTS/_newsletter-template.md`.

---

## Folder map

```
newsletter-paid/
├── .windsurfrules
├── README.md
├── LICENSE
│
├── CONTEXT/                 ← WHO + WHY + WHAT
│   ├── newsletter-brief.md
│   ├── voice-guide.md
│   ├── monetization-thesis.md
│   └── decisions-log.md
│
├── POSITIONING/             ← Course Module 1
│   ├── free-vs-paid.md
│   ├── platform-choice.md
│   ├── niche-framework.md
│   ├── competitive-analysis.md
│   ├── naming.md
│   ├── description.md
│   └── visual-brand.md
│
├── PUBLISHING/              ← Course Module 2
│   ├── idea-generator.md
│   ├── 90-day-calendar.md
│   ├── writing-templates.md     ← 5 proven structures
│   ├── subject-lines.md         ← 6-piece headline framework
│   ├── hooks.md
│   ├── pinned-newsletter.md     ← your cornerstone welcome post
│   ├── analytics.md
│   ├── repurposing.md
│   ├── mirror-ritual.md
│   └── platform-specific/       ← Platform guides
│       ├── substack.md          ← Complete Substack guide
│       ├── beehiiv.md           ← [Create when needed]
│       └── ghost.md             ← [Create when needed]
│
├── DRAFTS/SCHEDULED/PUBLISHED/  ← pipeline
│
├── GROWTH/                  ← Course Module 4
│   ├── traffic-engine.md
│   ├── cross-promotion.md
│   ├── referral-program.md
│   ├── paid-acquisition.md
│   └── comment-engagement.md
│
├── MONETIZATION/            ← Course Module 5
│   ├── affiliate.md
│   ├── sponsorship.md
│   ├── subscription.md
│   ├── digital-product.md
│   └── services-coaching.md
│
├── AUTOMATION/              ← Course Module 3
│   ├── workflow.md
│   ├── welcome-sequence.md      ← 10-email onboarding
│   ├── platform-templates.md
│   └── checklists.md
│
├── SUBSTACK/                ← ⚠️ DEPRECATED: Moving to PUBLISHING/platform-specific/
│   └── (contents being migrated)
│
├── PROMPTS/                 ← reusable LLM generators
│   ├── prompt-writing-template.md
│   └── generators/
│       ├── idea-to-outline.md
│       ├── outline-to-draft.md
│       ├── subject-line-generator.md
│       ├── repurposing-prompt.md
│       └── mirror-prompt.md
│
├── TEMP/                    ← raw inbox
└── DOCS/                    ← stable references
```

---

## Shared Patterns Library

References `H:\WORKSPACE TEMPLATES\_PATTERNS\`:
- `positioning-framework.md` — 6 ways to niche + constellation + bio variants
- `hook-library-core.md` — 6-piece headline + hook types + 30 listicle nouns
- `monetization-lanes.md` — 5 revenue lanes + 10-variable offer stack
- `10-magical-ways.md` — universal content expander
- `two-pass-review.md` — craft + voice rules
- `faulty-beliefs.md` — "2 clients, not 2,000" mental unlock
- `prompt-library-standard.md` — standard generator file shape
- `attribution-rules.md` — paraphrase + credit rules

---

## How Cascade helps

- Runs the positioning gate (refuses to draft if positioning incomplete)
- Drafts newsletters from your calendar entries using one of 5 templates
- Generates 5 subject-line variants per send (from 6-piece headline + 8 patterns)
- Generates 10 hook variants on demand (from 6 hook types)
- Runs Two-Pass Review (craft + voice) before anything moves to SCHEDULED
- Proposes quarterly calendar (12 weeks × angles rotating via 10 Magical Ways)
- Runs monthly mirror ritual (deconstructing 3 viral newsletters)
- Tracks analytics in `PUBLISHING/analytics.md` post-publish
- Proposes monetization-lane decisions based on stage (via `_PATTERNS/monetization-lanes.md` gates)
- Curates competitive analysis in `POSITIONING/competitive-analysis.md`

## How Cascade does NOT help

- Never publishes for you
- Never sends email on your behalf
- Never changes pricing without explicit approval + decisions-log entry
- Never adds a banned word or removes one without asking

---

## Stages

- **0-1** — no audience, no subscribers. Focus: positioning + first 10 subs via personal network
- **1-1k** — early subs from cold outreach + commenting. Focus: weekly publishing consistency
- **1k-10k** — growth lane activation (cross-promotion, referral, paid). Focus: retention + paid tier launch
- **10k+** — monetization diversification. Focus: 2-3 lanes, system stability, team if needed

`.windsurfrules` adjusts tone by stage — e.g., at 0-1 never suggests paid acquisition; at 10k+ routinely raises sponsorship conversations.

---

## Related Templates

| If you want to... | Use this template |
|-------------------|-------------------|
| Start from zero (no audience yet) | `02-CONTENT-BUSINESS/creator-studio/` — Build foundation and personal brand first |
| Sell newsletter services to local businesses | `02-CONTENT-BUSINESS/local-newsletter-agency/` — Agency model serving clients |
| Write for clients as a ghostwriter | `02-CONTENT-BUSINESS/ghostwriter-practice/` — Premium writing services |
| Run multiple revenue lanes (writing + products + services) | `02-CONTENT-BUSINESS/fullstack-writer/` — Advanced orchestration |
| Build a course instead of a newsletter | `03-EDUCATION/course-creator/` — Product-based business model |

---

## Credits & Influences

This template's craft patterns are adapted from:

- **Dickie Bush** — Category Newsletter Creator (positioning + publishing + growth + monetization curriculum)
- **Nicolas Cole** — Ghostwriter GPT (prompt generators, 6-piece headline, offer stack)
- **Ship 30 for 30** — writing-online fundamentals
- **Premium Ghostwriting Academy (PGA)** — service-business playbook
- **Classic direct response** — PAS, AIDA, BAB, 4Cs (public-domain craft)

All original IP remains with the respective authors. If you want the originals, buy the course. Frameworks in this template are paraphrased per `_PATTERNS/attribution-rules.md`.
