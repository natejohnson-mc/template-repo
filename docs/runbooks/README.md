# Runbook index

No project operation or recovery procedures are defined.
Use the [change workflow](../change-workflow.md) to plan and record changes.

## Add a runbook

Put standalone repeatable procedures in this directory and link them here by
task. Link to procedures maintained in component records rather than copying
them into this directory.

Each procedure should identify its scope, prerequisites, affected components,
commands, expected results, recovery steps, and known limits. Distinguish
read-only inspection from commands that change state. Reference maintained
tools rather than reproducing their implementation.

Record individual execution results in the owning task or component record and
link them from [project status](../status.md). Identify recovery procedures that
have not been exercised.
