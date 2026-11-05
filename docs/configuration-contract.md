# Configuration ownership

No project configuration schema or runtime environment is defined. Populate
this contract before adding configuration files or deployment tooling.

## Ownership map

For each configuration location, record:

- Its path and the component that owns it.
- Whether it is maintained source, an example, an observation of external
  state, generated output, or private runtime data.
- Which system is authoritative and how changes are applied or refreshed.
- Whether it is versioned and which tool reads or writes it.

## Schemas and examples

Link each maintained schema and example from this record or the owning
component record. Document required fields, defaults, supported schema versions,
and project-specific validation commands.

Record required credential names and storage mechanisms in the owning record
without including values. Define project-specific excluded paths when runtime
data or generated artifacts are introduced.

## Delivery boundary

No deployment mechanism is configured. If the project gains one, document which
files it consumes, how it handles runtime state, and where deployment and
recovery procedures are recorded. Link those procedures from the
[runbook index](runbooks/README.md).
