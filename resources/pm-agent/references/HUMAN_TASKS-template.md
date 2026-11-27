# Human Tasks - <Project Name>

**Last Updated:** YYYY-MM-DD
**Owner:** <Project Owner>

Tasks for the project owner or another human stakeholder.

---

## Pre-Phase 1

| # | Task | Status | Priority | Depends On | Notes |
|---|------|--------|----------|------------|-------|
| H-001 | <Human task title> | TODO | Urgent | - | <Context, access, approval, or external dependency> |
| H-002 | <Human task title> | TODO | High | H-001 | <What must be prepared or confirmed> |

---

## Pre-Phase 2

| # | Task | Status | Priority | Depends On | Notes |
|---|------|--------|----------|------------|-------|
| H-003 | <Human task title> | TODO | Urgent | - | <Required before Phase 2 starts> |

---

## Ongoing

| # | Task | Status | Priority | Depends On | Notes |
|---|------|--------|----------|------------|-------|
| H-005 | <Recurring or decision task> | TODO | Medium | - | <Review cadence, go/no-go rule, owner note> |

---

## Task Details

### H-001 - <Human task title>

- Context: <Why this task exists and when it should be done>
- Instructions:
  - <Step or setting to apply>
  - <Step or setting to apply>
- Expected Result: <What artifact, access, or state should exist after completion>

### H-00X - <Human task title>

- Context: <Use this block only when the table notes are not enough>
- Instructions:
  - <Detailed checklist, configuration, approval flow, or vendor-specific step>
- Expected Result: <How the human verifies the task is really done>

---

## Status Values

- `TODO` - not started
- `IN_PROGRESS` - currently being handled by human stakeholder
- `BLOCKED` - waiting for dependency, approval, or external action
- `DONE` - completed

## Priority Values

- `Urgent` - same-phase blockers
- `High` - blocks tasks in any future phase
- `Medium` - pre-launch but non-blocking work
- `Low` - post-launch / backlog / optional work

## Notes

- Add new sections only when they reflect a real project phase or gate.
- Set `Priority` when the task is created; do not recalculate it automatically after phase completion.
- `Pre-Phase N` sections must map directly to `Phase N` in `agent_tasks.md`: these are human prerequisites that must be completed before AI work for that phase can start.
- Phase flow is sequential: `Pre-Phase 1 -> Phase 1 -> Pre-Phase 2 -> Phase 2 -> ...`.
- `Depends On` may reference task IDs from `tasks/agent_tasks.md` and `tasks/human_tasks.md`.
- Task IDs must be unique across both registries inside the same project.
- Use `Task Details` for instructions that do not fit into the main table: setup steps, account configuration, provider-specific actions, approval flow, or validation checklist.
- Add a `Task Details` block only for tasks that actually need extra explanation; do not duplicate the whole table there.
- Use `Depends On` for approvals, account setup, payments, infra access, legal steps, and other human prerequisites.
- Keep `Notes` actionable: where to do it, what artifact is produced, and any approval criteria.
