# DD6

> Stop guessing discovery depth. Start classifying problems.

DD6 replaces one-size-fits-all discovery with a model that defines how much exploration a problem needs before AI agents can execute it.

## Example

**Intake:** redesign the onboarding flow

I: 2 | D: 2 | S: 3 | T: 1 | P: 1 | B: 1

→ requires deep discovery with multiple stakeholders

## Quick start

1. Pick an intake
2. Score it: `I(1-3) D(1-3) S(1-3) T(1-3) P(1-3) B(1-3)`
3. Apply the depth:
   - **6–8** → skip discovery
   - **9–11** → shallow (1-2 sessions)
   - **12–14** → standard (2-4 sessions)
   - **15–17** → deep (4+ sessions)
   - **18** → emergency (stabilize first)

DD6 is an open standard for classifying how much discovery a problem needs in AI-assisted software development.

It does **not** estimate effort or risk.
It defines discovery conditions for AI-native delivery.

---

## What DD6 addresses

In AI-assisted development, discovery is the bottleneck — not coding.

A vague business request, a cross-system migration, and a simple bug fix all arrive through the same intake channel. But they require fundamentally different levels of exploration before an AI agent can produce a good spec.

Without structured classification, teams either:

- over-engineer simple problems — running full discovery on tasks that could skip straight to execution
- under-explore complex problems — rushing to spec without understanding the problem space

DD6 models the discovery reality.

---

## The model

Each intake is represented as:

```text
[I, D, S, T, P, B]
```

- **I — Intent clarity**: How clear is what the requester wants?
- **D — Domain depth**: How much specialist knowledge is needed?
- **S — Stakeholder convergence**: How many perspectives must align?
- **T — Testability**: Can an agent verify the outcome?
- **P — Precedent**: Have we done something similar before?
- **B — Boundary clarity**: Are the problem boundaries defined?

Each dimension is scored from **1 to 3**:

- **1 — Low complexity** (favors less discovery)
- **2 — Medium**
- **3 — High complexity** (favors more discovery)

---

## In one sentence

DD6 answers this question:

> How much does this problem need to be understood before an AI agent can work on it?

---

## Why it matters

DD6 turns discovery into a governed, proportional process.

It helps teams decide:

- when discovery can be skipped entirely
- when a quick focused session is enough
- when deep multi-stakeholder exploration is needed
- when the problem is too chaotic for structured discovery

---

## Companion standard

DD6 classifies the **problem** (upstream).
[CIRK](https://github.com/core-618/cirk) classifies the **execution** (downstream).

Together, they provide end-to-end classification from problem understanding to execution governance.

```text
Intake → DD6 → Discovery → Spec → CIRK → Execution
```

DD6 output feeds CIRK input. Discovery sessions generate the context that makes CIRK scoring more accurate.

---

## Start here

1. Read [start-here.md](./start-here.md)
2. Review the full model in [model/dd6.md](./model/dd6.md)
3. See copy-paste patterns in [usage/quick-examples.md](./usage/quick-examples.md)
4. Map scores to discovery depth in [usage/policies.md](./usage/policies.md)
5. Understand the CIRK relationship in [model/cirk-companion.md](./model/cirk-companion.md)

---

## Example

```text
Intake: Fix Safari WebSocket disconnect
I1 D1 S1 T3 P3 B3
```

Implication:

- clear intent, known domain, one stakeholder
- highly testable, strong precedent, clear boundaries
- score: 10 → shallow discovery (quick-fix template)

---

## Design principles

DD6 is designed to be:

- **open** — not tied to any vendor or platform
- **simple** — usable by humans and systems
- **proportional** — discovery effort matches problem complexity
- **composable** — works with CIRK as a unified framework

---

## Adoption

DD6 is a proposed standard, not a product.

It can be adopted in:

- intake triage workflows
- discovery session planning
- agent pipeline configuration
- spec quality gates
- governance layers such as Orbit618

No specific implementation is required.

---

## Theoretical foundations

DD6 draws from established frameworks, adapted for AI-assisted development:

- Cynefin Framework (Snowden, 1999) — complexity domain classification
- VUCA (US Army War College, 1987) — uncertainty dimensions (inspiration, not reuse)
- Continuous Discovery Habits (Teresa Torres, 2021) — structured discovery cadence
- ISO/IEC/IEEE 29148:2018 — requirements engineering quality
- AI Engineering (Chip Huyen, 2025) — compound mistakes, planning granularity
- OWASP Agentic AI Top 10 (2025) — agent risk taxonomy
- Singapore Model Agentic AI Framework (IMDA, 2026) — risk bounding upfront

Full references: [model/references.md](./model/references.md)

---

## Development note

This project is developed with AI-assisted workflows.
AI tools support drafting, exploration, and implementation, while project direction, architecture, and review remain human-led.

---

## Contact

[hello@core618.com](mailto:hello@core618.com)

---

## License

MIT
