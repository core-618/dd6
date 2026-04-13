# Why One-Size-Fits-All Discovery Fails

## The problem

Most teams apply the same discovery process to every intake.

A trivial bug fix and a complex platform migration both get the same treatment: a meeting, a Jira ticket, and a prompt to the agent.

This creates two failures:

- **Over-discovery**: spending 3 sessions on a problem an agent could solve directly from the intake description
- **Under-discovery**: rushing a vague request to an agent that produces a wrong spec, causing rework downstream

Both waste time. Under-discovery is more expensive because agent execution costs compound with bad specs.

---

## Why it happens

Teams default to uniform process because they lack a classification model.

Without DD6, the only options are:

- gut feeling ("this seems complex")
- seniority-based judgment ("the tech lead says it needs more exploration")
- politics ("the VP wants it fast, skip discovery")

None of these are systematic, auditable, or consistent.

---

## What DD6 does differently

DD6 classifies the problem across six dimensions, producing a score that maps to a discovery depth.

A bug fix scores 7 → skip discovery.
A platform migration scores 16 → deep discovery with 4+ sessions.

The classification is:

- explicit — every dimension is scored and recorded
- proportional — more complex problems get more exploration
- auditable — the scoring reasoning is preserved
- systematic — different people scoring the same problem converge on similar depths
