# DOCS/

Stable references. Read-once-per-topic documentation for tools, integrations, and decisions you've made that compound.

## What goes here

- Platform-specific docs (if not already in `AUTOMATION/platform-templates.md`)
- Third-party tool docs (SparkLoop setup, Stripe integration, etc.)
- Process documentation that's stable over 6+ months
- Onboarding docs if you hire help

## What does NOT go here

- Living documents (those live in their proper folder)
- Decisions (→ `CONTEXT/decisions-log.md`)
- Drafts or editing work
- Analytics (→ `PUBLISHING/analytics.md`)

## Structure

Suggested files as needed:

```
DOCS/
├── stripe-setup.md        (only if Stripe integration)
├── sparkloop-config.md    (only if SparkLoop active)
├── domain-dns.md          (if custom domain, DNS records for reference)
├── sponsor-standard-contract.md
├── client-standard-contract.md
└── onboarding-for-help.md (if you hire a VA or collaborator)
```

## Rules

- Each DOCS/ file is a REFERENCE, not a workflow — you read it when needed, don't edit it weekly
- If a DOCS/ file changes monthly or more often, it doesn't belong here — move to the appropriate living folder
- Dated entries for material changes (so you can see which version was current when)

## Cascade behavior

- Reference DOCS/ files when user asks setup questions
- Propose NEW DOCS/ files when user writes down setup/config that would be useful to reference later
- Don't auto-update DOCS/ — these are intentional snapshots
