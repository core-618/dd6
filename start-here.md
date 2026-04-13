# DD6 in 60 seconds

DD6 replaces one-size-fits-all discovery with proportional exploration.

AI writes code. DD6 defines how much the problem needs to be understood first.

---

## Step 1 — Pick an intake

Example:

```
Add multi-tenant isolation to the API
```

---

## Step 2 — Score it

```
I2 D3 S2 T2 P1 B1
```

Meaning:

- **I2**: intent is partially clear but needs refinement
- **D3**: deep domain knowledge required (security, data isolation)
- **S2**: engineering + product need to align
- **T2**: testable but complex verification
- **P1**: no precedent in this codebase
- **B1**: boundaries are unclear — where does isolation start and end?

---

## Step 3 — Apply discovery depth

Sum the vector and apply the depth:

- **6–8** → none (skip discovery, template-based spec)
- **9–11** → shallow (1-2 focused sessions)
- **12–14** → standard (2-4 sessions, structured phases)
- **15–17** → deep (4+ iterative sessions)
- **18** → emergency (stabilize first, discover after)

For the example above: I2 + D3 + S2 + T2 + P1 + B1 = **11** → shallow discovery.

---

## Step 4 — Use DD6 consistently

Once every intake gets a DD6 score, teams gain a shared language for:

- discovery proportionality
- when to skip vs when to explore
- what questions must be answered
- when the problem is understood enough for an agent to work on it

---

## Rule of thumb

- **High I** → more intent clarification needed
- **High D** → bring in domain experts
- **High S** → schedule stakeholder alignment sessions
- **High T** → define acceptance criteria rigorously
- **Low P** → more exploration, less assumption
- **Low B** → scope definition is the first priority

---

## What DD6 is not

DD6 is not:

- an effort estimate
- a risk assessment (that is CIRK)
- a sprint planning tool
- a replacement for discovery — it governs how much discovery to do

DD6 is a problem classification standard for AI-native development.
