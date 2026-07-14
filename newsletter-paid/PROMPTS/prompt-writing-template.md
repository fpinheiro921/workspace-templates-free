# Prompt Writing Template

Local pointer. Canonical version: `_PATTERNS/prompt-library-standard.md`.

## Quick reference

Every prompt has 5 parts:
1. Introduction (What / How / Why)
2. Instruction
3. Context (Rules + Positive Attributes + Examples)
4. Final Delivery
5. Iteration (lives in the file's iteration log, not in the prompt)

## Checklist before committing

- [ ] Uses shape from `_PATTERNS/prompt-library-standard.md`
- [ ] Specific role (not "You are a writer")
- [ ] Every rule has a reason
- [ ] 3+ examples that MATCH the rules
- [ ] Tested on ≥2 models
- [ ] Model recommendation in front-matter
- [ ] Iteration log has "created" entry

## Credits

Meta-structure from Ghostwriter GPT Bonus Module 11. See `_PATTERNS/attribution-rules.md`.
