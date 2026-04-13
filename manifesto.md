# The Upstream Problem Nobody Governs

AI agents can write code in seconds.

But they cannot understand vague problems.

---

## The real bottleneck

For decades, software development was constrained by implementation effort.

Discovery was informal. Requirements were gathered in meetings, written in docs, and handed off to engineers. The process was messy, but humans could compensate — they asked questions, read between the lines, and made judgment calls.

AI agents cannot do that.

When an agent receives an ambiguous spec, it does not ask for clarification. It guesses. And guesses compound into failures.

---

## The compound mistake problem

Chip Huyen documented this in *AI Engineering* (2025): if an agent's accuracy is 95% per step, over 10 steps it drops to 60%. Over 100 steps, it drops to 0.6%.

The implication is clear: **the quality of the input determines the quality of the output**. A well-understood problem produces a precise spec. A precise spec produces fewer agent steps. Fewer steps means fewer compound mistakes.

Discovery is not overhead. It is error reduction.

---

## What the industry misses

Every framework for AI-assisted development focuses on execution:

- How should the agent write code?
- How should output be reviewed?
- How should deployment be governed?

Nobody asks the upstream question:

> How well is the problem understood before we ask an AI agent to solve it?

That question determines everything downstream.

---

## The one-size-fits-all failure

Most teams apply the same discovery process to every problem:

- A trivial bug fix gets a 2-hour requirements workshop
- A complex platform migration gets the same 2-hour workshop

Both are wrong.

The bug fix needs no discovery — skip straight to spec.
The migration needs deep, iterative discovery — 4+ sessions with multiple stakeholders.

Without classification, teams either waste time on simple problems or rush through complex ones.

---

## DD6

DD6 classifies the problem across six dimensions:

- **Intent clarity** — how clear is the request?
- **Domain depth** — how much expertise is needed?
- **Stakeholder convergence** — how many perspectives must align?
- **Testability** — can the outcome be verified by an agent?
- **Precedent** — have we done this before?
- **Boundary clarity** — where does the problem start and end?

Together, they answer:

> How much discovery does this problem need before an AI agent can produce a reliable spec?

---

## What changes

With DD6:

- discovery becomes proportional to complexity
- simple problems skip to spec immediately
- complex problems get the exploration they need
- the output quality of agents improves because input quality improves

---

## The companion

DD6 classifies the **problem**.
CIRK classifies the **execution**.

Together, they govern the full lifecycle:

```
Problem → DD6 → Discovery → Spec → CIRK → Execution → Delivery
```

No estimation. No guessing. Classification in, governance out.

---

## Open by design

DD6 is not tied to any vendor, framework, or platform.

It is designed to be:

- simple enough for teams
- structured enough for systems
- open enough to become a standard

---

## Final thought

Story points measure how humans code.
CIRK measures how AI-assisted work should execute.
DD6 measures how much a problem needs to be understood first.

That upstream question is the one nobody was asking.
