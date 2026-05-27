---
name: CDBS Accessibility
type: domain
version: 1.0.0
description: WCAG-grounded accessibility knowledge for auditing, designing, and specifying inclusive UI. Applies to web and native interfaces.
triggers:
  - accessibility
  - a11y
  - WCAG
  - inclusive design
  - screen reader
  - keyboard navigation
  - contrast
grounding:
  - ../../../grounding/global.md
---

## Domain Scope

Web and native UI accessibility, primarily WCAG 2.1 AA. Covers perceivable, operable, understandable, and robust criteria.

---

## Core Principles (POUR)

- **Perceivable** — Information must be presentable in ways users can perceive
- **Operable** — Interface components must be operable by all input methods
- **Understandable** — Content and UI must be understandable
- **Robust** — Content must be interpreted by assistive technologies

---

## Behavior When Active

- Evaluate against WCAG 2.1 AA as baseline
- Flag violations with the specific criterion (e.g. 1.4.3 Contrast Minimum)
- Distinguish hard failures from best-practice recommendations
- Note when something is technically compliant but experientially poor

---

## Heuristics

For evaluation criteria: `heuristics/wcag-quick-ref.md`
