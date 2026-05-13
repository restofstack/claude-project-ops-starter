# Sanitize Before Sharing

Before publishing your Claude setup, remove or replace:

- real Jira, GitHub, Linear, or Asana identifiers
- real Confluence space IDs, page IDs, and internal URLs
- customer names, project codenames, and ticket titles
- local usernames and machine-specific absolute paths
- secrets, API tokens, and private command permissions
- screenshots that reveal internal branch names, issues, or metrics

## Safe Replacements

- `PROJ-123` instead of a real ticket key
- `https://your-company.atlassian.net/...` instead of a live URL
- `docs/reports/` instead of a real wiki location
- `your-service`, `your-team`, `your-project` instead of internal names

## Files Usually Kept Private

- `.claude/settings.local.json`
- live `.workspace-temp/context-db.json`
- any repo-specific secrets or allowlists

If you are turning a private workflow or report into a public artifact, use the `sanitize` command first and then review the result manually.
