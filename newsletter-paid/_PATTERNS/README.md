# _PATTERNS/ — How to Use This Folder

## What this is

A shared-craft knowledge layer for Windsurf templates. Not a template itself — reference material used BY templates.

## Who reads these files

- **Cascade (inside any workspace that references `_PATTERNS/`)** — reads at session start per the workspace's `.windsurfrules` context-loading protocol
- **Template authors** — cite `_PATTERNS/` files in new or updated templates instead of re-explaining frameworks
- **The human user** — occasionally, to refresh on a pattern or update it after a new insight

## When to reference a pattern in a new template

Decision tree:

```
Is the pattern already in _PATTERNS/?
├── Yes  → reference it in .windsurfrules + cite in the template file that uses it
└── No   → is it used in ≥2 templates (current + likely future)?
          ├── Yes → create the _PATTERNS/ file FIRST, then reference
          └── No  → keep the pattern local to the one template
```

Rule of thumb: **one template, keep it local. Two or more, promote to `_PATTERNS/`.**

## How to add a new pattern file

1. Check `index.md` to ensure it's not already covered
2. Use the file structure:
   ```markdown
   # <Pattern Name>

   ## What it is
   <1 paragraph>

   ## When to reference
   <which templates + use cases>

   ## The pattern
   <content, paraphrased from source>

   ## How to apply
   <concrete integration snippets>

   ## Credits
   <source attribution>

   ## Iteration log
   - YYYY-MM-DD: created
   ```
3. Add an entry to `index.md`'s registry table
4. Update any existing templates' `.windsurfrules` if they should now reference it

## How to update a pattern file

- Dated entry in the file's own `## Iteration log` section
- If the change is breaking (e.g. renamed a framework step), bump a `decisions-log.md` entry in every referring template and surface the change to the user before applying

## Ignore rules

- `_PATTERNS/` files are **private study references** where they adapt paid course content
- Add the whole folder to `.gitignore` if the templates root ever becomes a public repo
- Never ship `_PATTERNS/` files inside a template distribution — templates reference the path, users populate their own copy
