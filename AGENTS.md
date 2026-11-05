# Repository instructions

## Start here

- Read the [documentation map](docs/overview.md) and [project status](docs/status.md),
  then follow their links for the task.
- Before proposing work, search the relevant records, Git history, and related
  pull requests for earlier decisions, existing plans, and verification gaps.
- Follow [development](docs/development.md) for repository setup and checks.
  Read the [configuration contract](docs/configuration-contract.md) before
  changing configuration ownership or tooling.
- Follow the [change workflow](docs/change-workflow.md) for implementation and
  handoff. Use the [runbook index](docs/runbooks/README.md) for documented
  operations and recovery procedures.

## Documentation workflow

Before creating a document, search the documentation map, tracked and untracked
Markdown files, and related pull requests for an existing record. Update that
record when its purpose is the same.

Update the existing authoritative record when durable project knowledge changes.
Create a document only when it serves a distinct ongoing purpose that existing
records cannot reasonably accommodate. Identify its expected reader and the
future decision, operation, or significant repeated work it will support.
Task-specific investigations qualify when their findings have lasting value.
Keep temporary plans, task narration, and routine verification in the chat or
pull request; completing a task does not itself require a repository document.

Give each retained Markdown file a purpose-specific inline link from an existing
document reachable from this file, except explicitly invoked skills. Explain
when to read it. A link provides discoverability, not a reason to retain a file.
Review orphaned documents: link useful records and consolidate or remove
redundant, obsolete, or temporary material. Preserve decision rationale that
future work still needs. Keep links current when moving or renaming documents.

Update [Run repository tools](RUN_TOOLS.md) whenever a manually invoked tool is
added or changed. Include prerequisites, the command, and how to verify its
result. Link to the owning record for implementation or operational details.

After consequential work, update affected records when durable knowledge changes.
Use [project status](docs/status.md) for ongoing work and unresolved verification,
with a link to the owning record or pull request and the next action. Retain
evidence, recovery steps, and verification limits in repository records only
when future work needs them. Keep routine results in the pull request.
Distinguish implementation, merge, deployment, and verification when applicable.

Read [opportunities for improvement](opportunities_for_improvement.md) when
planning future work or working on a listed topic. Update the relevant entry
when related work produces a plan, finding, deferral, or completion. Keep
details in the linked record or pull request.

Record significant choices using the
[decision record guidance](docs/decisions/README.md).

## Repository-specific instructions and skills

Add directory-specific `AGENTS.md` files only where a directory needs additional
recurring rules. Link them from the documentation map or the owning record so
their scope is discoverable.

Add repository skills under `.agents/skills/` when a repeatable repository
procedure has been exercised and its commands exist in versioned source.
Each skill should call those tools and link to its owning documentation.
For automatically selected skills, record the invocation trigger and link here
and in the documentation map. Explicitly invoked skills may remain unlinked;
give them a clear invocation description in their skill metadata.
This starter includes no repository skills.

## Documentation ownership

Maintain each fact, instruction, or procedure in one record. Link to that
record when another document needs the information.

The ownership map below is a starter structure, not a required file inventory.
Consolidate or remove unused records when adapting it to a project. Update the
ownership map and affected instructions and links together so routing stays valid.

| Record | Owns |
|---|---|
| This file | Repository task routing, documentation rules, and local skill triggers |
| [README](README.md) | Project purpose, scope, and entry points |
| [Documentation map](docs/overview.md) | Task links and source locations |
| [Project status](docs/status.md) | Progress, pending verification, and next actions |
| [Development](docs/development.md) | Project prerequisites, setup, checks, and contribution requirements |
| [Configuration contract](docs/configuration-contract.md) | Configuration ownership, schemas, and source versus runtime boundaries |
| [Change workflow](docs/change-workflow.md) | Repository change and handoff requirements |
| [Run repository tools](RUN_TOOLS.md) | Commands people run by hand and expected results |
| [Opportunities for improvement](opportunities_for_improvement.md) | Candidate work and links to existing context |
| [Decision records](docs/decisions/README.md) | Significant choices, reasons, and conditions for reconsideration |
| [Runbooks](docs/runbooks/README.md) | Repeatable operation and recovery procedures |
| Task and component records linked from the map | Durable plans, findings, evidence, and verification limits needed by future work |

Keep temporary task notes outside versioned documentation. Personal preferences
and rules that apply across repositories belong in the user's root instructions.
