# Content Creation Agent

## What It Does

Turns a voice note or written brief into a full week of client content — LinkedIn posts, email newsletters, and video scripts — all written in the client's voice.

**Output per run:**
- 5 LinkedIn posts (with hook variations)
- 1 email newsletter
- 1 video script (optional)
- All in the client's established voice and style

---

## Agent Architecture

```
[Voice Note / Written Brief]
    ↓
[Transcription Node]      ← Whisper API: audio → raw transcript
    ↓
[Writing Agent]           ← Claude trained on client voice → structured content
    ↓
[Image Generation]        ← Midjourney MCP (optional): creates post visuals
    ↓
[Scheduling / Export]     ← Google Sheets or Notion: stages content for review
```

---

## Building the Client Voice Model

Before running the agent, collect voice training data from the client.

### What to Collect
```
- 50–200 existing pieces of content (posts, emails, articles)
- 3–5 pieces the client is most proud of
- Answers to voice guide questions (see below)
```

### Voice Guide Q&A (send to client)
```
1. How would you describe your writing style in 3 words?
2. Topics you never talk about?
3. Words or phrases you use constantly?
4. Words or phrases you hate?
5. What's your typical CTA — buy, follow, reply, share?
6. Do you curse? Use slang? Write formally or casually?
7. Paste 3 posts you've written that feel most "you."
```

### Voice Guide Template (inject into system prompt)
```
VOICE PROFILE:
- Tone: [casual/formal/direct/storytelling]
- Sentence length: [short punchy / medium / long flowing]
- Common phrases: [list from client]
- Banned words/phrases: [list from client]
- Signature CTA style: [description]
- Industry vocabulary: [sector-specific terms they use]
- Personal details to reference: [company name, location, specific results]
```

---

## Node 1: Transcription Node

**Tool:** Whisper API (via N8N HTTP node or OpenAI integration)

**Input:** Voice note file (MP3/M4A from client WhatsApp, email, or Telegram)

**Output:** Raw transcript text passed to Writing Agent

**System Prompt:**
```
You are a transcription assistant. Convert the audio transcript into clean text.
Preserve the speaker's natural language, including informal phrasing.
Do not paraphrase, improve grammar, or change vocabulary.
Output: clean transcript only, no commentary.
```

---

## Node 2: Writing Agent

**Model:** Claude Sonnet (best at style mimicry and structured output)

**System Prompt Template:**
```
You are a professional ghostwriter. Your job is to produce content
that sounds exactly like [CLIENT NAME].

[PASTE VOICE PROFILE HERE]

Content rules:
- Match their vocabulary, not generic marketing language
- Hook format: lead with tension, curiosity, or a bold statement
- Never use: "In today's fast-paced world", "Game-changing", "Leverage synergies"
- CTAs must match their style (never use "Check the link in bio" unless they do)
- Every piece must be review-ready — no placeholders or [brackets]

You will receive a brief or transcript. Transform it into:
1. Five LinkedIn posts (include 3 hook variations per post)
2. One email newsletter (~300 words)
3. One short-form video script (optional — only if brief mentions video)
```

**User Prompt:**
```
Here is this week's content brief from [CLIENT NAME]:

[TRANSCRIPT OR WRITTEN BRIEF]

Produce all content formats. Output as structured sections:
## LinkedIn Posts
## Email Newsletter
## Video Script (if applicable)
```

---

## LinkedIn Post Generator

### Hook Formula Library

Include in system prompt for variety:
```
Hook types to rotate:
1. Contrarian: "Everyone says [X]. They're wrong."
2. Number: "[N] things I learned after [result/event]"
3. Story: "In [year], I [did thing]. Here's what happened."
4. Question: "Why do [most people] [fail at X]?"
5. Bold statement: "[Strong claim]. Here's the proof."
6. Personal failure: "I lost/failed/wasted [X]. Then I did [Y]."
```

### Output Format Per Post
```
POST [N]:
Hook Option A: [version 1]
Hook Option B: [version 2]
Hook Option C: [version 3]

Body:
[Content — 3–7 short paragraphs or bullets]

CTA:
[Single CTA in client's style]

---
```

---

## Email Newsletter Generator

**Format:**
```
Subject line 1: [Option A]
Subject line 2: [Option B]

Preview text: [One line — continues the subject line's tension]

Body:
[Opening line — expands on subject]
[Main insight or story — 2–3 paragraphs]
[Takeaway or lesson]
[CTA — one ask only]

Signature: [Client's name/style]
```

---

## Video Script Generator

**Format:**
```
HOOK (0–3 sec): [What stops the scroll]
SETUP (3–15 sec): [Context — why this matters]
CONTENT (15–45 sec): [Main value — teach, reveal, or story]
CTA (45–60 sec): [Single ask: follow, comment, DM]

B-roll notes: [Optional — what to film to support each section]
```

---

## Real Example: Lucas's Newsletter Automation

Lucas, a finance educator, built this workflow:
1. Records 2-minute voice note each week about a finance topic
2. Whisper transcribes it
3. Writing agent rewrites in his newsletter voice
4. Custom Midjourney prompt creates a header image in his visual style
5. Output staged in Notion → he reviews and hits publish

**Result:** Newsletter from idea to staged draft in ~15 minutes. He records the voice note on a walk.

---

## Running the Agent

1. Client sends voice note (WhatsApp, Telegram, or email attachment)
2. Upload to N8N trigger (webhook or manual)
3. Whisper transcribes → writing agent produces content
4. Review staged output in Google Sheets or Notion
5. **QA every post before scheduling**
6. Schedule via Buffer, Publer, or copy-paste to native platform

---

## Quality Checklist Before Publishing

- [ ] Every post sounds like the client (not generic AI content)
- [ ] No banned words or phrases from voice guide
- [ ] Hook creates genuine curiosity or tension
- [ ] Body delivers on the hook's promise
- [ ] One CTA only — no stacked asks
- [ ] Email subject line is specific, not clickbait
- [ ] No emojis unless client uses them
- [ ] No "In conclusion" or summary-style endings
