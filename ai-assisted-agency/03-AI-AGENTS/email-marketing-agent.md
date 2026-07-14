# Email Marketing Agent

## What It Does

Writes multi-step cold email sequences with spintax variations, follow-up logic, and break-up emails — fully personalized based on prospect data from the Lead Gen Agent.

**Output per run:**
- 3-email sequence per prospect
- Spintax subject lines (3+ variations)
- Personalized first line woven in from Lead Gen Agent
- Export to Google Sheets for import to Instantly/Smartlead

---

## Agent Architecture

```
[Prospect Data from Lead Gen Agent]
    ↓
[Email Sequence Writer]    ← Claude: writes 3-email sequence with spintax
    ↓
[Quality Filter]          ← Claude: scores each email against rules
    ↓
[Google Sheets Export]    ← Appends to sending queue
    ↓
[Import to Instantly / Smartlead]
```

---

## Node 1: Email Sequence Writer

**Model:** Claude Sonnet

**System Prompt:**
```
You are a cold email copywriter. Write 3-email sequences for B2B prospects.

Rules:
- Email 1: Lead with personalized first line → offer brief → single CTA
- Email 2 (3 days later): Different angle — case study, result, or proof point
- Email 3 (5 days later): Break-up email — low pressure, leave door open
- All emails under 120 words
- Subject lines: 3 spintax variations each, using {option1|option2|option3} format
- No: "Hope this finds you well", "I came across your profile", "Quick question"
- CTAs must be singular and frictionless: one ask per email
- Sound like a human, not a funnel
```

**User Prompt:**
```
Write a 3-email sequence for this prospect.

Prospect: [name]
Company: [company]
Job title: [title]
Personalized first line: [from Lead Gen Agent]
Company info: [from Lead Gen Agent]
Offer context: [your service + target outcome]
```

---

## Email 1: Cold Opener

**Goal:** Get a reply. Not a sale. A reply.

**Structure:**
```
Subject: {option A|option B|option C}

[Personalized first line from Lead Gen Agent]

[2-sentence offer: what you do + who it's for]

[1-sentence result/outcome: what they get]

[Frictionless CTA: "Worth a quick call?" or "Want me to send over an example?"]

[Name]
```

**Example:**
```
Subject: {quick question|[company] + leads|idea for [company]}

Saw your post about hiring 3 AEs last week — sounds like the pipeline 
needs to keep pace.

We build AI-personalized cold email systems for B2B SaaS companies that 
generate 20+ qualified calls/month.

We've done this for 4 companies similar to [company name] in the last 6 months.

Worth a 15-min call to see if it makes sense?

[Name]
```

---

## Email 2: Follow-Up (Day 3)

**Goal:** New angle. Don't resell. Show proof.

**Structure:**
```
Subject: {option A|option B|option C}

[1-sentence re-intro or context refresh]

[Case study or specific result: "[Client] went from X to Y in Z weeks"]

[Why it's relevant to them specifically]

[Same or softer CTA]

[Name]
```

**Example:**
```
Subject: {what [similar company] did|follow up|quick case study}

Following up on my last email.

One of our clients — a 25-person SaaS company — went from 
8 to 31 qualified calls/month in 6 weeks using our system.

Given you're scaling the sales team, the timing might be right.

Open to a quick chat this week?

[Name]
```

---

## Email 3: Break-Up (Day 5)

**Goal:** Final touch. Low pressure. Keep door open.

**Structure:**
```
Subject: {option A|option B|option C}

[Acknowledge they're busy — without being passive-aggressive]

[Soft last pitch: summarize the value in 1 line]

[Permission to say no — makes them feel safe to reply]

[Name]
```

**Example:**
```
Subject: {closing the loop|last one|no hard feelings}

Last one, I promise.

If generating a consistent pipeline of qualified calls isn't a priority 
right now, completely understood.

If it ever is — or if timing changes — feel free to reach out.

[Name]
```

---

## Spintax Rules

Use `{variation1|variation2|variation3}` for:
- Subject lines (at minimum 3 variations)
- Opening lines (when not personalized)
- CTA phrasing

**Subject line formulas:**
```
{Type 1: Direct value}    → "20 qualified calls/month for [company]"
{Type 2: Curiosity}       → "quick idea for [company]"
{Type 3: Social proof}    → "how [similar company] hit [result]"
{Type 4: Question}        → "struggling with pipeline right now?"
{Type 5: Personalized}    → "[first name] — quick question"
```

All spintax variations must read naturally. Test by reading each one individually.

---

## Quality Filter Node

Add a second Claude call that scores the sequence before export.

**System Prompt:**
```
You are a cold email quality reviewer. Score this 3-email sequence 
on the following criteria (1–10 each):

1. Personalization: Does Email 1 reference something specific?
2. Brevity: Are all emails under 120 words?
3. Single CTA: Is there only one ask per email?
4. No generic openers: Zero "Hope this finds you well" type phrases?
5. Spintax: Do all {option|option} variations read naturally?
6. Sequence logic: Does each email take a new angle?

If any score is below 7, flag and explain what to fix.
Output: PASS or FLAG with notes.
```

Only export sequences that PASS to Google Sheets.

---

## Google Sheets Export Schema

```
prospect_name | email | company | sequence_email_1 | subject_1a | subject_1b | subject_1c |
sequence_email_2 | subject_2a | subject_2b | subject_2c |
sequence_email_3 | subject_3a | subject_3b | subject_3c |
first_line | status | date_added
```

---

## Import to Sending Tool

### Instantly
1. Export CSV from Google Sheets
2. Instantly → Campaigns → Upload Leads
3. Set sequence timing: Email 1 → +3 days → +5 days
4. Enable spintax in campaign settings
5. Start with 10–15 emails/day per inbox (warm-up phase)

### Smartlead
Same process — Smartlead supports spintax natively and has a CSV import flow.

---

## Sending Infrastructure Checklist

Before sending a single email:
- [ ] Custom domain (not primary business domain)
- [ ] SPF, DKIM, DMARC configured
- [ ] Inbox warmed up for 2–3 weeks (10–15/day)
- [ ] Reply detection active (Instantly/Smartlead handles this)
- [ ] Unsubscribe link or "reply STOP" language included
- [ ] Sending from real human-named email (not info@ or sales@)

---

## Performance Benchmarks

| Metric | Cold (industry avg) | Good | Great |
|--------|--------------------|----|------|
| Open rate | 20–30% | 40%+ | 50%+ |
| Reply rate | 1–3% | 5–8% | 10%+ |
| Positive reply rate | 0.3–0.5% | 1–2% | 3%+ |
| Calls booked per 100 sent | 0.5–1 | 2–3 | 5+ |

Benchmark against yourself weekly. Improve subject lines first (highest leverage), then openers, then body copy.
