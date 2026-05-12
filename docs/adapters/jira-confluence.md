# Adapter: Jira + Confluence

This is the closest match to the workflow that inspired this starter.

## Backlog

Use Jira as the source of truth for:

- bugs
- RFEs
- in-progress work
- backlog priority

Best fit:

- `bug.md`
- `rfe.md`
- `standup.md`

## Published Context

Use Confluence for durable weekly reports and status pages.

Best fit:

- `weekly-report.md`

## Notes

- Prefer MCP-backed auth over storing raw API tokens in prompts or docs.
- Keep cloud IDs, space IDs, and page IDs out of the public repo.

