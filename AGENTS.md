# Repository instructions

## Task routing and ownership

Read the sections relevant to the task. Before proposing work, search the
relevant records, Git history, and related pull requests for earlier decisions,
existing plans, and verification gaps.

| When to read | Authoritative location |
|---|---|
| Understand the project, source layout, or template adoption | [README](README.md) |
| Set up the project | [Development: project setup](docs/development.md#project-setup) |
| Run or change a manual tool | [Development: commands](docs/development.md#commands) |
| Run or change checks | [Development: repository checks](docs/development.md#repository-checks) |
| Change configuration ownership or tooling | [Development: configuration](docs/development.md#configuration) |
| Implement, review, or hand off a change | [Development: change and delivery](docs/development.md#change-and-delivery) |
| Operate or recover a component | [Development: operations](docs/development.md#operations) |
| Plan or resume work, or investigate verification gaps | [Project status](docs/status.md) |
| Consider candidate or deferred work | [Project status: opportunities](docs/status.md#opportunities) |
| Prepare a pull request | [Pull request template](.github/pull_request_template.md) |

This file owns agent instructions and documentation policy. Maintain each fact,
instruction, or procedure in one authoritative location and link to it elsewhere.
Add task-specific links here or in an owning record as project knowledge grows.

## Documentation workflow

Before creating a document, search the routing table, tracked and untracked
Markdown files, and related pull requests for an existing record. Update that
record when its purpose is the same.

Create a document only when durable project knowledge needs a distinct ongoing
home that existing records cannot reasonably accommodate. Identify its expected
reader and the future decision, operation, or significant repeated work it will
support. Task-specific investigations qualify when their findings have lasting
value. Keep temporary plans, task narration, and routine verification in the
chat or pull request; completing a task does not require a repository document.

Give each retained Markdown file a purpose-specific inline link from a document
reachable from this file, except explicitly invoked skills. Explain when to
read it. A link provides discoverability, not a reason to retain a file. Review
orphaned documents: link useful records and consolidate or remove redundant,
obsolete, or temporary material. Keep links and routing current when moving,
renaming, or consolidating records.

Start with sections in the existing records. Extract a separate document when
the content needs independent navigation or maintenance. Add indexes only when
readers need help choosing among actual records; do not create empty indexes.

For a significant choice whose rationale future work will need, create a record
such as `docs/decisions/0001-descriptive-choice.md`. Include status, problem,
constraints, evidence, choice, alternatives, tradeoffs, and reconsideration
conditions. Preserve needed rationale when superseding a decision and link its
replacement. Routine fixes do not need decision records.

Keep personal preferences and cross-repository rules in the user's root
instructions.

## Repository-specific instructions and skills

Add directory-specific `AGENTS.md` files only where additional recurring rules
are needed. Link them from the routing table or owning record.

Add repository skills under `.agents/skills/` when a repeatable procedure has
been exercised and its commands exist in versioned source. Each skill should
call those tools and link to its owning documentation. For automatically
selected skills, record the invocation trigger and link here. Explicitly invoked
skills may remain unlinked; describe their invocation in their skill metadata.
This starter includes no repository skills.
