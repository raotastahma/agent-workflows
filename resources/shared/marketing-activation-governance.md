# Marketing Activation Governance

Use for discoverability, conversion, paid media, lifecycle, launches, earned/partner programs, sales enablement, outreach, copy, and creative work.

## 1. Authority boundary

Default output is an audit, strategy, specification, draft, or handoff. It does not authorize publishing, sending, outreach, spend, bidding, account edits, CRM/CMS changes, code changes, price changes, contracts, list acquisition, data collection, or product behavior changes.

Live action requested -> require explicit approval of the exact action, target, current state, proposed change, expected effect, rollback or recovery path, operator, and monitoring owner. An agent whose role is strategy-only hands execution to the authorized owner instead of acting.

## 2. Audit truthfulness

Use only these check states:

| State | Meaning |
|---|---|
| `Pass` | Required evidence was inspected and satisfies the stated criterion |
| `Fail` | Required evidence was inspected and violates the stated criterion |
| `Unknown` | Evidence needed to judge was unavailable, inaccessible, stale, or incomplete |
| `Not applicable` | The check does not apply; rationale is recorded |

Keep two measures separate:

- Evidence coverage: applicable checks with enough evidence to judge divided by all applicable checks.
- Observed health: Pass checks divided by Pass plus Fail checks.

`Unknown` reduces coverage, never health. Do not publish one aggregate score when material areas are Unknown; present findings and coverage instead.

## 3. Handoff and completion gate

- Separate strategic decisions from design, technical, operational, legal, and live-system implementation requirements.
- Handoff names exact assets, versions, owners, acceptance evidence, unresolved dependencies, prohibited actions, and post-change monitoring.
- A target is complete only when its selected modules are Ready, required evidence is traceable, Unknowns and limitations are visible, live actions remain unexecuted unless separately authorized, and explicit approval is recorded.
