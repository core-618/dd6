# ADR-0001 — DD6 as an AI-Native Discovery Standard

## Status

Active

---

## Context

AI changed software development.

Implementation effort is no longer the primary bottleneck. The harder upstream problem is understanding whether the problem itself is well-defined enough for an AI agent to produce a reliable spec.

Existing approaches apply uniform discovery to all problems, leading to over-exploration of simple problems and under-exploration of complex ones. No standard exists for classifying problem complexity in AI-assisted development.

---

## Decision

Adopt DD6 as a standard model for classifying problem complexity across six dimensions:

- Intent clarity
- Domain depth
- Stakeholder convergence
- Testability
- Precedent
- Boundary clarity

Use the DD6 vector as input for discovery depth, session planning, template selection, and guardrail activation.

---

## Rationale

DD6 was chosen because it:

- models problem complexity rather than effort or risk
- produces actionable discovery depth recommendations
- is simple enough for teams and systems
- is implementation-agnostic and standard-friendly
- complements CIRK (execution risk) as an upstream companion
- creates original dimensions specific to AI-assisted software discovery, avoiding VUCA's documented limitations (dimension overlap, lack of specificity)

---

## Theoretical foundations

- Cynefin Framework (Snowden, 1999) — complexity domain classification
- VUCA (US Army War College, 1987) — uncertainty dimensions (inspiration, not reuse)
- Continuous Discovery Habits (Torres, 2021) — structured discovery cadence
- AI Engineering (Huyen, 2025) — compound mistakes and planning granularity
- OWASP Agentic AI Top 10 (2025) — agent risk taxonomy
- ISO/IEC/IEEE 29148:2018 — requirements engineering quality
- Singapore Model Agentic AI Framework (IMDA, 2026) — risk bounding upfront

---

## Consequences

Adopting DD6 implies that teams can:

- classify problems before investing in discovery
- make discovery depth proportional to problem complexity
- skip discovery for well-understood problems
- invest deeply in complex problems that need it
- improve spec quality, which improves downstream execution

It also implies a shift toward discovery governance as a first-class concern in AI-native development.

---

## Notes

DD6 is intended to remain open and not be tied to a single implementation or vendor.

DD6 is the upstream companion to CIRK. Together they form a unified classification framework for AI-native software delivery.
