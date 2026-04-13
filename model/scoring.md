# Scoring Guidance

DD6 should be scored pragmatically and consistently.

The goal is not theoretical precision.
The goal is proportional discovery — enough exploration to produce a reliable spec, no more.

---

## Scoring flow

For each intake, ask:

1. **Intent** — how clear is what the requester wants?
2. **Domain** — how much specialist knowledge is needed?
3. **Stakeholder** — how many perspectives must converge?
4. **Testability** — can an agent verify the outcome?
5. **Precedent** — have we done something like this before?
6. **Boundary** — are the problem edges defined?

Then assign a value from 1 to 3 for each dimension.

---

## Practical advice

### Score the problem, not the solution

DD6 classifies the problem space, not the implementation. A problem can be complex (DD6 high) but produce a simple implementation (CIRK low). They measure different things.

### When in doubt, score higher

Under-discovery causes more damage than over-discovery. If you are unsure whether Domain is 2 or 3, score 3. The worst case is one extra discovery session. The alternative is a bad spec that wastes an agent's execution.

### Revisit after first discovery session

DD6 scoring improves with information. After the first session, re-score. If the problem turns out simpler than expected, reduce depth. If it turns out more complex, increase it.

### Use precedent honestly

If the team has never built something similar, P is 3 regardless of how simple the concept sounds. Novelty in the codebase means the agent has no patterns to follow.

---

## Example

Intake: update copy on marketing page

```
I1 D1 S1 T1 P1 B1
```

Intake: multi-tenant data isolation

```
I2 D3 S2 T2 P3 B2
```

Both may be described as "medium priority" in a backlog. DD6 reveals they need radically different discovery investment.
