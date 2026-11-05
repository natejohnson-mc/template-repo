# Development workflow

## Project setup

No language, runtime, package manager, or development environment is selected.
When establishing the project, replace this section with supported versions,
dependency installation commands, and required local configuration. Link to the
[configuration contract](configuration-contract.md) for configuration ownership.

## Repository checks

No automated checks, hooks, or CI jobs are configured. Add the exact commands
and expected results when they exist. Identify which checks run locally and in
CI, their prerequisites, and any platform or integration limits.

For documentation changes, verify that local links and heading anchors resolve
and that retained Markdown files are reachable from
[repository instructions](../AGENTS.md) through inline links, with the exception
for explicitly invoked skills defined in the
[documentation rules](../AGENTS.md#documentation-workflow). Review new and
retained records for distinct purpose, lasting value, and duplication; passing
link checks alone does not justify retaining a document. Follow the
[ownership map](../AGENTS.md#documentation-ownership) when adapting the structure.

## Review and delivery

The project has no configured branch policy, required checks, or release process.
Document those requirements here when selected. The
[pull request template](../.github/pull_request_template.md) captures the problem,
resulting behavior, validation, and delivery impact.

Use the [change workflow](change-workflow.md) to update the records affected by
a change. Add manual tool commands to [Run repository tools](../RUN_TOOLS.md).
