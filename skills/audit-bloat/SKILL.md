---
name: audit-bloat
description: "Audit a repository for dead code and overengineering when repo-wide cleanup analysis is requested; deletions require approval."
---

# Audit Bloat

Repo-wide hunt for code that should not exist. Apply the simplest sufficient design across the whole tree, not just the current change. Rank findings biggest cut first.

## Scope
Complexity and dead code only. Correctness bugs, security holes, and performance regressions go to `code-reviewer`, not here.

## Hunt
- Dead code: unreferenced functions/vars/files, commented-out blocks, unreachable branches, dead flags/config.
- Reinvented stdlib: hand-rolled logic the standard library already ships.
- Avoidable deps: a dependency doing what stdlib or the platform already covers; single-use deps.
- Speculative abstraction (YAGNI): interface/factory/wrapper with one implementation or one caller; config nobody sets.
- Shrinkable: same logic in far fewer lines.

## Procedure
1. Map the tree (Glob); skip `node_modules`, `.git`, build output, vendored/generated/lock/minified files.
2. Grep for unreferenced symbols, commented-out blocks, single-impl interfaces, wrappers that only delegate.
3. Confirm each candidate is truly unused by grepping its references repo-wide before listing it - no guessing.
4. Rank findings: biggest line/dep cut first.

## Output
One line per finding, ranked:
`<tag> <what to cut>. <replacement>. [path:line]`

Tags: `delete:` nothing replaces it · `stdlib:` name the function · `native:` name the feature · `yagni:` one impl/caller · `shrink:` show the shorter form.

End with `net: -<N> lines, -<M> deps possible.` Nothing to cut: `Lean already. Ship.`

## Boundaries
- Lists findings; deletes nothing until the user approves the cuts.
- On approval, apply the surgical-change rules: remove only listed items, match style, every removal traced to a listed finding.
- A smoke test or a `shortcut:`-marked simplification is intentional, not bloat - never flag it.
