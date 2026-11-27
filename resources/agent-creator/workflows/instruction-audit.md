# Instruction Audit Workflow

Use when optimizing existing agents, resources, skills, AGENTS.md, or CLAUDE.md.

1. Map requested agents, resources, skills, AGENTS.md, and CLAUDE.md files.
2. Read `resources/meta/instruction-authoring.md`.
3. Remove duplicate instructions and zero-utility prose.
4. Find contradictions between agents and resources.
5. Find legacy resources: unused, duplicated, or replaced.
6. Propose delete, merge, or move into agent references; do not delete without request.
7. Compare analogous agents for structure, frontmatter, skills, verification, and escalation gaps.
8. Add only missing instructions that materially improve task execution.
9. If a rule is scenario-only, move it to a resource.
10. If multiple agents can share a resource without quality loss, move it to shared resources.
11. Verify line counts, links, and that every changed line traces to the request.
12. Check skill descriptions against realistic requests and nearby skills; ordinary topic overlap must not activate unrelated workflows.

## Optimization Gate

Use for behavior-driven instruction changes:
- Rollout: define 3-7 representative tasks or documented behavior records.
- Reflect: separate failure patterns from success patterns; failures take priority.
- Aggregate: merge duplicate or conflicting candidate edits.
- Select: rank by systematic impact, gap coverage, generality, and actionability.
- Budget: apply 1-4 approved edits per pass unless the user approves more.
- Gate: accept only changes that improve or preserve required behavior on the representative set.
- Preserve: treat effective deterministic defaults, commands, templates, fallback paths, and standalone resource contracts as behavior; do not generalize or remove them for compactness alone.
- Move: verify equivalent destination content, relative links, and discoverability before replacing instructions with a reference.
- Reject: report skipped edits with reason: duplicate, too broad, unverified, or harmful.
- Meta notes belong in resources or a project behavior log, not runtime agent files.

## AGENTS.md / CLAUDE.md

- When paired with AGENTS.md, CLAUDE.md = `@AGENTS.md` only.
- Keep global/project files token-minimal: only critical always-on rules.
- Do not create these files if no always-on rule is needed.
- Put each instruction in the narrowest applicable global/project file.
- Prevent conflicts between global and project instructions.
