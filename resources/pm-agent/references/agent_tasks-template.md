# Agent Tasks - <Project Name> Task Registry

**Last Updated:** YYYY-MM-DD
**Managed by:** pm-agent

---

## Phase 1: <Phase Name>

| Task | Title | Agent | Owner | Status | Priority | Depends On | CR | QA |
|------|-------|-------|-------|--------|----------|------------|----|----|
| MOD-001 | <Task title> | <implementation owner> | - | TODO | Urgent | - | Yes | Yes |
| MOD-002 | <Task title> | <interface owner> | - | TODO | High | MOD-001 | No | Yes |

**Phase 1 Success Criteria:** <What must be true to consider the phase complete.>

---

## Phase 2: <Phase Name>

| Task | Title | Agent | Owner | Status | Priority | Depends On | CR | QA |
|------|-------|-------|-------|--------|----------|------------|----|----|
| MOD-003 | <Task title> | <implementation owner> | - | TODO | High | MOD-001 | Yes | Yes |
| MOD-004 | <Task title> | qa-agent | - | TODO | Medium | MOD-002, MOD-003 | No | Yes |

**Phase 2 Success Criteria:** <Outcome, metric, or readiness gate.>

---

## Status Values

- `TODO` - task is defined and ready when dependencies are clear
- `IN_PROGRESS` - actively being implemented
- `READY_FOR_REVIEW` - implementation finished, waiting for code review
- `READY_FOR_QA` - review passed, waiting for QA
- `DONE` - completed and accepted
- `BLOCKED` - cannot move forward due to dependency or external blocker

## Priority Values

- `Urgent` - same-phase blockers
- `High` - blocks tasks in any future phase
- `Medium` - pre-launch but non-blocking work
- `Low` - post-launch / backlog / optional work

## Notes

- Add phases only when they represent a real delivery milestone with a clear success criterion.
- Set `Priority` when the task is created; do not recalculate it automatically after phase completion.
- `Owner` identifies the intended executor:
  - `claude` - intended executor is Claude Code
  - `codex` - intended executor is Codex
  - `-` - no executor assigned
- `Depends On` may reference task IDs from `tasks/agent_tasks.md` and `tasks/human_tasks.md`.
- Task IDs must be unique across both registries inside the same project.
- Phase flow is sequential: `Pre-Phase 1 -> Phase 1 -> Pre-Phase 2 -> Phase 2 -> ...`.
- `Phase N` is gated by the matching `Pre-Phase N` section in `tasks/human_tasks.md`.
- `Depends On` and phase grouping define what can be taken next; a separate execution-order section is intentionally omitted.
- Keep agent names aligned with actual available project agents.
- `Managed by` should name the agent responsible for updating statuses in this registry.
- **Phase Gate:** Do not start the next phase until current phase success criteria are met.
- **Source of Truth:** Link PRD, architecture, API spec, schema, or any project-defining docs here.
