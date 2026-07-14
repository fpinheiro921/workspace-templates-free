# Two-Pass Review

## What it is

Every draft in a writer template moves through two explicit review passes before it can be published or scheduled: a **craft pass** (does it work?) and a **voice pass** (does it sound like you?). Cascade enforces both.

## When to reference

| Template | Files |
|---|---|
| creator-studio | `.windsurfrules`, `WRITING-LAB/writing-rituals.md` |
| newsletter-paid | `.windsurfrules`, `DRAFTS/` → `SCHEDULED/` pipeline rules |
| ghostwriter-practice | `.windsurfrules`, especially for client deliverables |
| fullstack-writer | `.windsurfrules`, all content folders |

## The two passes

### Pass 1 — Craft Pass

Does this piece work as writing? Runs BEFORE the voice pass.

Checklist:
- [ ] **Hook lands in first 1-2 sentences.** Would a stranger keep reading after the first line?
- [ ] **Promise is specific.** The title/intro promises something tangible. The body delivers it.
- [ ] **Structure is skimmable.** Headers, bullets, short paragraphs. A reader could extract 80% of value from headers alone.
- [ ] **Takes a stance.** No hedging. No "in some ways, one could argue…" If you believe it, say it.
- [ ] **CTA is clear.** If there's an ask, it's one specific action. If there's no CTA, that's a choice, not an oversight.
- [ ] **Length is justified.** Every paragraph earns its place. If you cut any paragraph, does the piece get worse?
- [ ] **4Cs pass** — Clear. Concise. Compelling. Credible. (See `copy-frameworks.md` §3.)
- [ ] **Headline/hook packs a punch.** The first line must hit hard as a standalone. Read only the first line — would a stranger stop scrolling? If not, rewrite.
- [ ] **Opinion is stated, not implied.** Don't shy away from a stance. If the post could be written by anyone, rewrite. Contrarian takes are acceptable — vague takes are not.
- [ ] **Active voice.** Passive voice implies something *could* happen. Active voice speaks to a known audience and incites action. Rewrite any passive construction.
- [ ] **No generalizations.** Every claim is specific enough that the reader never thinks "what does that mean?" or "why?". Vague: "Don't waste time on unqualified leads." Specific: "Unqualified leads bloat your pipeline, waste resources, and lead to missed opportunities."
- [ ] **No fat.** Every sentence earns its place. Test: can you cut this sentence without losing meaning? If yes, cut it. Filler example: "To start making a plan, sit down and ask yourself…" → "Ask yourself:"
- [ ] **No redundancy.** No sentence restates a previous sentence in different words. Every sentence adds new information.
- [ ] **White space.** Maximum 2–3 sentences per paragraph for social/email content. Walls of text fail on mobile and kill skimmability.

If anything is a No, fix it. Re-run Pass 1. Only proceed to Pass 2 when Pass 1 is clean.

### Pass 2 — Voice Pass

Does this sound like YOU (or your client, if ghostwriting)? Runs AFTER craft is locked.

Checklist:
- [ ] **Banned-word audit clean.** Scan against `BRAND/banned-words.md` (or client equivalent). Zero hits.
- [ ] **Rhythm.** Alternating long and short sentences. No 5 medium sentences in a row.
- [ ] **Punctuation style matches voice guide.** Em-dashes, ellipses, parentheticals — used or avoided per your `voice-guide.md`.
- [ ] **Register matches.** Conversational vs authoritative vs playful — matches what your `voice-guide.md` specifies.
- [ ] **No LLM tells.** "In today's fast-paced world." "Leverage synergies." "It's important to note that…" "Moreover." "Furthermore." If the LLM drafted this, it probably added at least one.
- [ ] **Contractions appropriate.** Usually yes for conversational; rarely for formal. Match the voice guide.
- [ ] **Opinion-laden, not hedged.** Voice = perspective. If it reads like it could be written by anyone, rewrite.

If anything is a No, fix it. Re-run Pass 2.

## How to apply

### In `.windsurfrules`

```
Content pipeline rule:
- Drafts live in `drafts/` (or `CONTENT/drafts/`)
- A draft cannot move to `scheduled/` without BOTH review passes completed
- When the user says "move this to scheduled" or similar:
  1. Cascade runs Craft Pass — surfaces any failed checks
  2. If Craft Pass clean, run Voice Pass — surfaces any failed checks
  3. Only if both clean, propose the move (but don't auto-move — user confirms)
- If Cascade is the drafter, run both passes before presenting the draft to the user
```

### As a Cascade output format

When reviewing a draft, Cascade produces:

```
## Craft Pass
- [x] Hook lands
- [x] Promise specific
- [ ] Structure skimmable — 3 paragraphs in a row, no bullets (suggest: break paragraph 2 into bullets)
- [x] Stance clear
- [x] CTA clear
- [x] Length justified
- [ ] 4Cs — "leveraging" appears 3x, weakens clarity

## Voice Pass
<run after Craft Pass is clean>
```

### As a ritual in `WRITING-LAB/writing-rituals.md`

Daily draft → Cascade runs Craft Pass on demand
Before scheduling → Cascade runs both passes
Weekly review → user re-reads scheduled posts, optional third "taste pass" for final feel

### Exceptions

- **Draft-stage explorations** don't need either pass (by definition not ready)
- **Private notes** (TEMP/, DOCS/) don't need passes
- **Client ghostwriting** uses the client's voice guide (not your own) in Pass 2
- **Cascade's internal work** (spec docs, analysis, plans) — skipped; this rule is for creative/persuasive content

## Credits

- Common editorial practice; no single source
- The specific "craft then voice" ordering is a synthesis of: Sean D'Souza's copy rework rhythm, Nicolas Cole's style enforcement in PGA, classical editing
- Active voice, no generalizations, trim fat, no redundancy, white space rules — Erica Schneider, *Zero to 10k Twitter Accelerator*; paraphrased
- Headline punch + opinion/contrarian checks — Tim Denning, *Twitter Badassery*; paraphrased

## Iteration log

- 2026-04-18: created
- 2026-04-21: added 5 Craft Pass checks (active voice, no generalizations, no fat, no redundancy, white space) — sourced from Erica Schneider, Zero to 10k Twitter Accelerator
- 2026-04-23: added 2 Craft Pass checks (headline punch, opinion stated not implied) — sourced from Tim Denning, Twitter Badassery
