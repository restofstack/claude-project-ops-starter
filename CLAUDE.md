# CLAUDE.md

Guidance for Claude Code when working in this repository.

## Quick Reference

Start with the curated docs in `docs/maintainers/README.md`.

## Operating Rules

1. Prefer the existing system of record over inventing local state.
2. Finish work in progress before recommending new work.
3. Never fabricate backlog items, statuses, counts, or ticket links.
4. Keep reports scannable and action-oriented.
5. Use `docs/maintainers/` for durable technical context instead of overloading this file.

## Project Context Layers

- `CLAUDE.md`: repo guardrails and non-negotiables
- `docs/maintainers/`: curated technical context for humans and Claude
- `.workspace-temp/context-db.json`: rolling working memory
- Backlog + PRs + release history: execution truth

## Workflow Expectations

- `/standup` should synthesize current state, not dump raw data
- `/bug` and `/rfe` should capture work cleanly, not over-spec it
- `/reflect` and `/checkpoint` should keep memory short and cheap
- `/docs-sync` and `/root-cause` should preserve durable learning, not create noise
- `/weekly-report` should publish a durable snapshot somewhere searchable
- `/release-notes` should summarize shipped value, not commit history
- `/sanitize` should remove private residue while preserving the workflow
