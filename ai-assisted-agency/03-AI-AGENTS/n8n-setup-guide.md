# N8N AI Agent Setup Guide

## Why N8N

N8N is the fulfillment backbone of an AI-assisted agency.

| Feature | Why It Matters |
|---------|---------------|
| Visual drag-and-drop builder | No coding required |
| 400+ app integrations | Connect anything |
| Host AI models inside workflows | No external complexity |
| Self-hostable | No vendor lock-in |
| Free tier available | Start at $0 |

> "In an afternoon you can build what used to cost $10,000 in developer fees."

---

## How Agents Work: 3 Components

```
TRIGGER  →  AI AGENT BRAIN  →  ACTIONS
```

| Component | What It Does | Examples |
|-----------|-------------|---------|
| **Trigger** | Starts the workflow | Schedule, webhook, chat message, form |
| **AI Brain** | Receives context + goal, uses tools | GPT-4.1, Claude, Gemini |
| **Actions** | What the agent executes | Send email, write to Sheet, scrape LinkedIn |

### System Message vs User Message
- **System message** = Agent's role, rules, and behavior ("You are a cold email specialist…")
- **User message** = The specific task right now ("Find 5 SaaS CEOs who are hiring…")

---

## What Agents Can and Can't Do

**Good at:**
- Repetitive tasks running 24/7 without you
- Research and data aggregation across sources
- Writing first drafts from templates and examples
- Moving data between systems automatically

**Not good at:**
- Replacing human judgment and strategy
- Running an entire business autonomously
- Perfect output — always requires human QA before client delivery

**Rule:** AI removes the busy work. You handle strategy, relationships, and quality review. Human-in-the-loop is non-negotiable.

---

## Setup: Cloud vs Self-Hosted

### Cloud (Start Here)
- n8n.io → sign up → build immediately
- $20–50/month
- No server management

### Self-Hosted (Scale)
- Deploy on Hetzner/DigitalOcean/Railway (~$5–20/month server)
- No execution limits
- Recommended when serving 5+ clients

---

## Required Integrations

| Tool | Purpose | Cost |
|------|---------|------|
| **Explorium MCP** | B2B prospect database for AI | Paid |
| **Apify** | LinkedIn scraping (posts for personalization) | Free tier |
| **Google Sheets** | Prospect list output | Free |
| **Claude API or OpenAI** | AI model for reasoning/writing | Pay per token |
| **Instantly / Smartlead** | Cold email sending infrastructure | $37–99/month |

---

## 3 Agents to Build First

1. **[Lead Gen Agent](lead-gen-agent.md)** — Finds prospects, researches them, writes personalized first lines, exports to Sheets
2. **[Email Marketing Agent](email-marketing-agent.md)** — Writes multi-step sequences with spintax and follow-up logic
3. **[Content Agent](content-agent.md)** — Creates social posts, scripts, blog articles in client's voice

---

## Architecture Principles

**One agent = one job.** Don't build monster workflows. Separate:
- Agent A: Research prospects
- Agent B: Write personalization
- Agent C: Export to sending tool

**Sub-agents for structured tasks.** For repeatable output (write to Sheet, send Slack message), create a tiny sub-agent with only the tools it needs.

**Test on your own business first.** Run the agent against 10 prospects in your own niche. Review every output manually. Refine the system prompt. Only then deploy for a client.

---

## Common System Prompt Patterns

```
"You are a [role]. Use [tool] for every request.
Never make anything up — only use verifiable data.
Minimize tool calls to ensure speed.
Always return [required fields].
Never ask follow-up questions — reason through ambiguity yourself."
```

---

## Troubleshooting

| Problem | Fix |
|---------|-----|
| Agent inventing information | Add: "Only write from verified data. Never fabricate." |
| Too slow / too many calls | Add: "Minimize tool calls. Get all data in one pass." |
| Inconsistent output format | Add explicit format instructions with an example |
| Agent silently fails | Add error-handling fallback node after AI agent |
