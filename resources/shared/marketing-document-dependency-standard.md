# Marketing Document Dependency Standard

Use for every marketing Brief, MRD, strategy, plan, audit, playbook, copy deck, or creative handoff produced by `marketing-analyst` or `product-marketing-agent`.

## 1. Canonical dependency model

`Selected target/module -> Brief question ID -> answer status -> dependency class -> target readiness`

- A target is a whole document or a selectable module ID from the Approved Deliverable Scope.
- The Marketing Brief owns questions and current answers. The Deliverable Scope owns selected targets. The MRD owns cross-document requirements and the readiness impact of unresolved inputs.
- Never use document order alone as a blocker. Apply the dependency register to the exact selected target or module.

## 2. Build the Brief as a constructor

1. Record requested documents, template variants, and modules before gathering detailed inputs.
2. Filter the [Brief Question Library](../marketing-analyst/MARKETING_BRIEF_QUESTION_LIBRARY.md) and its linked question resources: include a row only when its `Used by` field intersects selected targets and its `Include when` trigger is true. Record the trigger basis in the Brief Manifest. Unknown additional trigger -> include the row for confirmation; never assume it is false.
3. Add a question outside the library only when a selected target needs it. Give it a stable project ID, exact wording, applicability trigger, target mapping, purpose, gate condition, and source basis. Do not silently expand scope.
4. Prefill answers from inspected sources. Ask the user only for material gaps. Preserve the exact selected question IDs in the Brief Question Set Manifest.
5. Scope added later -> add only newly triggered questions, version the Scope and Brief, and recalculate affected readiness.

## 3. Answer and dependency states

Allowed answer states: `Answered`, `TBA`, `Not applicable`.

- `Answered`: a user answer or evidence-supported answer exists; record basis and source or decision ID. For inventory questions, confirmed absence is an answer. For choice questions, `Open for recommendation` is an answer only when decision owner, constraints, and approval point are known.
- `TBA`: no defensible answer exists. Never replace it with an assumption.
- `Not applicable`: the question does not apply to the selected target in this project; record rationale and approver.

An unknown value required to approve a target remains `TBA`. Do not treat `unknown`, silence, or delegated analysis as a resolved factual input.

For each selected-target intersection classify the question as:

- `Blocking`: the target or module cannot make a defensible decision without the answer.
- `Supporting`: the target can proceed with a visible limitation; no invented value may fill the gap.
- `Not used`: no dependency for that target.

The library supplies default gate conditions. A project may change a default only with rationale and explicit user approval recorded in the Scope or MRD.

## 4. Dependency and readiness register

| Question ID | Answer state | Selected target/module | Dependency class | Consequence if TBA | Resolution owner/due | Readiness |
|---|---|---|---|---|---|---|
| `[OPS-01]` | `[TBA]` | `[PAID-BUDGET]` | `[Blocking]` | `[Paid Media Plan cannot approve]` | `[ ]` | `[Blocked]` |
| `[OPS-01]` | `[TBA]` | `[BB-VOICE]` | `[Not used]` | `[None]` | `[ ]` | `[Ready if its own gates pass]` |

Calculate readiness per target or module:

- `Ready`: every Blocking input is `Answered` or justified `Not applicable`.
- `Partially Ready`: a document has at least one selected Ready module and at least one selected Blocked module.
- `Blocked`: at least one Blocking input is `TBA` for that target or module.
- `Not selected`: outside Approved Deliverable Scope.

Blocked target/module -> STOP only that target/module, name the question IDs and needed answers, then continue any independent Ready work. A document cannot be Approved while one of its selected modules is Blocked; Ready modules may be drafted or reviewed separately when their boundaries are explicit.

## 5. Brief and MRD approval semantics

- Brief approval confirms the selected question set, current answers, TBA list, and mappings. It does not resolve TBA.
- MRD approval requires all Blocking inputs for `MRD-CORE` to be `Answered` or justified `Not applicable`.
- A downstream-only TBA does not block MRD approval. The Approved MRD must preserve its target mapping, consequence, owner, and readiness state.
- MRD approval does not authorize a Blocked downstream target. Each target passes its own input-readiness and approval gates.
- A newly resolved answer that changes approved meaning -> version the Brief and MRD, run impact analysis, mark semantically affected artifacts `Needs Update`, and reapprove them.

## 6. Handoff gate

Every cross-agent or technical/design handoff states: source versions; selected target/module IDs; Ready and Blocked modules; unresolved question IDs; accepted limitations; required output; owner; approver; and prohibited live actions. The receiving agent does not reinterpret TBA as permission to choose a value.

## Verification

- Every Brief question has a stable ID, trigger basis, answer state, basis, selected-target mapping, and stated purpose.
- Every selected target has a readiness row; no unselected target creates questions or blockers.
- Every TBA has an explicit consequence. No global TBA blocker remains.
- Readiness and approval are distinct: `Ready` permits work, while `Approved` requires explicit user approval.
