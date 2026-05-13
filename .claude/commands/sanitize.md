---
description: Turn a repo artifact, workflow, or report into a shareable version without leaking private project details.
---

# Sanitize

Create a public-safe version of a file, snippet, command, or workflow.

## Input

$ARGUMENTS

## Process

1. Identify sensitive material such as:
   - ticket keys and identifiers
   - internal URLs, space IDs, and page IDs
   - service names, codenames, and customer names
   - usernames, machine paths, and local environment details
   - secrets, tokens, or private command permissions
2. Replace them with safe placeholders while preserving the structure and logic.
3. Keep the useful workflow intact so the output still teaches the pattern.
4. Return one of:
   - sanitized markdown or text
   - a patch plan for sanitizing files
   - a short list of replacements made

## Safe Replacement Patterns

- `PROJ-123` instead of a real ticket key
- `https://your-company.example/...` instead of a live URL
- `your-service`, `your-project`, `your-team` instead of internal names
- `docs/reports/` or `backlog.json` instead of a private destination

## Rules

- Never output secrets verbatim.
- Preserve the lesson, not the residue.
- If you are unsure whether something is sensitive, replace it.
- Ask for human review when the stakes are high.

