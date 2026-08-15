# Quality Gates

## Product and learning

- The target learner and end capability are explicit.
- Every required competency maps to instruction, practice, assessment, and documentation.
- Important skills receive transfer and delayed retrieval.
- The core game action practices the real skill.
- Hints escalate and feedback distinguishes common error types.
- Learners can inspect progress, revisit content, and recover from failure.

## Engineering and safety

- The project installs and starts from documented commands.
- Unit, integration, content-schema, and smoke checks pass where applicable.
- Save/resume, migration, reset, and corrupt-save recovery are tested.
- Learner-supplied executable input is isolated and resource-limited.
- Fixtures reset reliably and secrets do not enter content, logs, or saves.
- Terminal output works without color and at a narrow width.

## Content and documentation

- Challenge IDs and prerequisite links are valid and content is reachable.
- Accepted solutions test outcomes and legitimate alternatives.
- Examples and expected results have been executed or otherwise verified.
- Internal links resolve; external links are current at verification time.
- Source authority and project-authored claims are distinguishable.
- Accessibility and offline limitations are documented.

Use a coverage report or matrix for nontrivial curricula. Treat uncovered competencies and untested paths as explicit release risks, not invisible backlog.
