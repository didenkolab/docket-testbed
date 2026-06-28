# Пирс — a docket testbed

An [docket](https://github.com/vadymdidenkolab/docket) vault belonging to a fictional payments
team, kept here so that docket is exercised against a workflow that is nothing like its defaults.

[docket-demo](https://github.com/vadymdidenkolab/docket-demo) shows what a vault looks like. This
one shows what a vault looks like when a real team has had it for a quarter: a deployment
pipeline instead of three columns, a vocabulary that is not English, an epic with sub-tasks
under it, tasks that block and duplicate and cause each other, labels that are pages, and
releases that are tags on a history somebody actually made.

Everything in it is invented. It is modelled on the *shape* of a real board — an eight-column
pipeline, types named in the team's own language at standard hierarchy levels — and on nothing
else.

## What it is here to catch

| | |
|---|---|
| **A pipeline, not a kanban** | Eight statuses, and a workflow that moves forward one stage at a time and back to `В работе` when a stage fails. A board with more columns than fit on a screen is the normal case, not the edge case. |
| **A vocabulary that is not English** | `Эпик`, `История`, `Задача`, `Подзадача`, `Баг`; `критичный`, `высокий`. Nothing in docket is allowed to assume its own defaults — which is why a type carries a `level` rather than being recognised by name. |
| **Non-ASCII everywhere it can be** | File names, links, tags, folders. Git escapes non-ASCII paths by default and a tracker that gets this wrong loses the history of half its tasks. |
| **Hierarchy** | Four epics, sub-tasks beneath tasks, and one task that is deliberately parented at the wrong level in a proposal branch. |
| **Relations** | `blocks`, `blocked_by`, `duplicates`, `duplicated_by`, `causes`, `caused_by`, `relates` — all seven, on tasks that plausibly have them. |
| **Labels as notes** | Every label in `docs/метки/` is a page. Open one in Obsidian and its backlinks are the tasks that carry it. |
| **A history worth reading** | Six weeks of commits by four authors, three tags, and a proposal on a branch. `git log`, the Releases page and the Branches page all have something to show. |

## Try it

```bash
docket check                      # the vault against the specification
docket serve                      # board, backlog, releases, branches
open -a Obsidian .               # the same files, as a graph
```

The board is at `http://localhost:8080`. `/releases` reads the tags; `/branches` lists the
proposals and draws the board each one would produce.

## A note on language

Prose *about* docket — this file, `AGENTS.md` — is in English, like the rest of the project.
The vault's own content is in the fictional team's language, because that is the point of it:
a tracker whose defaults are English has to work for a team whose words are not.
