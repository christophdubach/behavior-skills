# Behavior Skills — Claude Instructions

This repository is a **Behavior Design System**: a library of reusable skills that shape how you think, communicate, and operate.

---

## How to use skills

Load a skill when its triggers match the task. Skills live at `skills/<type>/<name>/SKILL.md`.

If a **profile** matches, load the profile first. It tells you which component skills to load and how to combine them.

Prefer atomic skills for precise behavior. Prefer profiles for recurring combinations.

---

## Loading order

1. Repository `CLAUDE.md`
2. Project `CLAUDE.md`
3. Matching profile, if any
4. Component skills
5. Referenced grounding files
6. Optional `reference/`, `heuristics/`, `rules/`, `examples/`, `templates/` files only when needed

---

## Skill index

### Personas — “Who am I?”
| Skill | Triggers |
|---|---|
| `personas/ux-architect` | UX review, information architecture, user flows, system design |
| `personas/frontend-expert` | Frontend architecture, component design, performance, code review |

### Modes — “How do I think?”
| Skill | Triggers |
|---|---|
| `modes/explore-mode` | Open-ended discovery, understanding a problem space |
| `modes/review-mode` | Evaluating existing work, critique, audit, structured review |

### Styles — “How do I communicate?”
| Skill | Triggers |
|---|---|
| `styles/concise-style` | Structured, brief output requested |
| `styles/christoph-style` | Write like Christoph; personal voice; use examples when available |
| `styles/visual-style` | Diagrams, tables, spatial structure, comparison-heavy output |

### Processes — “How do I proceed?”
| Skill | Triggers |
|---|---|
| `processes/debugging-process` | Debugging, fixing bugs, diagnosing issues, root cause analysis |
| `processes/discovery-process` | Kicking off a project, scoping requirements, first-session work |
| `processes/text-to-skills-mapping` | `/map-skills`, decomposing text into skills, extracting skill definitions from any input |

### Domains — “What do I know?”
| Skill | Triggers |
|---|---|
| `domains/accessibility` | Accessibility audit, WCAG, inclusive design |
| `domains/ui-patterns` | UI component patterns, design system conventions |

### Profiles — Skill stacks
| Profile | Activates |
|---|---|
| `profiles/ux-review` | `personas/ux-architect` + `modes/review-mode` + `domains/accessibility` |
| `profiles/frontend-discovery` | `personas/frontend-expert` + `modes/explore-mode` + `styles/visual-style` + `processes/discovery-process` + `domains/ui-patterns` |

---

## Classification rules

| Category | Look for | Rewrite as |
|---|---|---|
| Persona | role, identity, expertise | “I am … I bring …” |
| Mode | thinking stance, evaluation posture, review posture | “When … I approach …” |
| Style | tone, formatting, expression, output shape | “I communicate … I avoid …” |
| Process | ordered method, sequence, success criteria | “1. … 2. … Success = …” |
| Domain | knowledge, reusable principles, constraints | “In this domain … Apply when …” |
| Profile | recurring stack of skills, composition only | “Use A + B + C together when …” |

When unsure, keep skills atomic and compose with a profile later.

## Heuristics

- If it sounds like identity, it is usually a persona.
- If it sounds like review posture, it is usually a mode.
- If it sounds like wording or presentation, it is usually a style.
- If it sounds sequential, it is usually a process.
- If it sounds reusable and factual, it is usually a domain or grounding.
- If it combines several of the above, it is probably a profile.

---

## Grounding and sub-files

Shared knowledge is in `grounding/`. Skills may reference it in frontmatter.

Load sub-folder files on demand:

| Folder | Load when |
|---|---|
| `reference/` | You need definitions, specs, or decision rules |
| `heuristics/` | You are evaluating or auditing something |
| `rules/` | You are producing output and need behavioral constraints |
| `examples/` | You need to match or demonstrate a pattern |
| `templates/` | You are generating structured output |
