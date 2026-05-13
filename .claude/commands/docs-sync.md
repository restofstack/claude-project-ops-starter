---
description: Update maintainer docs after meaningful code, workflow, or architecture changes.
---

# Docs Sync

Keep `docs/maintainers/` aligned with the current code and workflow.

## Input

$ARGUMENTS

## Process

1. Inspect the changed files or described work.
2. Identify what durable context changed:
   - architecture
   - service boundaries
   - local development instructions
   - runbooks
   - release notes
3. Update the smallest relevant file in `docs/maintainers/`.
4. If no relevant doc exists, create a concise new note in the right folder.
5. Summarize what changed and what still needs human confirmation.

## Rules

- Trust code over stale docs.
- Do not invent behavior that is not visible in code or clearly stated by the user.
- Keep maintainers docs concise and high-signal.
- Prefer editing existing docs over creating near-duplicates.

