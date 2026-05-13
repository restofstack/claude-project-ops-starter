---
description: Capture the real cause of a bug and the fix so future sessions do not have to rediscover it.
---

# Root Cause

Turn a resolved bug into a short durable learning note.

## Input

$ARGUMENTS

## Process

1. Capture the symptom and impact briefly.
2. Identify the actual root cause, not just the failing component.
3. Record the fix that was applied.
4. Capture prevention or follow-up:
   - tests added
   - guardrails
   - docs updates
   - monitoring or alerts
5. Store the note in one of:
   - the bug ticket or issue comment
   - `.workspace-temp/context-db.json` as a pattern or decision
   - `docs/incidents/YYYY-MM-DD-<slug>.md` if durable reference is warranted

## Note Template

```markdown
# Root Cause Note

**Date:** YYYY-MM-DD
**Issue:** PROJ-123

## Symptoms

<what broke>

## Impact

<who was affected>

## Root Cause

<actual cause>

## Fix

<what changed>

## Prevention

- <test, doc, or monitoring follow-up>
```

## Rules

- Focus on evidence, not blame.
- Keep it concise enough that someone will read it later.
- Record prevention whenever possible.

