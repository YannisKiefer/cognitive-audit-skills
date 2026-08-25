# Contributing

## The Filter

Every contribution must pass:

> **Would this still be interesting if the subject already knew it?**

Generic productivity wisdom fails by definition. Patterns that took months
of interactions to form pass.

## Rules for new skills

1. Format: `<skill-name>/SKILL.md` with YAML frontmatter (`name`,
   `description` starting with "Use this...").
2. Plain English. Short sentences. A smart 12-year-old should follow it.
3. Structure: The Big Idea -> The Method -> When It Backfires ->
   One-Line Memory.
4. No copyrighted text from any paper or book. Original phrasing only.
   Citing a source as inspiration is fine and encouraged.
5. No clinical or personality labels. Ever. Work behavior only.
6. Every claim type must specify its own evidence bar and counterevidence
   requirement.
7. Max ~130 lines per skill.

## Process

1. Open an issue describing the analysis gap: what question about work
   behavior currently has no skill behind it.
2. PR with the new skill folder + README table row.
3. CI validates frontmatter automatically.

## Lint locally

```bash
python3 scripts/lint.py
```
