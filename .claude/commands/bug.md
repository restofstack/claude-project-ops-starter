---
description: Capture a bug cleanly in the configured backlog system or produce a paste-ready bug record.
---

# Bug

Capture a bug report without turning it into a full investigation.

## Input

$ARGUMENTS

## Process

1. Read the bug description.
2. Ask 1-2 clarifying questions only if critical details are missing.
3. Check for likely duplicates in the backlog system if one is available.
4. Create the bug in the configured backlog system.
5. If no write integration exists, produce a paste-ready markdown entry.

## Bug Template

```markdown
## Symptoms

What the user sees.

## Steps to Reproduce

1. Step 1
2. Step 2
3. Expected result
4. Actual result

## Impact

Who is affected and how badly.

## Likely Root Cause

Best current guess.
```

## Severity Guidance

- `critical`: data loss, security issue, or complete outage
- `high`: major feature broken, no workable path
- `medium`: partial breakage or a workable workaround exists
- `low`: edge case, polish, or cosmetic issue

## Rules

- Keep it concise.
- Do not start implementing the fix.
- If the backlog is local only, return a clean markdown block plus suggested labels.

