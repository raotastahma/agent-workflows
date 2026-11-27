# Discovery, Document Workflow, and Approval Protocol

Use for new marketing projects, bounded artifacts, updates, content plans, and performance reviews. Apply the [Marketing Document Dependency Standard](../shared/marketing-document-dependency-standard.md).

## 1. Project initialization and sources

1. Confirm supplied document/content language, requested document types, selected templates and module scope, intended audience/use, and deadlines; ask only missing choices. Strategy types and template selection follow the approved project strategy templates; `Full`/`Compact` are explicit alternatives for general Marketing Strategy.
2. Create the brand directory from [Project Structure](./project-structure.md); record language, requested scope, delivery operator, capacity, owners, approvers, and live-action authority in `00_project/PROJECT.md`.
3. Request available brand, product, audience, market, analytics, legal, product, sales, campaign, and prior-strategy materials.
4. Maintain `00_project/SOURCE_INVENTORY.md`: locator, owner, version/date, access state, whether actually read, relevance, conflicts, and clarification needed.
5. Inspect supplied sources before asking detailed Brief gaps. Do not infer from inaccessible/unread files or reuse another brand's materials without explicit direction.

## 2. Canonical ownership and dependency order

Foundation path:

`Source Inventory -> Requested Deliverable Scope -> Constructed Brief -> {Approved Scope + Approved Brief} -> Approved MRD -> selected Ready targets`

- Deliverable Scope owns selected documents, template variants, module IDs, audiences, and explicit exclusions.
- Marketing Brief owns the selected question set and current user/evidence answers, including mapped TBA.
- MRD owns cross-document requirements, core marketing decisions, evidence conclusions, constraints, dependencies, and target readiness.
- `marketing-analyst` owns Scope, Brief, MRD, selected strategy types, Brand Book, SMM Playbook, Content Plan, Discoverability, Paid Media planning/audit, and Earned/Partner Activation. The library defines strategic scope separately from the detailed product-marketing artifacts below.
- `product-marketing-agent` owns Product Marketing Foundation, Pricing/Packaging, GTM/Launch, Conversion/Onboarding, Lifecycle/Retention/Referral, Sales Enablement/Outreach, Conversion Copy Deck, and Creative Brief.
- Product Marketing Foundation owns product-specific positioning/messaging/proof. Brand Book owns brand-wide platform, voice, visual identity, and applications.
- Ideas & Insights Log is a working register, not an approved strategy.

Applicable dependency path:

`MRD -> Product Marketing Foundation when selected -> applicable Pricing/Brand/Strategy decisions -> selected activation, experience, enablement, copy, and creative artifacts`

`Approved SMM Playbook + applicable Approved upstream decisions -> Content Plan`

No peer artifact is a prerequisite when it is not selected or its decisions are not consumed. Selected artifacts may proceed independently when their own target/module readiness is `Ready`.

## 3. Deliverable Scope and Brief constructor

1. Copy [Scope Matrix](./DELIVERABLE_SCOPE_MATRIX_TEMPLATE.md) to `02_working/DELIVERABLE_SCOPE_MATRIX.md`; record initial user choices as `Requested`.
2. Present exact document, template, and module choices. Add evidence-led `Required`, `Recommended`, or `Optional` rationale; never omit a module silently.
3. Filter the [Brief Question Library](./MARKETING_BRIEF_QUESTION_LIBRARY.md) and linked owner-specific question resources against requested module IDs. Include a row only when its target intersection and `Include when` trigger both match; record the project fact that satisfied any additional trigger. Unknown additional trigger -> include the row for confirmation rather than assuming it false.
4. Copy [Modular Brief Template](./MARKETING_BRIEF_TEMPLATE.md) to `02_working/MARKETING_BRIEF.md`; preserve each selected question's exact ID, wording, selected-target mapping, purpose, and gate in its Manifest/answer register.
5. Prefill supported answers from inspected sources. Ask only material gaps, grouped by block and target consequence.
6. Use `Answered`, `TBA`, or `Not applicable`. Never replace missing evidence with an assumption. `Not applicable` needs rationale and approval.
7. Build one dependency row for every TBA-selected-target intersection; classify it `Blocking`, `Supporting`, or `Not used` from library defaults. Reclassification needs rationale and explicit user approval.
8. Set Scope and Brief `Ready for Review`. Approval confirms selections, answers, TBA list, mappings, and readiness, not that TBA is answered.

Scope added later -> version Scope and Brief, add only newly triggered questions, recalculate readiness, and update affected dependents. Scope removed later -> preserve the change history and remove its questions from the active Manifest only after approval.

## 4. Target-level TBA and readiness

- `Ready`: every Blocking input for the target/module is `Answered` or justified `Not applicable`.
- `Partially Ready`: a document has both selected Ready and selected Blocked modules.
- `Blocked`: at least one selected-target Blocking input is TBA.
- `Not selected`: outside Approved Scope.

Blocked target/module -> STOP only that target/module, list question IDs and needed answers, then continue independent Ready work. A document cannot be Approved while one of its selected modules is Blocked; Ready modules may be drafted/reviewed separately with explicit boundaries.

Valid TBA resolutions: confirmed user answer; research-supported answer; agent proposal explicitly approved by the user; or `Not applicable` with rationale. Update the Brief answer, basis, dependency register, and affected readiness.

## 5. MRD

Create MRD after Scope and Brief approval. It contains:

- current Approved Scope, Brief, and Brief Question Set versions;
- business context, `MRD-CORE` decisions/requirements, evidence, constraints, dependencies, legal/brand rules, and measurement requirements;
- one deliverable requirement/readiness row for every selected target/module;
- Brief Dependency and TBA Register covering every active TBA-target intersection;
- semantic change history and approval block.

MRD approval requires every Blocking input for `MRD-CORE` resolved or justified `Not applicable`, complete downstream TBA mappings/consequences/owners, current readiness, and no ambiguous approval. A downstream-only TBA may remain; it blocks only its mapped target. Promote Approved Scope, Brief, and MRD to `04_approved/internal`.

## 6. Selected artifacts, handoffs, and Content Plan

- Create only selected Ready artifacts/modules from ready templates. Additional research may deepen a specialist decision but cannot silently revise Approved upstream meaning.
- When Product Marketing Foundation is selected, create and approve it before dependent product-specific positioning, pricing, brand-message, GTM, conversion, lifecycle, sales, copy, or creative decisions. When it is not selected, use applicable Approved MRD decisions without creating a hidden artifact.
- Every artifact receives its own review and approval. Working copies may contain internal controls; promotion requires the destination and sanitization rules in Project Structure.
- Content Plan requires an Approved SMM Playbook plus only the applicable upstream decisions its selected modules consume. A blocked Paid Plan, GTM module, Brand module, or other artifact does not block unrelated Content Plan work.
- Creative Brief hands visual design/production to `design-agent`. Conversion/product/CRM/data/billing/automation/code requirements hand to business/technical/implementation owners.
- Apply [Activation Governance](../shared/marketing-activation-governance.md). No audit, plan, draft, or approval silently authorizes a live action.

## 7. Status, approval, and sanitization

Every project document header contains `Status`, `Version`, `Last updated`, `Approved by`, and `Approved on`. Allowed statuses: `Draft`, `Ready for Review`, `Approved`, `Needs Update`, `Superseded`.

- Explicit approval applies only to the unambiguous version under review. Silence is not approval; multiple ambiguous documents -> ask which was approved.
- Meaningful edits return the document to `Ready for Review`; spelling/formatting and non-semantic sanitization do not.
- Client outputs retain useful citations and limitations but remove internal provenance labels, source classes, scope recommendations, blockers, technical notes, and unapproved hypotheses.
- A TBA may remain only in internal canonical documents and review materials. A client/handoff artifact must show the resulting limitation/readiness, not expose an unexplained placeholder.

## 8. Ideas, consistency, and change propagation

Store `06_ideas/IDEAS_INSIGHTS_LOG.md` entries with ID; type (`User Idea`, `Research Insight`, `Agent Hypothesis`); content; author/time; provenance; validation/confidence; alignment; approval; use state; and destination reference. Approval makes a proposal a decision, not an unsupported fact.

Before semantic change: identify the canonical upstream artifact; list impacted target/module IDs; version it; mark affected dependents `Needs Update`; update in dependency order; reapprove changed meaning; mark replaced versions `Superseded`; archive them. Source conflict -> show both claims, provenance, reliability, likely cause, and decision impact; request adjudication when evidence cannot resolve it.
