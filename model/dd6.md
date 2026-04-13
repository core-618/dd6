# DD6 Model

DD6 is a problem classification model for AI-assisted software development.

Each intake is represented as:

```text
[I, D, S, T, P, B]
```

Each dimension is scored from **1 to 3**:

- **1 — Low** (less discovery needed)
- **2 — Medium**
- **3 — High** (more discovery needed)

---

## I — Intent clarity

How clear is what the requester actually wants?

| Score | Description |
| ----- | ----------- |
| I1 | Crystal clear, spec-ready — the requester knows exactly what they want |
| I2 | Partially clear — the goal is understood but specifics need refinement |
| I3 | Vague or ambiguous — the requester has an idea but cannot articulate the desired outcome |

---

## D — Domain depth

How much specialist knowledge is needed to understand the problem?

| Score | Description |
| ----- | ----------- |
| D1 | Standard domain — general software engineering knowledge is sufficient |
| D2 | Moderate specialization — requires understanding of specific business rules or technical patterns |
| D3 | Deep expertise — requires specialist knowledge (security, compliance, performance, domain science) |

---

## S — Stakeholder convergence

How many perspectives need to align before the problem is well-defined?

| Score | Description |
| ----- | ----------- |
| S1 | Single stakeholder — one person or team defines the problem |
| S2 | Two to three stakeholders — engineering + product, or engineering + design |
| S3 | Multiple stakeholders — cross-functional alignment required (product, design, engineering, compliance, business) |

---

## T — Testability

Can an AI agent verify that the outcome is correct?

| Score | Description |
| ----- | ----------- |
| T1 | Easily testable — clear metrics, automatable verification, deterministic outcomes |
| T2 | Partially testable — some aspects are measurable but others require judgment |
| T3 | Hard to test — subjective outcomes, UX quality, or requires human evaluation |

---

## P — Precedent

Have we done something similar before in this codebase or team?

| Score | Description |
| ----- | ----------- |
| P1 | Strong precedent — many similar examples exist, established patterns available |
| P2 | Partial precedent — related work exists but this case has new aspects |
| P3 | No precedent — completely new territory, no existing patterns to follow |

---

## B — Boundary clarity

Are the boundaries of the problem clear?

| Score | Description |
| ----- | ----------- |
| B1 | Clear boundaries — well-defined scope, explicit in/out of scope |
| B2 | Partial boundaries — general scope is understood but edges are fuzzy |
| B3 | Unclear boundaries — open-ended problem, scope is part of what needs to be discovered |

---

## Composite score

```text
Score = I + D + S + T + P + B
```

| Score | Classification | Discovery depth |
| ----- | -------------- | --------------- |
| 6–8 | Clear | None — skip to spec |
| 9–11 | Complicated | Shallow — 1-2 focused sessions |
| 12–14 | Complex | Standard — 2-4 structured sessions |
| 15–17 | Deep | Deep — 4+ iterative sessions |
| 18 | Chaotic | Emergency — stabilize first |

---

## Important note

The vector matters more than the total.

Two intakes with the same composite score may require different discovery strategies.

Example:

- `I3 D1 S1 T1 P1 B3` and `I1 D1 S3 T1 P3 B1` both sum to 10
- but the first needs intent clarification and scope definition
- the second needs stakeholder alignment and exploration of unknowns

DD6 should be interpreted as a discovery input, not just a math output.
