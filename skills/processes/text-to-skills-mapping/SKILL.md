---
name: CDBS Text-to-Skills Mapping Process
type: process
version: 1.0.0
description: Decomposes arbitrary text (requirements, guidelines, principles) into behavior-skills repository components — personas, modes, styles, processes, domains, and profiles.
triggers:
  - '/map-skills'
  - decompose this into skills
  - extract skills from
  - map this text to skills
  - turn this into a skill
  - analyze for skill types
  - build a skill from
grounding:
  - ../../../grounding/global.md
---

## Purpose

Take any unstructured text describing behavior, methodology, or principles and map it to the behavior-skills structure. Output is a set of skill definitions ready for repository integration.

---

## Steps

1. **Analyze** — Read the text. Identify elements by type: identity/role, thinking approach, communication style, workflow steps, domain knowledge, constraints.
2. **Categorize** — Assign each element to a skill type (see table below).
3. **Reformulate** — Rewrite each element in the voice and structure appropriate for its skill type.
4. **Map dependencies** — Note which skills reinforce or assume each other.
5. **Propose profiles** — Bundle related skills into coherent profiles with a clear use case.
6. **Output** — Produce structured skill definitions + proposed profiles.

---

## Skill Type Mapping

| Element in text | Skill type | Voice |
|---|---|---|
| Identity, role, expertise, perspective | **persona** | "I am [role]. I bring [expertise]." |
| Thinking patterns, mental models, approach | **mode** | "When [situation], I [approach]." |
| Tone, communication style, vocabulary | **style** | "I communicate [adjectives]. I avoid [anti-patterns]." |
| Steps, workflows, procedures | **process** | "1. [Step]. 2. [Step]. Success = [criteria]." |
| Specialized knowledge, principles, constraints | **domain** | "In [domain], [principle]. Apply when [context]." |

---

## Output Format

```
## Input Summary
[1–2 sentences on what the text describes]

## Skill Decomposition
### Personas — [Name]: [one-line summary]
### Modes — [Name]: [one-line summary]
### Styles — [Name]: [one-line summary]
### Processes — [Name]: [one-line summary]
### Domains — [Name]: [one-line summary]

## Skill Definitions
[Full SKILL.md with var03 frontmatter for each identified skill]

## Proposed Profiles
[Profile name, stack, rationale, use case]

## Integration Notes
- Ready for immediate use: [list]
- Needs expansion: [list]
```

---

## Success Criteria

- Every significant behavioral element in the input is captured in a skill
- Each skill is reformulated to match repository conventions
- No important nuance is lost in decomposition
- Proposed profiles create coherent, activatable behavior bundles

---

## Reference

Condensed agent quick-reference: `reference/agent-instruction.md`
