# Modular Marketing Brief Template

Template state: Ready for use

Build this Brief from the [Deliverable Scope Matrix](./DELIVERABLE_SCOPE_MATRIX_TEMPLATE.md), [Brief Question Library](./MARKETING_BRIEF_QUESTION_LIBRARY.md), and [Marketing Document Dependency Standard](../shared/marketing-document-dependency-standard.md). Do not copy the whole question library. Include only blocks and question rows triggered by selected documents, modules, and applicable project-shape facts.

```text
Brand:
Document language:
Status: Draft
Version:
Last updated:
Approved by:
Approved on:
Scope matrix/version:
Source inventory/version:
```

## 1. Requested outcome and deliverable selection

| Artifact | Template variant | Requested module IDs | Intended audience/use | State |
|---|---|---|---|---|
| `[Selected strategy or other artifact]` | `[selected template path or NA]` | `[IDs or All]` | `[ ]` | `[requested/selected/deferred/not selected]` |

Record the strategy types and templates approved in the active project, including Full/Compact variants only when selected. Give each selected strategy its own row; qualify module IDs with the document type when several strategies use the same module.

Record explicit exclusions and the decision this set of documents must support: `[ ]`.

## 2. Brief Question Set Manifest

| Block | Included question IDs | Triggering selected target/module IDs | Additional trigger/basis | Added/removed in version | Rationale for any project-specific question |
|---|---|---|---|---|---|
| `[A. Project and governance]` | `[CORE-01...]` | `[ ]` | `[library trigger + observed project fact]` | `[ ]` | `[library/default or approved rationale]` |

- Every selected library question appears once below.
- Unselected modules create no question and no blocker.
- A project-specific question needs a stable ID, exact wording, applicability trigger, target mapping, purpose, gate condition, and source basis.

## 3. Answers by selected block

Repeat this section for each block in the Manifest. Preserve the exact library wording so answer provenance and dependencies remain stable.

### `[Block name]`

| Question ID | Exact question/parameter | Answer | Answer state | Basis/source or user decision | Used by selected targets | Why needed | Gate condition if TBA |
|---|---|---|---|---|---|---|---|
| `[ID]` | `[exact library question]` | `[supported answer or TBA]` | `[Answered/TBA/Not applicable]` | `[source ID/path or user decision]` | `[target/module IDs]` | `[exact decision/section supported]` | `[exact consequence]` |

`Not applicable` requires rationale and approver: `[ ]`.

## 4. TBA Dependency Register

Include every `TBA` once per affected selected target. Do not list unselected or `Not used` targets as blockers.

| Question ID | Selected target/module | Dependency class | Why the answer is needed | Consequence now | Resolution path | Owner/due | Readiness |
|---|---|---|---|---|---|---|---|
| `[OPS-01]` | `[PAID-BUDGET]` | `[Blocking]` | `[allocation cannot be reconciled]` | `[module blocked]` | `[user answer/research/approved proposal/NA rationale]` | `[ ]` | `[Blocked]` |

## 5. Deliverable and module readiness

| Selected target/module | Blocking question IDs | Supporting TBA IDs | Readiness | Work allowed now | Approval consequence |
|---|---|---|---|---|---|
| `[BB-VOICE]` | `[none]` | `[ ]` | `[Ready]` | `[draft/review]` | `[may approve after its own gate]` |
| `[PAID-BUDGET]` | `[OPS-01]` | `[ ]` | `[Blocked]` | `[none beyond evidence collection]` | `[cannot approve]` |

Allowed readiness: `Ready`, `Partially Ready`, `Blocked`, `Not selected`.

## 6. Confirmed assumptions, limitations, and conflicts

| ID | Type | Statement | Basis | Affected targets | Decision/owner |
|---|---|---|---|---|---|
| `[LIM-001]` | `[limitation/conflict/approved assumption]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |

An assumption is allowed only when explicitly approved and never converts an unsupported claim into fact.

## Brief approval gate

- Requested documents, variants, and modules match the Scope Matrix.
- Manifest contains every and only triggered question ID; each selected question has an answer state, basis, selected-target mapping, and purpose.
- Every TBA maps to exact selected targets with dependency class, consequence, and resolution path.
- Readiness is calculated per target/module; no TBA creates a global blocker.
- Approval confirms current answers and the unresolved-item map. It does not treat TBA as answered or authorize a Blocked target.
- Approval fields remain blank until explicit user approval.
