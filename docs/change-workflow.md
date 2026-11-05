# Change workflow

1. Read the [documentation map](overview.md) and [project status](status.md).
   Follow the relevant records and inspect related Git history and pull requests
   before choosing an implementation.
2. Describe intended behavior and validation in the pull request or working chat.
   Apply the [documentation rules](../AGENTS.md#documentation-workflow) when
   deciding whether durable knowledge needs an existing record updated or a
   separate record created. Routine changes do not require a repository record.
   Include recovery steps for changes to deployed state or stored data.
3. Implement the change and run the applicable checks defined in
   [development](development.md). Record results and checks that could not run
   in the pull request. Preserve evidence in an owning record when future work
   needs it, linking to the evidence rather than duplicating it.
4. Update [Run repository tools](../RUN_TOOLS.md) for manual command changes,
   the [configuration contract](configuration-contract.md) for ownership changes,
   and [decision records](decisions/README.md) for significant choices.
5. Use [project status](status.md) for ongoing work or unresolved verification,
   linking to the owning record or pull request and naming the next action.
   Remove or condense resolved entries rather than accumulating a task log.
   Update a related
   [improvement topic](../opportunities_for_improvement.md) when its disposition
   changes.
6. Follow the project's delivery requirements in
   [development](development.md#review-and-delivery). At handoff, report the
   resulting behavior, validation results, delivery state, and remaining work.

## Operational changes

This template has no deployment or live-operation procedure. When a project
needs one, add a component-specific runbook with prerequisites, the starting
state, commands, expected results, recovery, and verification limits. Register
it in the [runbook index](runbooks/README.md).

Keep the repeatable procedure separate from results of individual executions.
Keep routine results in the pull request or operational system of record.
Preserve execution evidence in a repository record only when future work needs
it; link unresolved verification from project status. A successful build or
merge alone does not establish deployed or verified state.
