---
description: Create release notes or a shipped-work summary from commits, PRs, and issue context.
---

# Release Notes

Create concise release notes from real shipping signals.

## Default Destination

If no external publishing target is configured, write the notes to:

`docs/releases/YYYY-MM-DD-release-notes.md`

## Process

1. Gather shipped signals:
   - merged PRs
   - release tags
   - relevant commits
   - issues closed by shipped work
2. Group changes by user-facing outcome or theme.
3. Call out:
   - fixes
   - breaking changes or migrations
   - manual rollout steps
   - follow-up risks
4. Publish to the configured destination or return a paste-ready markdown draft.

## Output Format

```markdown
# Release Notes

**Date:** YYYY-MM-DD

## Highlights

- <major shipped outcome>

## Fixes and Improvements

- <notable improvement>

## Breaking Changes or Migrations

- <change, or "None">

## Follow-Ups

- <known follow-up>
```

## Rules

- Write for humans, not commit logs.
- Prefer grouped outcomes over raw ticket dumps.
- Never claim something shipped unless the signals support it.

