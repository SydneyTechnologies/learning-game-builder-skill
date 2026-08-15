# Documentation and Knowledge Base

Organize notes by concepts and tasks, not by game screen alone. A practical structure is:

```text
docs/
  index.md
  learning-path.md
  concepts/
  recipes/
  glossary.md
  troubleshooting.md
  sources.md
```

Each concept note should include: outcome, intuition, formal explanation, annotated example, common mistakes, related challenges, related concepts, and sources. Use relative Markdown links and stable filenames. Include external URLs with descriptive labels and access dates when facts may change.

For Obsidian, use standard Markdown first. Wikilinks are acceptable if the vault prefers them, but do not make core navigation depend on community plugins. Keep YAML frontmatter small and consistent, for example `tags`, `aliases`, `competencies`, and `source_status`.

Classify sources:

- authoritative: official specifications, standards, primary documentation, or peer-reviewed primary work
- supplementary: reputable tutorials, books, courses, or explanatory articles
- project-authored: explanations and examples created for the game

Do not copy substantial copyrighted text. Summarize, link, and quote only short necessary excerpts. Add a link checker and ensure every challenge's documentation target resolves.

