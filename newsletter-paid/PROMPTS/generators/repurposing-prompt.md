# Repurposing Prompt (Newsletter → Short-Form)

**When to use:** after publishing a newsletter, extract 3-5 tweets + 1-2 LinkedIn posts.

## This is a thin pointer

The canonical generator lives at `creator-studio/PROMPTS/generators/repurposing-prompt.md`. It handles all platforms + formats.

**Newsletter-specific usage notes:**

- Input: the FULL newsletter text (not outline — needs paragraph detail)
- Target platforms: Twitter (3-5 tweets) + LinkedIn (1-2 posts)
- Skip the video/Instagram/callout sections unless you're producing those regularly

## Quick usage

```
Use the prompt at `creator-studio/PROMPTS/generators/repurposing-prompt.md`
with these inputs:
- Source: <paste full newsletter text>
- Target platforms: Twitter, LinkedIn
- Nugget priorities: <optional — specific paragraphs you want highlighted>
```

## Why we don't duplicate here

Repurposing logic is identical across templates. Maintaining two copies = drift risk. Canonical copy in creator-studio; this file points there.

## If you're only running newsletter-paid (not creator-studio)

Copy the full generator content from `creator-studio/PROMPTS/generators/repurposing-prompt.md` into this file. Flag in your `.windsurfrules` that creator-studio isn't a sibling in your setup.

## Iteration log

- 2026-04-18: created as pointer to creator-studio canonical version
