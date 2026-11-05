# Development

## Project setup

No language, runtime, package manager, or development environment is selected.
When establishing the project, record supported versions, dependency setup,
and required local configuration. Reference runnable commands in
[Commands](#commands) and ownership rules in [Configuration](#configuration).

## Commands

No manually invoked project tools are included in this starter. When adding or
changing one, update this section with its purpose, prerequisites, working
directory, exact command, required inputs, expected result, and how to verify
success. State whether it reads or changes state. Link to an owning component
record or procedure for operational details. Keep implementation in versioned
source and publish commands only when their entry points exist.

## Repository checks

No automated checks, hooks, or CI jobs are configured. Add exact commands and
expected results when they exist, distinguishing local and CI checks and their
prerequisites and platform or integration limits. Link to entries in
[Commands](#commands) when a check already has an authoritative command there.

For documentation changes, verify that local links and heading anchors resolve.
Check Markdown reachability and review purpose, lasting value, duplication,
and ownership against the
[documentation policy](../AGENTS.md#documentation-workflow).

## Configuration

The template maintainer owns the versioned [Codex configuration](../.codex/config.toml).
It was copied from `home-media-server/.codex/config.toml` and is now maintained
here as the repository's authoritative configuration for Codex. Edit this file
directly to update the repository's model and reasoning settings.

No project configuration schema or runtime environment is defined. Before
introducing configuration or deployment tooling, document each location's path,
component owner, authoritative source, versioning, consumer, and update method.
Distinguish maintained source, examples, observations of external state,
generated output, and private runtime data.

Link maintained schemas and examples; document required fields, defaults,
supported schema versions, and validation commands. Record credential names
and storage mechanisms without values. Identify excluded runtime or generated
paths and what deployment consumes, including how runtime state is handled.

## Change and delivery

No branch policy, required checks, or release process is configured. Record
project-specific requirements here when selected.

1. Use the [task routing](../AGENTS.md#task-routing-and-ownership) to read relevant
   context and earlier decisions before choosing an implementation.
2. Describe intended behavior and validation in the pull request or working
   chat. Include recovery steps for changes to deployed state or stored data.
3. Implement and run applicable [checks](#repository-checks). Record results,
   checks that could not run, and remaining verification in the pull request.
4. Apply the [documentation policy](../AGENTS.md#documentation-workflow) to
   update affected durable knowledge, including commands and configuration.
   Link evidence rather than duplicating it.
5. Update [project status](status.md) when ongoing work, unresolved verification,
   or an existing opportunity changes. Follow that record's entry guidance.
6. Use the [pull request template](../.github/pull_request_template.md) for review.
   At handoff, report resulting behavior, validation, delivery state, and
   remaining work. Distinguish implementation, merge, deployment, and
   verification; a successful build or merge alone does not establish deployed
   or verified state.

## Operations

No deployment or live-operation procedure is defined. Document actual procedures
here or in an existing component record when needed. Extract a runbook under
`docs/runbooks/` when a procedure needs independent navigation or maintenance,
and link it here or from its owning record. Add an index when actual procedures
need it; do not duplicate procedures already maintained elsewhere.

Each procedure should identify scope, prerequisites, starting state, affected
components, commands, expected results, recovery steps, and verification limits.
Distinguish read-only inspection from state changes and identify recovery steps
that have not been exercised. Reference maintained tools instead of copying
their implementation.

Keep routine execution results in the pull request or operational system of
record. Apply the [documentation policy](../AGENTS.md#documentation-workflow)
when evidence has lasting value and needs a repository record.
