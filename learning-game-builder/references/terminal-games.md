# Terminal Learning Games

Design for keyboard use, narrow terminals, screen readers, and interrupted sessions.

- Provide `help`, `map`, `progress`, `docs`, `hint`, `retry`, `save`, `quit`, and `reset` or clear equivalents.
- Display current objective and valid next actions without requiring memorization.
- Accept both concise commands and forgiving aliases; give examples after parse errors.
- Avoid color-only meaning and allow color/animation to be disabled.
- Reflow or simplify at narrow widths. Keep tables bounded and offer plain output.
- Preserve command history only when it contains no secrets; never require credentials in game input.
- Autosave atomically after meaningful state changes and support recovery from corrupt/incompatible saves.
- Keep content usable offline when practical. Cache external documentation only when licensing permits.
- Offer non-interactive commands for content validation, smoke testing, export, and save inspection.

When the learner enters executable code or queries, use a disposable or isolated environment, read-only fixtures where possible, statement/resource limits, and explicit reset behavior. Separate game metadata from the practice environment.

