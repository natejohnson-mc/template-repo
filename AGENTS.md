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

## Directory agent files

Treat `AGENTS.md` as the working interface to its directory and subtree. Keep
one authoritative agent file at the root and one at each module boundary that
needs recurring guidance on navigation, reuse, or local rules. Directories
without a local file use the nearest ancestor's guide.

Keep each guide short and focused on the decisions contributors need to make.

- State what the directory owns and when to work there.
- Explain when to use each immediate child directory that contributors need to
  navigate. Link its guide or owning record when it has one.
- Name the files, commands, or APIs contributors should start with. Point to
  shared tools and the supported ways to configure or extend them.
- State the rules that apply throughout the subtree, such as dependency
  boundaries or required checks. Keep inherited rules in their owning guide.

Make every local guide reachable from its nearest ancestor guide. Link to code
or owning records for details, and update routes when entry points or module
boundaries change.

Before adding a new implementation, use the guides and search the code for a
suitable module, command, or extension point. Reuse, configure, or extend it
when it fits the task.

## Repository-specific instructions and skills

Add repository skills under `.agents/skills/` when a repeatable procedure has
been exercised. If it relies on project tools, keep the commands in versioned
source and have the skill call those tools and link to their owning
documentation.
For automatically selected skills, record the invocation trigger and link here.
Explicitly invoked skills may remain unlinked. Describe their invocation in
their skill metadata.

Use [`$refactor-to-template`](.agents/skills/refactor-to-template/SKILL.md) when
asked to refactor an existing repository to follow this template. Invoke it
with the target repository path from a chat that can access both checkouts.
