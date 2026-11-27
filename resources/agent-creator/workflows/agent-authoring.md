# Agent Authoring Workflow

Use when creating one new agent or editing one existing agent.

1. Define goal, inputs, outputs, ownership, non-goals, handoff target.
2. Read analogous agents in `agents/`.
3. Read `resources/agent-creator/references/agent-frontmatter.md`.
4. Discover capability sources: installed skills and relevant resources. For a new agent, also research external capability sources; for an existing agent, search externally only when local coverage is insufficient or the user requests it.
5. Compare applicable candidates and decide whole-skill vs fragment/idea vs skip.
6. Present findings and proposed agent design for user approval before editing.
7. Reuse local section order when it improves consistency.
8. Write critical rules first; keep runtime instructions short and enforceable.
9. Add skills only with a clear trigger and context-cost benefit.
10. Put every-session rules in the agent file.
11. Put templates, examples, checklists, and rare details in resources.
12. Select practical tools: enough to complete and verify quickly.
13. If a proven dependency/CLI avoids fragile manual work, include/install it and verify.
14. Verify frontmatter, line count, referenced files, and duplicate blocks.

Default sections:

1. Critical Rules / Principles
2. Skills
3. Inputs & References
4. Workflow
5. Verification
6. Escalation / STOP protocol
