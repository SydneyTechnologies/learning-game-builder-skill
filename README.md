# Learning Game Builder Skill

A Codex skill for designing, building, and evaluating rigorous educational games. It supports terminal games, coding tutors, simulations, quiz adventures, curriculum-driven games, and documentation-backed practice environments for any subject.

The skill emphasizes active practice, mastery mapping, useful feedback, safe learner input, accessible terminal UX, connected documentation, and verifiable curriculum coverage.

## Install

### 1. Clone the repository

```bash
git clone git@github.com:SydneyTechnologies/learning-game-builder-skill.git
cd learning-game-builder-skill
```

You can use HTTPS instead if you do not have GitHub SSH access configured:

```bash
git clone https://github.com/SydneyTechnologies/learning-game-builder-skill.git
cd learning-game-builder-skill
```

### 2. Copy the skill into Codex

```bash
mkdir -p ~/.codex/skills
cp -R learning-game-builder ~/.codex/skills/
```

Restart Codex or begin a new session after installation so the skill is discovered.

### 3. Verify the installation

```bash
test -f ~/.codex/skills/learning-game-builder/SKILL.md \
  && echo "learning-game-builder is installed"
```

The installed directory should contain:

```text
~/.codex/skills/learning-game-builder/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── documentation.md
    ├── game-design.md
    ├── learning-design.md
    ├── quality-gates.md
    └── terminal-games.md
```

## Use

Invoke the skill explicitly in Codex:

```text
Use $learning-game-builder to design a terminal game that teaches SQL from beginner to advanced.
```

Other example prompts:

```text
Use $learning-game-builder to turn this Python syllabus into a narrative CLI game.
```

```text
Use $learning-game-builder to review my learning game for curriculum gaps, weak feedback, and inaccessible terminal interactions.
```

Codex may also select the skill automatically when a request clearly involves building or evaluating an educational game.

## Update

From the cloned repository:

```bash
git pull
cp -R learning-game-builder/. ~/.codex/skills/learning-game-builder/
```

Start a new Codex session after updating.

## Uninstall

Remove only this skill's installed directory:

```bash
rm -rf ~/.codex/skills/learning-game-builder
```

The cloned repository is independent of the installed copy and may be retained for later updates.

## Repository structure

The distributable Codex skill lives in [`learning-game-builder/`](learning-game-builder/). Detailed learning design, game design, terminal UX, documentation, and quality guidance is stored under [`learning-game-builder/references/`](learning-game-builder/references/) and loaded as needed.
