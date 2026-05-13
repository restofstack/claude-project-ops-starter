# Claude Project Ops Starter

A Claude Code starter for running project operations through a few repeatable workflows instead of one-off prompts.

This starter is opinionated about the pattern, not the products:

- Your backlog can be Jira, GitHub Issues, Linear, Asana, or a local JSON file.
- Your published context can be Confluence, a `docs/` folder, MkDocs, Obsidian, Notion, or dated markdown files.
- Your working memory can stay as a local JSON file until you outgrow it.

## What is in here

- `.claude/commands/` for reusable Claude Code workflows
- `CLAUDE.md` for repo-level operating rules
- `docs/maintainers/` for curated durable context
- `templates/` for cross-session memory and reporting templates
- `docs/adapters/` for swapping tools without changing the overall pattern

## Core idea

Claude works better on real projects when it has four stable context layers:

1. Repo guardrails in `CLAUDE.md`
2. Curated technical context in `docs/maintainers/`
3. Lightweight working memory in `.workspace-temp/context-db.json`
4. Real systems of record for backlog, docs, PRs, and releases

The commands in `.claude/commands/` sit on top of those layers and turn them into repeatable workflows like:

- planning and capture: `/standup`, `/bug`, `/rfe`
- memory and learning: `/reflect`, `/checkpoint`, `/root-cause`, `/docs-sync`
- publishing and sharing: `/weekly-report`, `/release-notes`, `/sanitize`

## Quick Start

1. Copy this repo or the parts you want into your project.
2. Create `.workspace-temp/context-db.json` from `templates/context-db.template.json`.
3. Customize the command files to match your backlog and publishing targets.
4. Add or trim `docs/maintainers/` until Claude has the minimum useful durable context.

## Suggested first customizations

- Replace placeholder project keys, labels, and URLs in `.claude/commands/`
- Decide where weekly reports should land by default
- Decide whether release notes and incident notes should live in `docs/` or an external system
- Adjust the priority labels to match your team
- Keep `CLAUDE.md` short and move heavier context into `docs/maintainers/`

## Share safely

Before making your setup public, read `docs/sanitize-before-sharing.md`.
