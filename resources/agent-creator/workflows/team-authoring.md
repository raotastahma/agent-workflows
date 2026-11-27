# Team Authoring Workflow

Use when creating a connected group of agents.

Design teams as a handoff lifecycle, not a pile of roles:

`discovery/requirements -> design/spec -> task decomposition -> implementation -> review -> QA -> release -> documentation`

1. Identify the project's full delivery cycle, starting from raw idea when needed.
2. Create only roles needed to run that lifecycle.
3. Assign each agent one output artifact or bounded specialty.
4. Define each handoff artifact.
5. Define owner and non-owner files per agent.
6. State sequential and parallel pairs explicitly.
7. Raw idea -> discovery/requirements before architecture; one agent may own questions, research, scope, and the target requirements artifact.
8. Design/spec starts from confirmed requirements and produces the UI, architecture, API, data, integration, or other specs needed for task decomposition.
9. Parallelize only independent scopes; duplicate context freely, but never duplicate write ownership or decision authority unless explicitly running review or A/B comparison.
10. Verify the team can move work through requirements, spec, tasks, implementation, checking, release, and documentation.
