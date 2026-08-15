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

## Make progression, hints, and presentation legible

For games with levels or rounds:

- Show the learner the total number of core levels, their current position, and the competency taught by each level.
- Provide an accessible map or curriculum overview from the beginning. Locked content may hide challenge details, but must not hide the overall learning destination.
- Distinguish required progression from optional bonus rounds.
- Include bonus rounds when the subject supports meaningful advanced transfer. Bonus rounds should have clearly labeled high difficulty, combine previously learned competencies, permit multiple valid strategies where appropriate, and not block completion of the core path.
- Use color to clarify structure, state, feedback, and syntax when the interface supports it. Never make color the only carrier of meaning, detect or respect non-color environments, and provide a way to disable color.
- Divide long terminal screens into plainly labeled, text-visible regions such as mission brief, learning card, workspace, feedback, and next action. Use restrained horizontal rules or equivalent structural boundaries that remain clear without color or a wide terminal.
- Give learners an ungraded exploration workspace before and during assessment whenever the subject has an inspectable world, dataset, code environment, model, or simulation. Start it with an inventory of what exists and concise ways to inspect its parts, then let learners test safe ideas without needing to satisfy the current challenge.
- Keep exploration and assessment separate: use the same realistic fixture or simulation where useful, retain the current mission on return, award no completion or mastery evidence in the workspace, and make its safe execution boundaries explicit.
- For code or query input, make hints syntax-aware whenever practical. Use the learner's attempt, parser or runtime error, objective, and expected concepts to identify the relevant clause, token, or structural gap.
- Syntax hints should explain the usable form of the construct and provide a partial pattern with placeholders, such as `SELECT <columns> FROM <table> WHERE <condition>;`. Do not immediately reveal the completed answer.
- Escalate hints from locating the problem, to naming the construct, to showing a reusable syntax pattern, to an analogous example, and finally to an explained reveal with reduced mastery credit.

## Audit curriculum depth and teaching visibility

Do not equate a mission count with curricular depth. A short trail can be a useful vertical slice, but it is not evidence that a learner can perform the advertised end capability across its full scope.

- State the course boundary precisely: for example, “read-only SQL querying” rather than “learn SQL” when data changes, schema design, transactions, performance, or other major capabilities are out of scope.
- Organize a nontrivial course into named units that introduce, practice, retrieve, and integrate skills; expose those units and the total core/bonus count in the map from the beginning.
- Introduce a concept before requiring it. For terminal missions, display a concise teaching card containing the goal, why the construct matters, a reusable syntax pattern, an analogous worked example, and a common misconception.
- Revisit important skills in changed contexts later in the trail. Add retrieval and integration missions before and after introducing new syntax so progress represents durable performance instead of one-pass completion.
- Validate every explicitly requested result property. If a challenge asks for a column alias, grouping, a filtered relationship, or row order, its assessment must check that property rather than merely accepting a similar-looking set of values.
- Keep the course playable in sessions: provide a visible resume point, unit-scale progress, optional high-difficulty transfer missions, and a truthful indication of what remains outside the course.

For an expanded curriculum, add a coverage matrix that maps each competency to initial instruction, guided practice, independent or retrieval practice, transfer, feedback, assessment, and documentation. Treat missing later retrieval for essential skills as a curriculum gap.

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

## Make authored challenges executable and inspectable

Give each challenge a compact, reviewable contract: stable ID, competency, objective, prerequisite or sequence position, lesson card, reusable pattern, analogous example, misconception, hint ladder, documentation target, canonical execution, expected outcome, and completion explanation. Keep required and optional challenge boundaries as explicit content configuration rather than scattered UI assumptions.

Use a canonical solution to execute and verify the fixture, not as the only accepted learner input. Define result contracts deliberately: check headers, aliases, values, grouping, and ordering only when the objective requires them; normalize rows when order is irrelevant. Include at least one test for a legitimate alternative strategy whenever the domain permits it.

Provide non-interactive commands or equivalent automation for content validation and a full smoke path. Validate duplicate IDs, required fields, prerequisite reachability, core/bonus boundaries, documentation targets, canonical executions, and saved-state compatibility. Test the validator itself against representative broken data where practical.

## Implement evidence-based feedback

Validate outcomes, not one exact input, when multiple solutions are legitimate. Distinguish syntax or input errors, conceptual mistakes, incomplete solutions, and valid alternative strategies. Never reveal the complete answer before the learner has a meaningful attempt unless explicitly requested.

Use feedback in this order when appropriate:

1. Identify what succeeded.
2. Locate the mismatch without ridicule.
3. Give the smallest useful hint.
4. Offer a deeper explanation or relevant reference.
5. Allow retry, alternate practice, or an explicit reveal with reduced mastery credit.

For executable learner input, isolate execution, impose resource limits and result-size bounds, make sample data recoverable, and never interpolate untrusted input into host shell commands. Prefer a disposable fixture, explicit read-only policy, and engine-level authorization over string filtering alone.

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
