# Terminal Learning Games

Design for keyboard use, narrow terminals, screen readers, and interrupted sessions.

- Provide `help`, `map`, `progress`, `docs`, `hint`, `retry`, `save`, `quit`, and `reset` or clear equivalents.
- Display current objective and valid next actions without requiring memorization.
- Segment long screens with concise, text-visible headings and horizontal rules or an equivalent boundary. Separate mission information, instruction, feedback, workspace output, and the next action; do not make visual grouping depend on color.
- Accept both concise commands and forgiving aliases; give examples after parse errors.
- Avoid color-only meaning and allow color/animation to be disabled.
- Reflow or simplify at narrow widths. Keep tables bounded and offer plain output.
- Preserve command history only when it contains no secrets; never require credentials in game input.
- Autosave atomically after meaningful state changes and support recovery from corrupt/incompatible saves.
- Version saved state, retain only the minimum learner evidence needed for resume, and test migrations or safe recovery. Do not persist raw learner input unless the product needs it and its privacy implications are explicit.
- Keep content usable offline when practical. Cache external documentation only when licensing permits.
- Offer non-interactive commands for content validation, smoke testing, export, and save inspection.

Offer a `workspace`, `explore`, or clear equivalent when the learner needs to discover a dataset, world, or tool before solving a mission. On entry, show an inventory and simple inspection actions appropriate to the domain—for example list/describe/sample for data, inspect/run for code, or map/examine for a simulation. Make it ungraded, preserve the current mission when leaving, and state the safe action boundary. Reprint the mission or provide an equally clear return point after exit.

When the learner enters executable code or queries, use a disposable or isolated environment, read-only fixtures where possible, statement/resource and result-size limits, and explicit reset behavior. Enforce permissions at the execution engine when available; do not rely solely on a prefix or regex check. Separate game metadata from the practice environment.

For syntax-bearing input, use the latest parser/runtime error and the expected task stages to give a first targeted, non-revealing hint, then continue with the authored hint ladder. Keep command output bounded, label color-coded states in text, and make the current objective and next actions available after every mission display.
