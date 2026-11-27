# Agents and Skills

Reusable instructions for AI-assisted project work, written and refined in my own agent collection. This edition contains 12 specialist roles, two custom skills, and their supporting briefs, checklists, and handoff rules. They cover discovery, architecture, project management, design, marketing, review, QA, documentation, quantitative research, and risk assessment.

Each role defines its inputs, ownership, working procedure, verification, and stop conditions. The files are actual working instructions adapted for reuse. They do not start an agent, configure a model, or grant tool access.

## Use a role

Clone or download this repository. Give your agent runtime read access to the collection and your project. Select one role and state the project, task, inputs, output, and allowed actions:

```text
Read project-rules.md and agents/business-analyst.md from the agent-workflows
collection. Follow that role for this task; do not spawn another agent.

Project: the current repository.
Task: turn the supplied customer request into a scoped PRD.
Inputs: the request and existing product documents in this project.
Output: docs/prd-account-export.md and the analyst handoff.
Ask about material missing requirements before drafting. Do not implement code.
```

Use the actual location of the downloaded collection in your prompt. Markdown links inside it resolve relative to their file. Backticked `resources/`, `agents/`, `skills/`, and `project-rules.md` paths identify collection files; `docs/` and `tasks/` paths identify the project being worked on. Keep the directory structure intact so conditional references remain usable.

Configure your runtime's model, reasoning level, tools, filesystem permissions, and network access yourself. These files contain no personal model assignments. Read the selected role and load its references only when their trigger applies.

## Choose the right role

| Role | Use it for | Main result |
|---|---|---|
| [Business analyst](agents/business-analyst.md) | Clarify what is needed and why | Scoped PRD, confirmed decisions, architect handoff |
| [System architect](agents/system-architect.md) | Turn approved requirements into exact technical contracts | Architecture, schemas, API and migration decisions |
| [Project manager](agents/pm-agent.md) | Break approved work into tasks and identify what needs a human decision | Specialist briefs, dependency order and task registries |
| [Design agent](agents/design-agent.md) | Specify source-led interfaces and creative work | Flows, states, tokens, accessible design handoff |
| [Marketing analyst](agents/marketing-analyst.md) | Define marketing scope, gather inputs, coordinate strategy work | Modular Brief, readiness register, selected marketing artifacts |
| [Product marketing agent](agents/product-marketing-agent.md) | Develop selected positioning, pricing, launch, lifecycle, copy, or creative work | Product-specific decisions and bounded handoffs |
| [Code reviewer](agents/code-reviewer.md) | Review a concrete implementation against its contract | Prioritized evidence and a review verdict |
| [QA agent](agents/qa-agent.md) | Verify implemented behavior and required checks | Test evidence, observed failures, QA verdict |
| [Knowledge agent](agents/knowledge-agent.md) | Keep documentation consistent with the implementation | README, changelog, onboarding, manuals |
| [Quant analyst](agents/quant-analyst.md) | Research models, data, strategy hypotheses, and backtests | Reproducible analysis with bias and uncertainty limits |
| [Risk manager](agents/risk-manager.md) | Assess portfolio, model, liquidity, and operational risk | Calculated exposure, stress cases, constraints and gaps |
| [Agent creator](agents/agent-creator.md) | Maintain role instructions and their handoffs | Source-backed design, approved edits, verification |

For implementation handoffs, name the person or specialist who owns that part of your project.

## Use a skill

Skills supply a bounded workflow instead of a full role. Read the relevant `SKILL.md` directly, or install that directory through your runtime's supported skill mechanism. This repository has no installer or runtime dependency.

| Skill | What it does | Example request |
|---|---|---|
| [Audit bloat](skills/audit-bloat/SKILL.md) | Finds verified dead code and unnecessary complexity; lists proposed cuts before deletion | "Use this skill to audit the current repository. Return ranked findings and evidence. Do not edit files." |
| [Build startup pitch deck](skills/build-startup-pitch-deck/SKILL.md) | Coordinates a sourced deck with a verified supporting workbook | "Use this skill with the supplied outline, company materials, and model inputs. Deliver the editable deck and workbook." |

The pitch skill requires presentation and spreadsheet creation/rendering capabilities supplied by your runtime. Its France profile is a reusable, user-commissioned deck outline, not an official visa requirement or eligibility assessment.

## Combine the instructions

For a feature, start with the business analyst, use architecture and design where needed, then hand implementation to your project's owner. Review the actual changes, run QA against the implemented behavior, and update documentation from the verified result. The handoff checklists keep each stage's inputs explicit. Review and QA status transitions assume a project task file; for an ad hoc audit, request the report without task-file changes.

For marketing work, begin with the [Scope Matrix](resources/marketing-analyst/DELIVERABLE_SCOPE_MATRIX_TEMPLATE.md), then construct the [Brief](resources/marketing-analyst/MARKETING_BRIEF_TEMPLATE.md) using its [question library](resources/marketing-analyst/MARKETING_BRIEF_QUESTION_LIBRARY.md). An unanswered budget question can block a paid-media budget module while unrelated brand work continues. The [dependency standard](resources/shared/marketing-document-dependency-standard.md) defines that behavior. Supply or approve the templates for final strategy, MRD, and specialist deliverables in your project; this edition includes the reusable intake and control system, rather than every local artifact template.

## Scope and reuse

These are instructions, not a sandbox or a claim of autonomous production readiness. Your runtime must enforce permissions. Quantitative roles perform research and assessment; they do not place or route live orders. An instruction to prepare a plan or draft does not authorize publication, external communication, deployment, spending, or account changes.

Installed third-party skill packages, private project material, local service access, and personal runtime settings are excluded. The collection contains original roles and authored portions of custom workflows. See [NOTICE.md](NOTICE.md) for credit and reuse scope.

You may use and adapt the included work under [LICENSE](LICENSE). Keep the copyright and permission notice with copies. No third-party runtime or upstream package is licensed by this repository.
