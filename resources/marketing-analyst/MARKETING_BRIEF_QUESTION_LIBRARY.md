# Marketing Brief Question Library

Library state: Ready for use

This file is the canonical router for the modular Marketing Brief. The question rows live in two owner-specific resources so responsibility stays explicit without duplicating shared questions. Apply the [Marketing Document Dependency Standard](../shared/marketing-document-dependency-standard.md) and decode every module ID through the [Deliverable Scope Matrix](./DELIVERABLE_SCOPE_MATRIX_TEMPLATE.md).

## Coverage contract

A constructed Brief is input-complete when it contains every triggered question for every selected target/module, each with an answer state, basis, target mapping, purpose, and exact TBA consequence. It gathers user-controlled facts, constraints, existing decisions, evidence availability, and open decision authority. It does not replace market/customer/competitor research, inspection of supplied sources, account or experience audits, current-platform verification, or specialist analysis.

- For an inventory question, a confirmed `none exists` is an `Answered` input and creates a visible research or evidence limitation.
- For a choice question, `Open for recommendation` is `Answered` only when the decision owner, evaluation constraints, and approval point are known.
- For a value required to approve a target, `unknown` remains `TBA`; do not convert absence of an answer into permission to choose.
- Prefill from inspected sources before asking the user. When all documents are selected, present unresolved questions in manageable blocks, not as one undifferentiated questionnaire.

## Row semantics and routing

Every row has six fields:

1. `ID`: stable provenance and dependency key.
2. `Exact question or parameter`: wording copied unchanged into the Brief.
3. `Include when`: target selection plus any additional project-shape trigger.
4. `Used by`: exact document/module sections consuming the answer.
5. `Why needed`: the decision, analysis, or output field this input supports.
6. `Gate when TBA`: default Blocking intersections; every other listed use is Supporting unless an Approved Scope or MRD records a user-approved reclassification.

`Mapped target selected` means at least one exact target or wildcard in `Used by` intersects the selected module IDs. `All` means every selected target. Prefix matches such as `BB-*` mean every selected module with that prefix. `All customer-facing modules` means selected `STR-*`, `BB-*`, `SMM-*`, `CP-*`, `DISC-CONTENT`, `DISC-AI`, `DISC-ASO`, `PAID-*`, `EARN-*`, `PMF-*`, `PRICE-*`, `GTM-*`, `CONV-*`, `LIFE-*`, `SALES-*`, `COPY-*`, and `CREATIVE-*` modules containing external claims or experiences.

Evaluate additional triggers from inspected sources and scope answers. If a trigger is still unknown, include the row as a confirmation question; do not assume it is false. A confirmed false trigger may be omitted, or retained as `Not applicable` with rationale when it was already asked.

## Module prefix legend

| Prefix | Document |
|---|---|
| `MRD` | Market Requirements Document |
| `STR` | Selected strategy types and general Marketing Strategy variants from the approved project strategy templates |
| `BB` | Brand Book |
| `SMM` | SMM Playbook |
| `CP` | SMM Content Plan |
| `DISC` | Discoverability Audit and Map |
| `PAID` | Paid Media Plan and Audit |
| `EARN` | Earned and Partner Activation |
| `PMF` | Product Marketing Foundation |
| `PRICE` | Pricing and Packaging Decision |
| `GTM` | GTM and Launch Plan |
| `CONV` | Conversion and Onboarding Review |
| `LIFE` | Lifecycle, Retention, and Referral Program |
| `SALES` | Sales Enablement and Outreach |
| `COPY` | Conversion Copy Deck |
| `CREATIVE` | Creative Brief |

Strategy selection uses the Scope Matrix's module mappings. `STR-*` may apply to multiple separate strategies; qualify each selected target with its document type and narrow each question's uses and readiness consequences to that target. A shared module prefix does not select another strategy or make it a prerequisite.

## Question resources by owner

| Owner | Blocks | Question resource | Coverage |
|---|---|---|---|
| `marketing-analyst` | A-I and L | [Marketing analyst documents and shared foundation](./MARKETING_ANALYST_DOCUMENT_QUESTIONS.md) | Shared project/governance, objectives, audience/VOC/JTBD, market/brand/positioning, product/offer/experience, budget/capacity/timing/access; Marketing Strategy, Brand Book, SMM/Content Plan, Discoverability, Paid, and Earned/Partner inputs |
| `product-marketing-agent` | J-K and M-O | [Product marketing documents](../product-marketing-agent/PRODUCT_MARKETING_DOCUMENT_QUESTIONS.md) | Lifecycle, sales, conversion/copy/creative, pricing/packaging, and GTM/launch inputs |

Shared blocks A-F remain in the `marketing-analyst` resource because that agent owns the Brief and MRD. Product Marketing Foundation consumes A-E directly; the product resource adds only specialist inputs and never duplicates a shared question.

## Constructor verification

- Every selected module resolves to at least one non-universal question in the linked question resources.
- Every included row satisfies both its target intersection and `Include when` trigger.
- Every included question appears once in the Brief and carries its exact `Used by`, `Why needed`, and gate fields narrowed to selected targets.
- Unselected modules and unmet shape triggers create no question and no blocker.
- Project-specific questions require a stable ID, exact wording, trigger, target mapping, purpose, gate condition, and source basis.
