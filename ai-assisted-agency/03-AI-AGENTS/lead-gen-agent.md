# Lead Generation Agent

## What It Does

Automatically builds a prospect list and generates personalized cold email opening lines for each prospect — what would take 1+ hours manually happens in ~10 minutes.

**Output per run:**
- Prospect name, email, LinkedIn URL
- Job title and company info
- Personalized first line based on their recent LinkedIn activity
- All saved automatically to Google Sheets

---

## Agent Architecture

```
[Chat Trigger / Schedule]
    ↓
[Research Agent]          ← Explorium MCP: finds prospects matching criteria
    ↓
[First Line Writer]       ← Apify MCP: scrapes LinkedIn posts → Claude writes personalized opener
    ↓
[Google Sheets Sub-Agent] ← Appends all prospect data to tracking sheet
    ↓
[Email Campaign Writer]   ← Writes full sequence based on prospect data
```

---

## Node 1: Research Agent

**Model:** GPT-4.1 or Claude Sonnet

**Tools connected:**
- Explorium MCP (prospect database)

**System Prompt Template:**
```
You are a lead gen assistant. Use your Explorium MCP for every request.
Never make anything up — only use verifiable data from Explorium.
If LinkedIn is ever mentioned, include the prospect's LinkedIn URL.
Minimize tool calls to ensure speed.
Always return: prospect name, email, LinkedIn URL, job title, company info.
Never ask follow-up questions — reason through any ambiguity yourself.

[Paste accepted LinkedIn category list from Explorium docs here]
```

**User Prompt (how to trigger):**
```
Find me [N] [job title]s at [company type] companies
that employ between [X] and [Y] people
and are actively [hiring/expanding/recently funded].
```

Example:
```
Find me 10 CEOs of B2B SaaS companies that employ
between 10 and 50 people and are actively hiring.
```

---

## Node 2: First Line Writer

**Model:** Claude Sonnet (better at nuanced personalization)

**Tools connected:**
- Apify MCP (LinkedIn scraper)

**What it does:**
1. Receives prospect data + LinkedIn URLs from Node 1
2. Sends URLs to Apify → scrapes 5 most recent LinkedIn posts per prospect
3. Writes a personalized opening line based on recent activity
4. Passes all data to Google Sheets sub-agent

**System Prompt Template:**
```
You are a professional cold email personalization specialist.
Your task: create hyper-personalized opening lines based on LinkedIn data.

Rules:
- Reference something SPECIFIC from their recent posts or company news
- Never use generic compliments ("I love your content")
- Keep each line under 30 words
- Sound conversational, not corporate
- Never fabricate information

Good examples:
- "Saw your post about [specific topic] last week — [genuine reaction/connection]"
- "Noticed [company] just [specific recent event] — congrats"
- "Your [specific post] on [topic] resonated — we've seen the same pattern"

Bad examples:
- "I came across your profile and was impressed"
- "I noticed you're a leader in [industry]"
```

**User Prompt:**
```
Create a personalized cold email opening line for this prospect.
Write all data into Google Sheets.

Prospect data: [passed automatically from Node 1]
Task 1: Extract LinkedIn URL → research via Apify → find recent activity → write personalized line
Task 2: Write to Google Sheets: [name, email, linkedin, job_title, company, first_line, company_info]
```

---

## Node 3: Google Sheets Sub-Agent

**Purpose:** Write all prospect + personalization data to a tracking sheet

**Tools:** Google Sheets (get rows, append/update rows)

**Sheet columns:**
```
prospect_name | email | linkedin_url | job_title | company | 
first_line | company_info | date_added | status
```

---

## Node 4: Email Campaign Writer (Optional)

After prospect list is built, generate a full 3-step email sequence:

**System Prompt:**
```
You are a cold email copywriter. Write a 3-email sequence for this prospect.
Use spintax format: {option1|option2|option3} for subject lines and openers.
Email 1: Lead with the personalized first line. Present the offer briefly. CTA = book a call.
Email 2 (3 days later): Follow up with a case study or result. Different angle.
Email 3 (5 days later): Break-up email. Low pressure. Leave door open.
Keep all emails under 120 words.
```

---

## Running the Agent

1. Open N8N workflow
2. In the chat trigger, type your prospect criteria
3. Agent runs (~10 minutes for 10 prospects)
4. Open Google Sheet to review output
5. **QA every first line before importing to sending tool**
6. Import approved prospects + sequences to Instantly/Smartlead

---

## Quality Checklist Before Sending

- [ ] Every first line references something specific (not generic)
- [ ] No fabricated information
- [ ] All emails are under 150 words
- [ ] Subject lines are curiosity-driven (not spammy)
- [ ] Spintax variations all read naturally
- [ ] CTA is singular and frictionless (one ask per email)
