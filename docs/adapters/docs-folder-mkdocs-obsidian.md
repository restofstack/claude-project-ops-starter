# Adapter: Docs Folder, MkDocs, or Obsidian

This is the simplest publishing layer if you want everything close to the repo or in markdown.

## Published Context

Good targets:

- `docs/reports/` inside the repo
- an MkDocs site built from `docs/`
- an Obsidian vault folder synced however you prefer

## Good Uses

- weekly reports
- product notes
- decision logs
- release summaries

## Why this works well

- markdown is easy for Claude to read and write
- no extra wiki integration is required
- public and private variants are easy to separate

## Suggested paths

- `docs/reports/YYYY-MM-DD-status.md`
- `docs/decisions/YYYY-MM-DD-<topic>.md`
- `docs/maintainers/` for curated repo context

