---
name: learning-game-builder
description: Design, build, and evaluate rigorous learning games that teach a subject through active practice, feedback, progression, and mastery. Use when Codex must create or improve an educational game, terminal/CLI learning game, coding tutor, simulation, quiz adventure, curriculum-driven game, or documentation-backed practice environment for any subject; also use when converting a syllabus, competency map, or reference material into playable lessons and assessments.
---

# Learning Game Builder

Create a learning system that happens to be a compelling game. Preserve instructional depth: do not reduce a broad domain to trivia, syntax recall, or a linear collection of quizzes.

## Start with the design brief

Infer safe defaults from the request and existing workspace. Ask only questions whose answers materially affect the product. Establish:

- learner profile, prerequisites, and desired end capability
- subject boundaries and authoritative reference sources
- interface and runtime constraints, including accessibility and offline needs
- intended session length, total depth, tone, and replay expectations
- assessment expectations, persistence, hints, and failure model
- documentation destination and whether external links may be used

If these choices remain open, create a clearly labeled proposed brief before implementation.

## Build the mastery map

Read [references/learning-design.md](references/learning-design.md). Decompose the domain into observable competencies, prerequisites, misconceptions, and transfer tasks. Give every competency:

- a stable identifier and plain-language outcome
- prerequisite links
- an explanation or reference target
- guided practice and independent practice
- assessment criteria and evidence of mastery
- at least one later retrieval or integration opportunity

Maintain traceability from competency to lesson, challenge, feedback, assessment, and documentation. Use the map to detect gaps and avoid teaching only what is easy to gamify.

## Design the game loop

Read [references/game-design.md](references/game-design.md). Define a short repeatable loop of goal, action, system response, feedback, reflection, and next choice. Make game actions exercise the target skill directly whenever possible.

Use progression to unlock complexity, not merely larger scores. Provide productive failure, graduated hints, explanations tied to the learner's action, and opportunities to retry. Keep rewards subordinate to learning.

For command-line games, also read [references/terminal-games.md](references/terminal-games.md).

## Plan content and data separately

Represent curriculum content in inspectable data where practical. Separate:

- game engine and interface
- lesson/challenge definitions
- validation and scoring logic
- learner state and migrations
- documentation/reference metadata
- analytics or local learning history

Select the smallest dependable stack that supports the brief. Prefer local-first, deterministic behavior unless live services add essential learning value. Avoid collecting sensitive learner data.

Produce an implementation plan with a playable vertical slice early: one complete competency including instruction, play, feedback, assessment, persistence, and documentation.

## Implement evidence-based feedback

Validate outcomes, not one exact input, when multiple solutions are legitimate. Distinguish syntax or input errors, conceptual mistakes, incomplete solutions, and valid alternative strategies. Never reveal the complete answer before the learner has a meaningful attempt unless explicitly requested.

Use feedback in this order when appropriate:

1. Identify what succeeded.
2. Locate the mismatch without ridicule.
3. Give the smallest useful hint.
4. Offer a deeper explanation or relevant reference.
5. Allow retry, alternate practice, or an explicit reveal with reduced mastery credit.

For executable learner input, isolate execution, impose resource limits, make sample data recoverable, and never interpolate untrusted input into host shell commands.

## Create a connected knowledge base

Read [references/documentation.md](references/documentation.md). Create learner-facing explanations, examples, glossaries, troubleshooting notes, and source links alongside the game. If Obsidian is requested, use portable Markdown, relative links, and useful frontmatter/tags without requiring proprietary plugins.

Link game challenges to stable documentation anchors or note identifiers. Distinguish authoritative sources, supplementary explanations, and project-authored guidance. Verify time-sensitive or uncertain sources before presenting them as authoritative.

## Verify before declaring completion

Read [references/quality-gates.md](references/quality-gates.md). Run relevant automated checks and manually play the vertical slice plus representative beginner, advanced, failure, hint, resume, and completion paths. Verify curriculum coverage and links in addition to code correctness.

Report:

- what is playable and how to start it
- tested environments and checks run
- mastery-map coverage and intentional exclusions
- save-data and learner-input safety boundaries
- documentation location and source status
- remaining risks or next recommended slice

