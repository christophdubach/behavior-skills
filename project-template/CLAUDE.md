# [Project Name] — Claude Instructions

## Project context

Describe what this project is, who it serves, and any important context that should always stay active.

## Always-on rules

Project-specific rules live in `.claude/rules/`.

- `language-conventions.md` — Swiss German, French/Italian, and American English orthography and style rules
- `ux-context.md` — UX goals, target users, product principles
- `accessibility.md` — accessibility requirements and compliance level
- `terminology.md` — project-specific vocabulary and naming conventions
- `constraints.md` — hard technical, time, or organizational constraints

These rules are always active and should not be overridden without explicit confirmation.

## Skill loading

Use this order:

1. Read this file.
2. Apply the rules in `.claude/rules/`.
3. Load the most relevant profile if one matches.
4. Otherwise load the minimum set of atomic skills needed.

## Recommended skills

- Load `ux-architect` for flows, components, IA, and UX structure.
- Load `ux-review` when asked to critique a design or specification.
- Load `frontend-discovery` when exploring implementation options for frontend UI work.
