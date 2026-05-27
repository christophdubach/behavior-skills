# Text-to-Skills Mapping — Agent Quick Reference

Condensed version of `SKILL.md` for use during execution. Load when actively running the process.

---

## Task

Given text describing behavior, methodology, or principles: decompose it into skill definitions and propose profile bundles.

## Steps

1. Analyze → identify elements by type
2. Categorize → assign to skill type
3. Reformulate → rewrite in the appropriate voice
4. Map dependencies → note overlaps and conflicts
5. Propose profiles → bundle complementary skills
6. Output → structured skill definitions ready for integration

## Categorization Table

| Category | Identifies | Rewrite As |
|---|---|---|
| **Persona** | Identity, role, expertise | "I am [role]. I bring [expertise]." |
| **Mode** | Thinking patterns, mental models | "When [situation], I [approach]." |
| **Style** | Tone, voice, vocabulary | "I communicate [adjectives]. I avoid [anti-patterns]." |
| **Process** | Steps, workflows, methods | "1. [Step]. 2. [Step]. Success = [criteria]." |
| **Domain** | Knowledge, principles, constraints | "In [domain], [principle]. Apply when [context]." |

## Reformulation Hints

- Look for implicit behavior: "I prioritize X" → Mode; "I communicate Y" → Style
- Combine related principles → one Domain skill
- Generalize where possible; avoid one-off combinations
- Could an agent using these skills produce the intended behavior? If not, revise.

## Example

**Input:** "I'm a frontend developer focused on performant, accessible interfaces. I think in components. I explore multiple implementations before settling. I explain with code examples."

| Element | Category |
|---|---|
| "frontend developer" | Persona |
| "think in components" | Mode |
| "explore implementations" | Mode |
| "explain with code" | Style |
| "performant, accessible" | Domain (×2) |
