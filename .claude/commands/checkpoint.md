---
description: Capture an end-of-session handoff so the next Claude session can restart quickly.
---

# Checkpoint

Record the current state of work in `.workspace-temp/context-db.json`.

## Input

$ARGUMENTS

## Process

1. Read `.workspace-temp/context-db.json` if it exists.
2. Inspect the current local state:
   - branch
   - uncommitted changes
   - recent commits
   - open PRs if that signal exists
3. Summarize:
   - current focus
   - blockers or open questions
   - the next 1-3 concrete steps
4. Append a short session entry to the `sessions` list.
5. Confirm the checkpoint in 3-5 concise lines.

## Suggested Session Shape

```json
{
  "date": "YYYY-MM-DD",
  "branch": "feature/example",
  "summary": "Implemented X and investigated Y",
  "blockers": ["Need decision on Z"],
  "next_steps": ["Finish validation", "Open PR"]
}
```

## Rules

- Prefer concrete next steps over narrative.
- Mention if uncommitted changes are present.
- Keep entries short and easy to skim.
- This is handoff memory, not a diary.

