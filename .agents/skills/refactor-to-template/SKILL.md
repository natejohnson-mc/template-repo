---
name: refactor-to-template
description: Refactor an existing repository to follow template-repo's documentation layout and ownership conventions. Use when asked to adopt this template in a different repository or reorganize that repository's documentation and agent instructions to match it.
---

# Refactor a repository to match the template

Use `template-repo` as the reference and the repository identified by the user
as the target. An invocation from the template checkout can look like
`$refactor-to-template F:/Repositories/my-project`. Resolve the target's Git
root and confirm it differs from the template checkout before editing. Work
from the target root and follow its applicable instructions. If the target is
ambiguous, ask which checkout to refactor.

## Inventory the target

Inspect Git status, tracked and untracked Markdown, repository instructions,
contribution and operations guides, review templates, and the entry points for
setup, checks, and CI. Search relevant Git history and pull requests for prior
decisions, work in progress, and verification gaps. Use the current files and
their callers to confirm which commands, configuration, and paths are live.
Preserve existing user edits and staging.

For each affected document, identify its audience, the facts or procedures it
owns, its incoming links and other consumers, and whether to keep it, move its
content into an existing record, or remove it. Use the owning source to resolve
duplicates. Surface consequential contradictions you cannot resolve from the
repository or its history.

## Apply the template's ownership model

The destination names show default paths in the target. Use the linked template
files as examples. Adapt headings or locations when an existing equivalent
already serves readers or a tool requires its path.

| Destination | What it owns |
|---|---|
| [`AGENTS.md`](../../../AGENTS.md) | Repository-specific agent rules, task routing to exact sections, documentation policy, and links to applicable scoped instructions and skills. |
| [`README.md`](../../../README.md) | The project's purpose, scope, entry points, and actual source layout. Link to development guidance for setup and routine work. |
| [`docs/development.md`](../../../docs/development.md) | Setup, runnable commands, local and CI checks, configuration ownership, change and delivery, and operations. Verify commands against their entry points and record prerequisites, expected results, and whether they change state. Document configuration sources, consumers, and update methods without credential values. |
| [`docs/status.md`](../../../docs/status.md) | Active work, pending verification, and candidate or deferred opportunities. Keep one entry per item with evidence and a next action. Distinguish implementation, merge, deployment, and verification when applicable. |
| [`.github/pull_request_template.md`](../../../.github/pull_request_template.md) | On GitHub, a review prompt covering the change, validation and gaps, and delivery impact. Adapt the existing review template for the target's forge and process. |

Populate these destinations from verified target material. Omit unused sections
and avoid copying starter placeholders. Keep a single authoritative home for
each fact or procedure and link to it from other documents. Keep temporary
plans and routine verification in the chat or pull request. Retain decision
records, runbooks, and component guides when they have lasting value and need
independent navigation or maintenance. Link every retained Markdown document
through a purpose-specific route from `AGENTS.md`, with an exception for
explicitly invoked skills. Add an index only when readers need it to navigate
existing records.

Keep the target's source layout, runtime and CI behavior, and tool configuration
in place for a documentation refactor. Document the target's `.codex/config.toml`
if it exists and the work touches its ownership. The reference's Codex settings
and user-root preferences are local choices. Bring them over only when the user
requests them. Keep personal preferences in user-level instructions.

## Migrate and verify

Move durable content before deleting or consolidating its old location. Update
links, heading fragments, and other references together. Check scripts, CI,
generated navigation, and published documentation for path dependencies. Where
an existing path is a public or tool-facing entry point, preserve it or provide
the target's supported redirect or forwarding mechanism.

Verify local Markdown links and anchors, reachability from `AGENTS.md`, and
references to removed paths or headings. Review the diff for lost instructions,
duplicated ownership, starter text, and unrelated changes. Run `git diff --check`
and the target's applicable checks, including docs builds or link checks when
available. Check untracked new files too. Report the resulting structure,
material adaptations, checks run, and unresolved verification.
