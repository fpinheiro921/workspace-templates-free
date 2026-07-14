# Cold Email System

## The Pipeline Math

Every cold email campaign comes down to one equation:

```
Sends → Opens → Replies → Positive Replies → Calls Booked → Clients Closed
```

You control the top (sends, offer, subject lines). The market controls the rest. Your job is to optimize each step incrementally.

**Target numbers for a viable campaign:**
```
100 emails sent
→ 45 opens       (45% open rate)
→ 5 replies      (5% reply rate)
→ 2 positive     (2% positive reply rate)
→ 1 call booked  (50% of positives book)
→ 0.2 clients    (20% close rate)

To close 1 client/month → send ~500 emails/month
```

---

## 4-Part System

```
1. Infrastructure   → Sending setup (domains, inboxes, warm-up)
2. List Building    → ICPs, targeting, enrichment
3. Copywriting      → Subject lines, openers, sequences
4. Follow-Through   → Booking, showing up, closing
```

None of the 4 can be skipped. A great list with bad copy fails. Great copy with bad infrastructure hits spam.

---

## Part 1: Infrastructure

### Domain Setup
```
Primary domain:     yourcompany.com    ← Never send cold email from this
Sending domain:     yourcompany.io     ← Dedicate 1–2 domains per campaign
Inbox:              firstname@yourcompany.io
```

### Technical Requirements
```
SPF record:   Set up on all sending domains
DKIM:         Configure via Instantly/Smartlead settings
DMARC:        p=none to start; monitor for 30 days
MX records:   Point to Google Workspace or Microsoft 365
```

### Warm-Up Protocol
```
Week 1–2:   10–15 emails/day (warm-up pool only — Instantly/Smartlead does this)
Week 3:     25 emails/day (start real outreach)
Week 4+:    50–100 emails/day per inbox
```

**Rule:** Never skip warm-up. Sending cold on a new domain = immediate spam folder.

### Inbox Ratio
- 1 inbox per 30–50 cold emails/day maximum
- Scale by adding inboxes, not by increasing volume per inbox

---

## Part 2: List Building

### Ideal Customer Profile (ICP)

Before building any list, answer:
```
Who:       [Job title] at [company type]
Size:      [X–Y employees]
Signal:    [Hiring / funded / expanding / posting content]
Geography: [Country/region]
Exclusions:[Industries to avoid / company types to skip]
```

### List Sources (in order of quality)

| Source | Quality | Cost | Notes |
|--------|---------|------|-------|
| Explorium | Very high | Paid | AI-enriched, intent signals |
| Apollo | High | Freemium | Large database, good filters |
| ListKit | High | Paid | Daniel Fazio's own tool |
| LinkedIn Sales Nav | High | Paid | Manual, but most accurate |
| Hunter.io | Medium | Freemium | Domain-based email finding |

### List Hygiene
- Verify all emails before sending (use NeverBounce or ZeroBounce)
- Remove generic addresses (info@, hello@, admin@)
- Max 2% bounce rate — anything above tanks deliverability

---

## Part 3: Copywriting

### Subject Line Rules
- Under 7 words
- No all-caps, exclamation marks, or spam trigger words
- Should feel like an internal email, not marketing
- Test 3 variations minimum (use spintax)

**What works:**
```
"quick idea for [company]"
"[first name] — had a thought"
"[mutual connection / reference]"
"question about [specific thing]"
```

**What kills open rates:**
```
"RE: Our conversation"       ← deceptive
"🚀 Double your revenue"     ← spam trigger
"URGENT: Limited time offer" ← obvious pitch
```

### Opening Line Rules
- Reference something SPECIFIC to this person
- Under 20 words
- Never start with "I" — start with "Saw", "Noticed", "Your", "Congrats"
- Never: "I came across your profile", "I hope this email finds you well"

### Body Copy Rules
- Under 80 words for Email 1
- One idea only — no feature lists
- Proof in Email 2, not Email 1
- Break-up in Email 3

See [Email Marketing Agent](../03-AI-AGENTS/email-marketing-agent.md) for full sequence templates.

### The 7-Touch DM / Social Follow-Up Sequence (Rohan's System)

For social outreach (LinkedIn DM, Instagram, Twitter) where email isn't available, use this 7-touch pattern before archiving a prospect:

| Touch | Content | Timing |
|---|---|---|
| 1 | Permission-needed opener: "Noticed [specific thing]. Have an idea — okay if I share it?" | Day 1 |
| 2 | Quick check-in if no reply: "Hey [Name], just wanted to bump this up" | Day 3–4 |
| 3 | Meme or light humor relevant to their niche | Day 6–7 |
| 4 | Free value drop: share a tip, framework, or resource — no ask | Day 9–10 |
| 5 | Quick check-in: "Any thoughts on what I sent?" | Day 13–14 |
| 6 | Second free value drop (different format from Touch 4) | Day 17–18 |
| 7 | Breakup message: "I'll assume now's not the right time. I'll check in a few months — no hard feelings." | Day 21–22 |

**Why this works:** Most prospects aren't ignoring you — they're busy. The breakup message at Touch 7 often generates more replies than touches 2–6 combined. People respond when they think you're leaving.

**Rule:** Space each touch at least 2–3 days apart. Never send two messages in one day. Never apologize for following up.

**4 metrics to track for social outreach:**
```
Messages sent this week:    ________
Reply rate:                 ________%
Calls booked:               ________
Deals closed:               ________
```

If reply rate < 10% on social DMs: rewrite your opener or target a different ICP.

---

## Part 4: Follow-Through

### Reply Handling (within 24 hours)

| Reply type | Response |
|-----------|----------|
| "Interested, tell me more" | Send 1-paragraph case study + calendar link |
| "Not the right time" | "Totally fine — mind if I check back in 3 months?" |
| "Who referred you?" | "Nobody — found you via [honest source], [reason why relevant]" |
| "Remove me" | Remove immediately. Reply: "Done — sorry for the interruption." |
| No reply (sequence ended) | Move to quarterly re-touch list |

### Booking Call
- Use Calendly with 15-min intro slot
- Set timezone detection on
- Send confirmation + reminder emails automatically
- Have a short agenda in the confirmation: "We'll cover [X, Y, Z] — you'll leave knowing whether this makes sense for you"

### Pre-Call Prep
Before every call, research:
- Company revenue range (approximate)
- Recent news or LinkedIn posts
- Their current pain point (hiring? launching product? new funding?)
- Competitor they reference in content

---

## Weekly Operating Rhythm

| Day | Activity |
|-----|---------|
| Monday | Upload new prospects to campaign, review last week's stats |
| Tuesday–Thursday | Monitor replies, handle conversations |
| Friday | QA subject line performance, A/B test rotation |
| Weekly | Analyze: open rate, reply rate, call bookings |

---

## Metrics Dashboard (track weekly)

```
Sent this week:          ________
Open rate:               ________%
Reply rate:              ________%
Positive reply rate:     ________%
Calls booked:            ________
Calls completed:         ________
Proposals sent:          ________
Clients closed:          ________
```

If open rate < 30%: fix subject lines.
If reply rate < 2%: fix opening lines or offer.
If positive reply rate < 0.5%: fix the offer or niche.
If calls → clients < 20%: fix the sales conversation.

---

## Troubleshooting

| Problem | Root Cause | Fix |
|---------|-----------|-----|
| Emails going to spam | Domain reputation | Check SPF/DKIM/DMARC, reduce volume |
| Low open rate (<25%) | Subject lines | Test 5 new subjects this week |
| High open, low reply | Body copy | Rewrite opener + CTA |
| Replies but no calls | Offer unclear | Simplify the ask: "15-min call?" |
| Calls but no closes | Sales process | See [sales-call-script.md](../05-SALES-SYSTEM/sales-call-script.md) |
