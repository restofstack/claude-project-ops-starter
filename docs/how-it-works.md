# How It Works

This starter uses a layered context model instead of trying to solve everything with a single giant prompt.

## Layer 1: Repo Guardrails

`CLAUDE.md` defines the rules that should be true in every session.

Examples:

- what not to do
- how to prioritize work
- how to report status

## Layer 2: Curated Durable Context

`docs/maintainers/` is where you put the context that should survive beyond a single session:

- architecture
- service boundaries
- local development instructions
- release notes and runbooks

This is better than stuffing all of that into `CLAUDE.md`.

## Layer 3: Working Memory

`.workspace-temp/context-db.json` is intentionally lightweight. It stores rolling memory like:

- what was shipped recently
- current branch and PR context
- decisions worth remembering
- estimate patterns

## Layer 4: Systems of Record

Claude should synthesize from your real systems of record, not replace them:

- backlog tool
- PR system
- release history
- docs or wiki

## Commands as the Orchestration Layer

The command files in `.claude/commands/` pull those layers together into reusable workflows.

Examples:

- planning and capture: `/standup`, `/bug`, `/rfe`
- memory and handoff: `/reflect`, `/checkpoint`
- durable learning: `/docs-sync`, `/root-cause`
- publishing and sharing: `/weekly-report`, `/release-notes`, `/sanitize`
