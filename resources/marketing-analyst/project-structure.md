# Marketing Project Structure

Ask for or identify the active project's `<brands-root>` before creating files.

```text
<brands-root>/
  <brand-slug>/
    00_project/
      PROJECT.md
      SOURCE_INVENTORY.md
    01_sources/
      user/
    02_working/
      MARKETING_BRIEF.md
      DELIVERABLE_SCOPE_MATRIX.md
      MRD.md
      MARKETING_STRATEGY.md
      BRAND_BOOK.md
      SMM_PLAYBOOK.md
      activation/
        DISCOVERABILITY_AUDIT_AND_MAP.md
        PAID_MEDIA_PLAN_AND_AUDIT.md
        EARNED_PARTNER_ACTIVATION.md
      product-marketing/
        PRODUCT_MARKETING_FOUNDATION.md
        PRICING_PACKAGING_DECISION.md
        GTM_LAUNCH_PLAN.md
        CONVERSION_AND_ONBOARDING_REVIEW.md
        LIFECYCLE_RETENTION_REFERRAL.md
        SALES_ENABLEMENT_OUTREACH.md
      handoffs/
        CONVERSION_COPY_DECK.md
        CREATIVE_BRIEF.md
      content-plans/
    03_research/
      EVIDENCE_REGISTER.md
      <research-id>.md
    04_approved/
      internal/
        MARKETING_BRIEF.md
        DELIVERABLE_SCOPE_MATRIX.md
        MRD.md
        PRODUCT_MARKETING_FOUNDATION.md
        PRICING_PACKAGING_DECISION.md
      client/
        MARKETING_STRATEGY.md
        BRAND_BOOK.md
        SMM_PLAYBOOK.md
        <approved-audit-plan-or-playbook>.md
      handoffs/
        CONVERSION_COPY_DECK.md
        CREATIVE_BRIEF.md
    05_content_plans/
      <yyyy>/
        <period>_CONTENT_PLAN.md
    06_ideas/
      IDEAS_INSIGHTS_LOG.md
    07_archive/
      <artifact-name>/
        <artifact>_<version>_<yyyy-mm-dd>.md
```

## Directory rules

- `<brand-slug>` is stable lower-kebab-case. A brand is the highest project-material level below `<brands-root>`.
- `00_project` stores project language, scope, owners, approvers, and the inventory of every received, read, inaccessible, disputed, or superseded source.
- `01_sources/user` stores immutable user-supplied originals. Record versions and checksums in Source Inventory when practical; do not edit originals.
- `02_working` stores drafts and review candidates. It may contain internal provenance labels, source classifications, blockers, scope matrices, technical notes, and unapproved hypotheses. Create brand-specific copies here from agent resources.
- `03_research` stores research plans, notes, source records, and the Evidence Register. Research files belong only to this brand.
- `04_approved/internal` stores current Approved Scope, Brief, MRD, Product Marketing Foundation, and Pricing/Packaging decisions with the evidence, classifications, and traceability required by their canonical roles.
- `04_approved/client` stores sanitized client-facing strategies, books, playbooks, plans, audits, reviews, and enablement artifacts. `04_approved/handoffs` stores exact-version Copy Deck and Creative Brief handoffs. Do not place files directly in `04_approved`.
- `05_content_plans` stores Approved plans by coverage year and period. Keep draft plans under `02_working/content-plans`.
- `06_ideas` stores the working Ideas & Insights Log; an entry is not a strategic decision unless promoted into an Approved canonical document.
- `07_archive` stores replaced versions. Set their document status to `Superseded`; do not delete the audit trail.

## Version movement

1. Start or revise a document in `02_working` with `Draft` status.
2. Set it to `Ready for Review` without moving it.
3. On explicit approval, record approver/date/version. If an older Approved version exists, mark it `Superseded` and move it to `07_archive/<artifact-name>/`.
4. Move an Approved Scope, Brief, MRD, Product Marketing Foundation, or Pricing/Packaging Decision to `04_approved/internal`. Move a sanitized approved client artifact to `04_approved/client`, Copy/Creative handoffs to `04_approved/handoffs`, and an Approved Content Plan to `05_content_plans/<yyyy>/`.
5. For later material changes, copy the current Approved version back to `02_working`, increment the version, and preserve the current Approved file until its replacement is approved.

## Approval promotion gate

- Approved Brief may retain mapped `TBA`. Approved MRD may retain downstream-only TBA, but no Blocking input for `MRD-CORE`, incomplete TBA mapping, or unresolved MRD blocker.
- Internal Approved documents retain required evidence provenance, source classification, Deliverable Scope, decision history, and resolution registers.
- Before promotion to `04_approved/client`, remove internal provenance labels, source classifications, blockers, scope matrices, technical comments, and unapproved hypotheses.
- Keep client-useful citations, footnotes, source lists, assumptions, and limitations needed to support material external facts and quantitative claims.
- Sanitization does not change meaning. A semantic edit returns the document to `Ready for Review` and requires approval again.

## Isolation and reuse

- Every source, Brief, MRD, research note, evidence record, working file, approved artifact, Content Plan, idea, and archive version stays inside its brand directory.
- Never place two brands in one project directory or use one brand's material for another without explicit user direction.
- Only brand-neutral templates, methods, and agent instructions belong in `resources/marketing-analyst/`, `resources/product-marketing-agent/`, or applicable `resources/shared/` files.
