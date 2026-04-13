# DD6 + CIRK: Companion Standards

DD6 and CIRK are designed as companion models — not competing, not overlapping.

---

## Different questions, different stages

| | DD6 | CIRK |
| - | --- | ---- |
| Question | How much discovery does this problem need? | How safely can this task be executed? |
| Stage | Upstream (intake → spec) | Downstream (spec → delivery) |
| Input | Raw intake | Defined spec |
| Output | Discovery depth | Execution policy |
| Dimensions | 6 (I, D, S, T, P, B) | 4 (C, I, R, K) |
| Score range | 6–18 | 4–12 |

---

## The pipeline

```text
Intake → DD6 → Discovery sessions → Spec → CIRK → Execution → Delivery
         ↑                                   ↑
    "How complex is        "How risky is
     the problem?"          the execution?"
```

---

## Feed-forward relationship

DD6 output improves CIRK accuracy:

- A problem classified as Deep (DD6 15+) that goes through full discovery produces specs with well-defined context, reducing CIRK's C dimension uncertainty
- Discovery sessions surface dependencies and risks early, making CIRK's K dimension more accurate
- Testability assessment in DD6 (T dimension) directly informs CIRK's R dimension — if the problem outcome is hard to test, human review will be more intensive

---

## One framework, two models

DD6 and CIRK together form a unified classification framework for AI-native development:

```text
┌────────────────────────────────────────────┐
│  Problem → Discovery → Spec → Execution    │
│                                             │
│  DD6 [I,D,S,T,P,B]    CIRK [C,I,R,K]      │
│  score 6-18            score 4-12           │
│  Problem upstream      Execution downstream │
└────────────────────────────────────────────┘
```

Neither model is complete without the other. DD6 without CIRK leaves execution ungoverned. CIRK without DD6 assumes the problem is already understood — which is often the most dangerous assumption in AI-assisted development.

---

## Adoption

Teams can adopt either model independently. But the full value emerges when both are used together:

1. Intake arrives
2. DD6 classifies the problem → determines discovery depth
3. Discovery sessions produce a well-defined spec
4. CIRK classifies the execution → determines governance policy
5. Agent executes under the classified policy

This creates end-to-end governance from problem to delivery.
