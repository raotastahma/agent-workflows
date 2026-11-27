# Implementation Handoff Checklist

Use when architecture output is about to be handed to the project's delivery owner.

- Name the exact contracts, schemas, and invariants that delivery must preserve.
- Name the likely files, modules, or surfaces if they are discoverable.
- Separate locked design decisions from optional implementation suggestions.
- State migration impact and backward-compatibility constraints.
- State explicit non-goals so delivery does not widen scope.
- If delivery would still need to read the whole architecture doc to write tasks, extract a short implementation-facing slice first.
