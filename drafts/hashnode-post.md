# My Claude Code Project Ops Starter

## Subtitle

How I use Claude Code with lightweight memory, reusable workflows, and a few systems of record instead of a giant prompt.

## Draft

The useful part of my setup is not Jira, Confluence, or any one tool. The useful part is that Claude has a few stable places to look and a few repeatable workflows to run.

I ended up with four context layers:

1. `CLAUDE.md` for repo-level guardrails
2. `docs/maintainers/` for curated durable context
3. `.workspace-temp/context-db.json` for rolling working memory
4. real systems of record for backlog, PRs, releases, and published status

On top of that, I use a handful of commands that keep turning vague requests into the same repeatable operations:

- `/standup` for “what should I work on next?”
- `/bug` for clean issue capture
- `/rfe` for idea capture without over-specifying
- `/reflect` for small bits of memory that help future sessions
- `/weekly-report` for durable status snapshots

The important part is that each layer has a job.

`CLAUDE.md` is not where I dump the whole project brain. It stays short and sets the non-negotiables. Heavier context goes into maintainers docs. That gives Claude a better entry point and makes the setup more useful for humans too.

The local JSON memory file is deliberately boring. It is not a product database. It is just enough session memory to remember recent work, branch context, decisions, and estimate patterns. The reason I like this is simple: zero extra service to run, zero startup tax, and I can change the schema whenever I want.

The backlog and reporting layers are swappable. I use one stack today, but you could map the same pattern to GitHub Issues and a `docs/` folder, or even to a plain `backlog.json` file if the project is small.

That is also why I split the public starter into roles instead of products:

- backlog system
- published context layer
- working memory
- repo guardrails
- reusable Claude workflows

If you already have your own tools, keep them. The point is to give Claude stable interfaces, not to rebuild your stack around one blog post.

## Suggested sections

1. The problem with default Claude usage on ongoing projects
2. The four context layers
3. Why I kept memory as JSON instead of introducing another service
4. The commands that changed the workflow
5. Why maintainers docs matter as much as prompts
6. How to swap Jira and Confluence for your own tools
7. What I made public and what I kept private

