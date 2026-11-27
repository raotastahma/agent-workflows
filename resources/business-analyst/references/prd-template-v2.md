# PRD Template v2

Use this template when drafting a product requirement document that other planning agents will consume.

## Structure

```markdown
# Product Requirements Document

**Project Name:** <name>
**Document Version:** <version>
**Date:** YYYY-MM-DD
**Author:** business-analyst
**Status:** Draft | Approved

## Executive Summary
### Problem
### Proposed Product Direction
### Product Value

Rules:
- Keep this section short.
- Do not restate the full requirement list here.

## Product Context
### Current State
### Desired State
### Primary User / Stakeholder

## Goals And Non-Goals
### Goals
### Non-Goals

## Scope Decisions
- Frontend: yes / no
- Backend: yes / no
- Integrations: <list>
- Deployment shape: <local / cloud / mixed>
- Design ownership: <user-provided / agent-created / none>

## Functional Requirements
| ID | Requirement | Notes |
|----|-------------|-------|
| FR-001 | <canonical requirement statement> | <constraints, if needed> |

Rules:
- Each requirement appears once here as the canonical statement.
- Put detailed rule text here, not in roadmap sections.

## Non-Functional Requirements
| ID | Requirement | Notes |
|----|-------------|-------|
| NFR-001 | <canonical non-functional rule> | <constraints, if needed> |

## Phase Roadmap
### Phase 1 - <name>
- Outcome: <phase outcome>
- Includes: `FR-001`, `FR-003`, `NFR-001`
- Excludes: `FR-010`

Rules:
- Reference requirement IDs instead of repeating full requirement prose.

## Success Metrics
- <observable business or delivery outcomes>

## Risks And Mitigations
- Risk
- Mitigation

## Open Questions
- <true unresolved item only>

## References
- <canonical docs and sources>
```

## Quality bar

- Summary sells the problem and value.
- Requirement details live in canonical requirement sections.
- Phases map requirements to milestones instead of repeating them.
- Open questions stay separate from confirmed scope.
