# MEMORY.md — Sleeping Context Index

> Read this at session start. Load ONLY what the conversation needs. Do not load everything upfront.

---

## Always-On (Load Every Session)
These are read automatically by `.windsurfrules` at session start:
- `01-COMPANY-CONTEXT/index.md`
- `03-INITIATIVES/index.md`

---

## Load When Relevant

| Load When... | File(s) to Read |
|---|---|
| Any product strategy or vision discussion | `01-COMPANY-CONTEXT/vision-strategy.md` |
| Writing or reviewing OKRs | `01-COMPANY-CONTEXT/okrs.md` |
| Any mention of a specific stakeholder by name | `01-COMPANY-CONTEXT/stakeholder-avatars/[name].md` |
| Any comms, negotiation, or political situation | `01-COMPANY-CONTEXT/org-survival/power-map.md` + `political-landscape.md` |
| Competitor mention or competitive question | `02-KNOWLEDGE/competitors/[name].md` |
| User research or customer feedback topic | `02-KNOWLEDGE/research/` + `02-KNOWLEDGE/feedback/` |
| Any mention of a past decision ("why did we...") | `02-KNOWLEDGE/decisions/` |
| Active feature/initiative by name | `03-INITIATIVES/[initiative].md` |
| Retrospective or reflection | `00-META/learning-log.md` |
| Performance review or growth topic | `00-META/growth-portfolio.md` |
| Forecast or "were we right?" question | `00-META/forecast-tracker.md` |

---

## Never Load Upfront
- All of `02-KNOWLEDGE/` (load only the relevant subfolder/file)
- All stakeholder avatars (load only the mentioned person)
- All initiative files (load only active/mentioned ones)
- `00-META/` files (load only when reflection is the topic)

---

## Checkpoint Protocol
For long sessions (50+ exchanges), checkpoint to avoid context drift:
1. Save current state summary to `checkpoints/session-YYYY-MM-DD.md`
2. Note what files were loaded this session
3. Note open questions or unfinished decisions
