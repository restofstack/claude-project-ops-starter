---
description: Capture a request for enhancement in the configured backlog system or produce a paste-ready story.
---

# RFE

Capture a feature idea or request for enhancement as a structured backlog item.

## Input

$ARGUMENTS

## Process

1. Read the idea.
2. Ask 2-3 clarifying questions only if the scope or beneficiary is unclear.
3. Check for likely duplicates in the backlog system if one is available.
4. Create the item in the configured backlog system.
5. If no write integration exists, return a paste-ready markdown entry.

## Story Template

```markdown
## Problem

What problem does this solve and who benefits?

## Proposal

What should change at a high level?

## User Story

As a <user>, I want <action> so that <benefit>.

## Notes

Any constraints, dependencies, or estimate hints.
```

## Priority Guidance

- `critical`: blocks launch, revenue, safety, or major commitments
- `high`: materially important this cycle
- `medium`: useful near-term improvement
- `low`: roadmap or backlog parking lot

## Rules

- Keep it as a capture workflow, not a full spec.
- Default to the simplest clear write-up.
- If no backlog integration exists, return a clean markdown block plus suggested labels.

