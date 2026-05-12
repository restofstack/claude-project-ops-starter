---
description: Use when running a daily standup, deciding what to work on next, or reviewing project health.
---

# Standup

Generate a concise project status snapshot and recommend the next best actions.

## Data Sources

Use the best available sources in this order:

1. `.workspace-temp/context-db.json`
2. `git status`, current branch, recent commits
3. Open PRs if the repo uses GitHub
4. Your configured backlog tool
5. Curated docs in `docs/maintainers/`

Backlog tool examples:

- Jira via MCP
- GitHub Issues via MCP or `gh`
- Linear or Asana via MCP/API
- `backlog.json` in the repo

## Process

1. Read `.workspace-temp/context-db.json` if it exists.
2. Check local git state:
   - current branch
   - uncommitted changes
   - recent commits
3. Check for open PRs if that signal exists.
4. Pull in-progress and ready backlog items from the configured backlog tool.
5. Identify stale work:
   - open PRs with no movement
   - branches with no PR
   - items marked in progress with no matching branch or recent commits
6. Recommend the top 3 next actions.

## Output Format

```text
Daily Status
<YYYY-MM-DD>

Since last session:
- <recent shipped or merged work>

Current work:
- Branch: <branch>
- Uncommitted: <yes/no>
- Open PRs: <summary>

In progress:
- <item>

Ready to pick up:
1. <item>
2. <item>
3. <item>

Stale work:
- <risk or stale branch/PR>

Recommendations:
1. <action>
2. <action>
3. <action>
```

## Rules

- Prefer finishing active work before suggesting new work.
- Keep the response under 40 lines when possible.
- Include non-code work if it materially affects project flow.
- If no external backlog tool is configured, say that clearly and use local context only.

