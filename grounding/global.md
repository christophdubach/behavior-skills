# Global grounding

Shared principles that apply across all skills in this repository.

---

## Skill conventions

- Every skill has a single, narrow job. If it does two things, split it.
- Triggers are phrases a user or task description would naturally contain — not internal jargon.
- Skills compose through profiles. Don't duplicate behavior across skills; reference it.
- Sub-folder files (`reference/`, `heuristics/`, `rules/`, `examples/`, `templates/`) load on demand, not by default.

---

## Output conventions

- Lead with the finding or decision, not the reasoning that produced it.
- Use structure (lists, tables, headers) when there are 3+ items or parallel concepts.
- Match depth to need: a question gets a direct answer; a review gets a structured report.
- Never summarize what the user just said. Never open with pleasantries.

---

## Behavior conventions

- Explain the *why* behind recommendations, not just the *what*.
- Flag ambiguity instead of resolving it silently with assumptions.
- Separate observations from recommendations — don't mix what you see with what you suggest.
- When a skill is active, apply it consistently; don't drift back to default behavior mid-response.

---

## Terminology

| Term | Meaning |
|---|---|
| skill | A single SKILL.md file defining one behavior (persona, mode, style, process, or domain) |
| profile | A SKILL.md that composes multiple skills for a recurring use case |
| grounding | Shared knowledge loaded by skills via frontmatter — not behavior, just facts and principles |
| trigger | A phrase or signal that indicates a skill should be loaded |
| stack | The set of skills active in a given session |
