---
name: build-startup-pitch-deck
description: "Create or repair fundraising and innovation-visa pitch decks with supporting financial workbooks, including France Talent Passport deliverables. Not for sales or board decks."
---

# Build Startup Pitch Deck

Create the deck and its supporting workbook as one evidence system. Treat the workbook as the source of truth for every projected or financial claim.

## Critical Rules

- User structure, required sections, slide counts, reference deck, and template are hard constraints. Change them only with explicit approval.
- User feedback or revision comments -> apply each change to the current deck or workbook in place. Create a separate file and leave the current file unchanged only when the user explicitly requests a new version.
- Missing source or decision required for a material claim or model driver -> STOP and request it. Never invent traction, customers, market facts, financials, credentials, or eligibility.
- Label founder-provided facts, externally verified facts, estimates, assumptions, targets, and missing data distinctly in working materials.
- Build and verify the Excel model before drafting slides that depend on projections, market sizing, unit economics, funding, or milestones.
- Map every deck number to an exact workbook cell or range. Keep currency, units, period, scenario, and rounding consistent.
- Cite external claims and assets in slide notes. For every slide claim based on external research or authoritative online data, also add a small, readable `Source:` or `Sources:` line at the bottom of the slide and hyperlink each source label to the exact supporting page. Cite researched model inputs in cell comments and the Sources sheet.
- Write every slide title as a one-line, plain-language conclusion; a reader without specialized knowledge must understand the slide's subject and point at first glance.
- Write all deck text for people, not agents: use professional, natural, direct language that readers without specialized knowledge can understand. Explain unavoidable domain terms in plain language.
- Do not use U+2014 in generated prose.
- Use accent colors only to communicate meaning, grouping, hierarchy, or intended focus; never add an accent solely for decoration.
- A slide outline is not completion when the user requested deliverable files. Return an editable deck and workbook.

## Workflow

1. **Lock the brief.** Inspect every supplied document, screenshot, deck, workbook, brand asset, and source. Record audience, decision sought, language, output format, stage, raise, geography, and required structure. Read [deck-workflow.md](references/deck-workflow.md). For the supplied France outline, also read [france-talent-passport.md](references/france-talent-passport.md).
2. **Build the evidence ledger.** For each required slide, record the intended takeaway, supporting evidence, source, date, visual, workbook link, and status. Research current external claims from primary or official sources. Ask for all material missing inputs in one focused batch.
3. **Create the model first.** Read [financial-model.md](references/financial-model.md). Use the caller's available spreadsheet tooling. Build the model from business-specific drivers, not a generic growth curve. Verify formulas, checks, scenarios, sources, and visual output; then export the `.xlsx`.
4. **Write the investor story.** Work inside the locked structure. Apply the writing rules in [deck-workflow.md](references/deck-workflow.md), keep one idea per slide, and use speaker notes to add context without duplicating the canvas.
5. **Design the deck.** Follow the supplied brand, reference deck, or template. Use the caller's available presentation tooling for composition, rendering, and visual checks. Use actual product evidence and verified model outputs; do not add decorative elements that obscure the argument.
6. **Reconcile and verify.** Read [quality-gates.md](references/quality-gates.md). Reconcile the deck against workbook outputs, render every slide and user-facing sheet, fix all meaningful content, formula, clipping, wrapping, overlap, and consistency defects, and deliver only after every mandatory gate passes.

## Deliverables

- Editable `.pptx` or native Google Slides deck in the requested language and format.
- Editable `.xlsx` or Google Sheets-ready financial model.
- Sources embedded in slide notes and workbook audit fields; do not deliver scratch ledgers unless asked.
- When the user explicitly requests a new version, preserve the current file and export a separate copy.

## References

- [deck-workflow.md](references/deck-workflow.md) - intake, research, narrative, copy, and visual direction.
- [financial-model.md](references/financial-model.md) - workbook architecture, driver logic, scenarios, and deck outputs.
- [quality-gates.md](references/quality-gates.md) - evidence, model, reconciliation, narrative, and visual acceptance gates.
- [france-talent-passport.md](references/france-talent-passport.md) - user-supplied 18–19 slide France profile.
