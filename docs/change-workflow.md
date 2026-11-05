# Change workflow

1. Read the [documentation map](overview.md) and [project status](status.md).
   Follow the relevant records and inspect related Git history and pull requests
   before choosing an implementation.
2. Update the existing task or component record. Create a separate record only
   when the scope needs one, then link it from the map or an owning record.
   Record the intended behavior and validation approach. Include recovery steps
   for changes that affect deployed state or stored data.
3. Implement the change and run the applicable checks defined in
   [development](development.md). Record results and checks that could not run
   in the owning record.
4. Update [Run repository tools](../RUN_TOOLS.md) for manual command changes,
   the [configuration contract](configuration-contract.md) for ownership changes,
   and [decision records](decisions/README.md) for significant choices.
5. Update [project status](status.md) with progress, the evidence link, and the
   next action. Update a related
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

Keep the repeatable procedure separate from records of individual executions.
Link execution evidence from project status. A successful build or merge alone
does not establish deployed or verified state.
