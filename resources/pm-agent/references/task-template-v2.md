# Task File Template v2

Each task file you create (`tasks/<module>/TASK-CODE.md`) must be execution-ready from the task text alone.

```markdown
# TASK-CODE - Task Title

**Status:** TODO | IN_PROGRESS | READY_FOR_REVIEW | READY_FOR_QA | DONE | BLOCKED
**Agent:** [assigned specialist agent]
**Owner:** [claude | codex | -]
**Depends on:** [TASK-CODE list or "none"]
**Code Review Required:** Yes | No
**QA Required:** Yes | No
**Tests Required:** Yes | No

## Goal
[One paragraph on the intended outcome]

## Deliverable
- [Concrete artifact or behavior that must exist after completion]

## Files / Surfaces
- [Exact file path]
- [Exact module, endpoint, screen, or registry surface if path is not yet knowable]

## Critical Context
- [Task-relevant fact extracted from PRD / architecture / API / schema]
- [Invariant or constraint]
- [Material edge case or forbidden change]

## Scope
- [What this task includes]

## Acceptance Criteria
- [ ] [Observable and verifiable result]
- [ ] [Observable and verifiable result]

## Verification
- Commands:
  - `[command 1]`
  - `[command 2]`
- Expected evidence:
  - [What must be visible in output, files, UI, logs, or docs]

## Out of Scope
- [Explicitly excluded change]

## References
- [1-3 narrow references only]

## Handoff Notes
- [What the next reviewer / QA / knowledge agent must verify or record]
```

## Rules

- Do not leave `TBD`, `None yet`, or placeholder review sections in planning output.
- `Critical Context` is mandatory.
- `Files / Surfaces` must be specific enough that the implementing agent knows where to start.
- `References` support the brief; they do not replace it.
