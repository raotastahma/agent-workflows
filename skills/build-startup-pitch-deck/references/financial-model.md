# Supporting Financial Model

## Purpose

Build an auditable operating model that substantiates the deck's business model, three-year plan, funding requirement, milestones, and financial charts. Do not create numbers merely to fill slides.

Use the caller's available spreadsheet tooling. Default to 36 monthly periods for a three-year plan; aggregate verified monthly results into annual deck outputs.

## Minimum Workbook

Include only the necessary sheets:

- `Cover`: purpose, version, currency, units, scenario, as-of date, and model status
- `Assumptions`: editable drivers, scenario selector, source/owner, and notes
- `Drivers`: customer, volume, pricing, retention, hiring, and cost schedules
- `Model`: monthly revenue, COGS, gross profit, OPEX, operating result, and cash
- `Scenarios`: downside, base, and upside driver sets
- `Deck Outputs`: annual summaries, KPIs, charts, ask, uses, and milestones
- `Checks`: decomposed controls with actual, expected, difference, tolerance, status, and fix location
- `Sources`: input, value, units, period, source, URL/reference, accessed date, and notes

## Core Mechanics

- Put inputs in dedicated cells; calculations must reference them.
- Separate historical actuals, estimates, assumptions, targets, and forecast periods visually.
- Calculate revenue from operating drivers.
- Calculate COGS from unit costs, variable rates, infrastructure, fulfillment, or delivery capacity as appropriate.
- Calculate headcount cost by role, hire date, salary/OTE, employer costs, and ramp where material.
- Calculate other OPEX by explicit driver, schedule, or labeled assumption.
- Roll cash as `Beginning cash + collections + financing - cash expenses - capex = Ending cash`.
- Define net burn as positive cash consumed during the period; do not report negative burn.
- Calculate runway from the cash schedule and the first projected funding shortfall. Use cash divided by recent positive net burn only as a clearly labeled approximation.
- Calculate the funding requirement from cash needed to reach specified milestones plus an explicit buffer; do not back-solve it from a desired headline.
- Drive downside, base, and upside from assumption sets. Never paste scenario outputs.

## Deck Outputs

Create a compact output table with stable labels and exact source ranges for:

- Revenue and growth
- Gross profit and gross margin
- Operating expenses and operating result
- Ending cash, net burn, and runway
- Customers, volume, retention, or other business-specific operating KPIs
- Headcount
- Funding ask, use of funds, and milestone dates

Build deck charts only from verified `Deck Outputs` ranges. Record each used range in the evidence ledger. Keep workbook values at calculation precision and control rounding in display formats.

## Model Integrity

- Cite hardcoded researched inputs in cell comments and `Sources`.
- Mark founder inputs separately from externally verified inputs.
- Guard formulas against invalid denominators and insufficient data.
- Use copy-across-consistent formulas and avoid hidden magic numbers.
- Add checks for source completeness, scenario validity, revenue build, headcount roll-forward, totals, cash roll-forward, signs/units, deck-output ties, and formula errors.
- `MODEL STATUS` passes only when every required check passes. A disclosed missing input is not a passing check.
