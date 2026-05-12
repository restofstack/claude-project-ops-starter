---
description: Create a durable weekly project status report and publish it to the configured destination.
---

# Weekly Report

Create a concise weekly project report from real project signals.

## Default Destination

If no external publishing target is configured, write the report to:

`docs/reports/YYYY-MM-DD-status.md`

## Optional Destinations

- Confluence
- Notion
- Google Docs
- MkDocs-backed `docs/`
- Obsidian vault folder

## Process

1. Gather signals:
   - recent merged or shipped work
   - open backlog by priority
   - in-progress work
   - major risks
   - relevant notes from `.workspace-temp/context-db.json`
2. Group shipped work into themes instead of dumping tickets.
3. Summarize backlog health and open risks.
4. Publish to the configured destination.

## Report Format

```markdown
# Weekly Status

**As of YYYY-MM-DD**

## TL;DR

<one short paragraph>

## Shipped This Week

- <theme or milestone>

## Backlog Health

- Total open: <count>
- In progress: <count>
- Highest-priority open items: <summary>

## Risks

1. <risk>
2. <risk>

## Recommended Calls

1. <decision or follow-up>
2. <decision or follow-up>
```

## Rules

- Use absolute dates.
- Never fabricate numbers or backlog items.
- Keep it short enough to scan quickly.

