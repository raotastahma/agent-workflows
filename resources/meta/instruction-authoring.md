# Instruction Authoring

- Write instructions like shell comments.
- Put critical rules first.
- `CLAUDE.md` = only always-on rules.
- `AGENTS.md` = only always-on rules.
- `agents/*.md` = runtime role rules.
- `resources/` = templates, references, situational details.
- `skills/` = reusable workflows loaded on demand.
- Prefer short directives over explanations.
- Remove duplicate rules unless duplication prevents context switching for non-parallel roles.
- Move templates, examples, and long references out of runtime files.
