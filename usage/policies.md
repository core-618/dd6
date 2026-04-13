# Discovery Policies

DD6 is useful because it maps classification into discovery behavior.

---

## Discovery modes

### Skip (None)

Typical signals:

- score 6–8
- all dimensions ≤ 2
- I1 and B1

Behavior:

- no discovery session needed
- generate spec directly from intake using a template
- optional human spot-check

---

### Focused (Shallow)

Typical signals:

- score 9–11
- one or two dimensions at 3

Behavior:

- 1-2 focused sessions
- clarify the dominant dimension (e.g., if D3, bring in a domain expert)
- structured Q&A, not open-ended exploration

---

### Structured (Standard)

Typical signals:

- score 12–14
- multiple dimensions at 2-3

Behavior:

- 2-4 sessions with defined phases
- intent → scope → risk progression
- stakeholder alignment if S ≥ 2
- exit criteria per phase

---

### Iterative (Deep)

Typical signals:

- score 15–17
- multiple dimensions at 3

Behavior:

- 4+ sessions, iterative
- hypothesis testing and validation
- architectural exploration
- multi-stakeholder workshops
- AI Bubbles for parallel exploration

---

### Stabilize (Emergency)

Typical signals:

- score 18
- or active incident regardless of score

Behavior:

- human-led stabilization
- no structured discovery during crisis
- triage → stabilize → then classify and discover

---

## Policy rules by dimension signal

| Signal | Suggested behavior |
| ------ | ------------------ |
| I3 | Intent clarification is the first priority |
| D3 | Domain expert must participate in discovery |
| S3 | Multi-stakeholder alignment session required |
| T3 | Define acceptance criteria rigorously before spec |
| P3 | Exploration and prototyping recommended |
| B3 | Scope definition is the first phase of discovery |

---

## Key idea

DD6 is not just descriptive.
It can act as policy-as-code input for discovery orchestration.
