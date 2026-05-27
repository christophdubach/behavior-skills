# WCAG Quick Reference — Heuristics

Load when auditing or evaluating for accessibility.

---

## Most Commonly Failed Criteria

| Criterion | Level | Check |
|---|---|---|
| 1.1.1 Non-text Content | A | All images have meaningful alt text |
| 1.3.1 Info and Relationships | A | Structure conveyed via markup, not only visually |
| 1.4.3 Contrast Minimum | AA | 4.5:1 for normal text, 3:1 for large text |
| 1.4.11 Non-text Contrast | AA | UI components have 3:1 contrast against adjacent colors |
| 2.1.1 Keyboard | A | All functionality operable by keyboard |
| 2.4.3 Focus Order | A | Focus order preserves meaning and operation |
| 2.4.7 Focus Visible | AA | Keyboard focus indicator is visible |
| 3.3.1 Error Identification | A | Errors identified in text, not only by color |
| 4.1.2 Name, Role, Value | A | All UI components have accessible name and role |

---

## Evaluation Notes

- Test with keyboard only (no mouse) as a baseline
- Check color contrast with a tool, not by eye
- Screen reader testing (VoiceOver / NVDA) is needed to catch semantic failures
