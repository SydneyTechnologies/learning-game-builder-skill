# Quality Gates

## Product and learning

- The target learner and end capability are explicit.
- Every required competency maps to instruction, practice, assessment, and documentation.
- Important skills receive transfer and delayed retrieval.
- The core game action practices the real skill.
- Hints escalate and feedback distinguishes common error types.
- Learners can inspect progress, revisit content, and recover from failure.
- Terminal displays have text-visible structural boundaries that remain meaningful without color.
- When assessment depends on an unfamiliar environment, learners can inspect its essential objects, attributes, and relationships and try safe ideas without affecting mastery evidence.

## Engineering and safety

- The project installs and starts from documented commands.
- Unit, integration, content-schema, and smoke checks pass where applicable.
- Save/resume, migration, reset, and corrupt-save recovery are tested.
- Learner-supplied executable input is isolated and resource-limited.
- Fixtures reset reliably and secrets do not enter content, logs, or saves.
- Terminal output works without color and at a narrow width.

## Content and documentation

- Challenge IDs and prerequisite links are valid and content is reachable.
- Every challenge has the required instructional card, hint ladder, explanation, documentation target, and executed canonical solution.
- Accepted solutions test the required output contract—labels, values, grouping, and order where requested—and legitimate alternatives.
- Examples and expected results have been executed or otherwise verified.
- Core/bonus counts and labels are derived from or checked against declared curriculum boundaries.
- Internal links resolve; external links are current at verification time.
- Source authority and project-authored claims are distinguishable.
- Accessibility and offline limitations are documented.

Run a fast content validator and a complete non-interactive smoke path when the game is data-driven. Include tests for an alternative valid solution, a wrong-but-runnable attempt, hint/reveal gating, save/resume and corrupt-save recovery, executable-input restrictions, and color-disabled output where relevant. For a workspace, test inventory and inspection actions, its safe execution limits, and returning to the unchanged active mission.

Use a coverage report or matrix for nontrivial curricula. Treat uncovered competencies and untested paths as explicit release risks, not invisible backlog.
