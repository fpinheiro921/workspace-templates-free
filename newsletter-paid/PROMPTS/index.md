# PROMPTS/ — Newsletter Generator Library

Reusable LLM prompts for this newsletter workspace. Follows the standard shape in `_PATTERNS/prompt-library-standard.md`.

## When to use which

| Situation | Generator |
|---|---|
| Have a topic, need an outline | `generators/idea-to-outline.md` |
| Have an outline, need a full draft | `generators/outline-to-draft.md` |
| Need 5 subject-line variants | `generators/subject-line-generator.md` |
| Newsletter published, need derivatives | `generators/repurposing-prompt.md` |
| Deconstructing a viral newsletter | `generators/mirror-prompt.md` |
| Authoring a new prompt | `prompt-writing-template.md` |

## Cross-template notes

Some generators in this template are thin pointers to `creator-studio/PROMPTS/generators/`:
- `repurposing-prompt.md` — cross-references creator-studio version
- `mirror-prompt.md` — cross-references creator-studio version

This avoids duplication. If you're running both templates, edit the canonical copy in creator-studio.

## Credits

Prompt structures adapted from Dickie Bush & Nicolas Cole's course prompts. See `_PATTERNS/attribution-rules.md`.
