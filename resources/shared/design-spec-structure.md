# Design Spec Structure

Use for feature-specific design specs stored at `docs/design/<feature-name>.md`.

## Core Format

```md
# Design Spec: [Feature Name]

## 1. Goal & Users

## 2. Visual Direction

## 3. Screen Inventory

## 4. Layout & Hierarchy

## 5. Components & States

## 6. Tokens

## 7. Responsive Behavior

## 8. Accessibility

## 9. Implementation Notes

## 10. Open Questions
```

## Required Content Rules

- Use natural language, not CSS dumps.
- Keep the file feature-specific. Reference a project-level design system instead of duplicating it.
- In `Components & States`, cover empty/loading/error/success/permission states when relevant.
- In `Tokens`, list only tokens that matter for this feature: color, type, spacing, radius, shadow, motion.
- In `Implementation Notes`, capture details the frontend implementation would otherwise have to infer.

## Guardrails

- Keep section order stable unless the feature truly needs an extra section.
- If a section does not apply, write `N/A`.
- Do not copy external style catalog text directly into the spec.
- Do not invent missing rules. Derive them from approved project docs or approved design inputs only.
