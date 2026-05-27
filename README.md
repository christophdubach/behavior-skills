# Behavior Skills

A modular **Behavior Design System** for AI agents.
Skills are pure Markdown. No application code. Optimized for Claude-style skill loading and portable to other agent runtimes.

---

## What a skill is

A Behavior Skill defines **how** an agent thinks, communicates, or operates — not the task domain alone. A skill may define a persona, mode, style, process, domain, or profile.

The system is built around two ideas:
- **Atomic skills** do one thing well.
- **Profiles** compose multiple atomic skills into a repeatable stack.

---

## Repository structure

```text
behavior-skills/
├── .claude-plugin/
│   └── plugin.json
├── .claude/
│   └── commands/
│       └── cdbs/
├── skills/
│   ├── personas/
│   ├── modes/
│   ├── styles/
│   ├── processes/
│   ├── domains/
│   └── profiles/
├── grounding/
├── _templates/
└── project-template/
    ├── CLAUDE.md
    └── .claude/
        └── rules/
```

Each skill lives in its own folder and uses a canonical `SKILL.md` file.

```text
skills/processes/discovery-process/
├── SKILL.md
└── reference/
    └── methodology.md
```

Optional sub-folders:

| Folder | Purpose |
|---|---|
| `reference/` | Definitions, decision rules, field specs |
| `heuristics/` | Evaluation criteria, judgment rules |
| `rules/` | Behavioral constraints, content guidelines |
| `examples/` | Concrete demonstrations |
| `templates/` | Output templates |
|

---

## Skill types

| Type | Question answered | Use when |
|---|---|---|
| `persona` | Who am I? | You need role, stance, or expertise identity |
| `mode` | How do I think? | You need a mental approach or review stance |
| `style` | How do I communicate? | You need tone, brevity, structure, or voice |
| `process` | How do I proceed? | You need steps, workflow, or operating sequence |
| `domain` | What do I know? | You need principles, constraints, or subject expertise |
| `profile` | Which skills together? | You need a reusable bundle of multiple skills |

---

## Classification guide

Use these rules to avoid overlap:

- Put identity and expertise framing in a **persona**.
- Put thinking posture in a **mode**.
- Put wording, structure, or presentation constraints in a **style**.
- Put ordered steps or success criteria in a **process**.
- Put reusable knowledge or evaluation principles in a **domain**.
- Put combinations only in a **profile**; avoid embedding a full stack inside one atomic skill.

If something contains both behavior and knowledge, keep the behavior in the skill and move reusable facts or reference material into `grounding/` or a sub-folder.

---

## Loading order

Use a predictable loading model:

1. Read repository `CLAUDE.md` for the system overview.
2. Read project `CLAUDE.md` for always-on project context.
3. If a profile matches, load the profile first.
4. Load the profile's component skills.
5. Load referenced grounding files.
6. Load sub-folder files on demand, not upfront.

This keeps context lean and reduces duplication.

---

## Profiles

A profile is a composition layer, not a place for duplicate behavior prose. A good profile should:

- list component skills explicitly,
- explain when the bundle is appropriate,
- describe how components should be combined,
- avoid restating the full content of each atomic skill.

---

## Grounding

Shared knowledge lives in `grounding/` and is referenced from skills by relative path. This keeps **knowledge** separate from **behavior** and makes updates easier.

Use `grounding/global.md` only for material that is broadly useful across many skills. Put narrower material in named grounding files closer to the domain they support.

---

## Naming conventions

- Folder names should be lowercase and hyphenated, for example `ux-architect` or `text-to-skills-mapping`.
- Every skill folder contains one canonical `SKILL.md`.
- Profiles should be named as bundles, for example `ux-review` or `frontend-discovery`.
- Atomic skills should not use bundle-like names such as `ux-review-mode-style`.

---

## Creating a new skill

1. Choose the right category under `skills/`.
2. Create `skills/<category>/<skill-name>/`.
3. Copy `_templates/SKILL.template.md` into that folder as `SKILL.md`.
4. Fill in frontmatter and sections.
5. Add only the optional sub-folders the skill actually needs.
6. If the skill is mostly composition, make it a profile instead.

---

## Versioning

- `1.0.0` initial stable definition
- `1.1.x` non-breaking clarifications
- `1.x.0` additive behavior changes
- `2.0.0` breaking structural or behavioral change
