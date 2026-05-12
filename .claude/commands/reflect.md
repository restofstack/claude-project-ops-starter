---
description: Log a small amount of durable session memory for future Claude sessions.
---

# Reflect

Record a decision, pattern, or estimate result in `.workspace-temp/context-db.json`.

## Input

$ARGUMENTS

## Usage

- `/reflect decision: chose X over Y because Z`
- `/reflect pattern: frontend polish tasks usually take longer than expected`
- `/reflect estimate ISSUE-123 estimated 2d actual 3d`

## Process

1. Read `.workspace-temp/context-db.json`.
2. Based on the input type:
   - `decision`: append to the most recent session
   - `pattern`: append to the top-level `patterns` list if not duplicated
   - `estimate`: append to the top-level `estimates` list
3. Keep the file small and readable.
4. Confirm what was recorded in one line.

## Rules

- Keep entries brief.
- Prune old sessions periodically.
- This file is working memory, not a second product database.

