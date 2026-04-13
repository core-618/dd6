# FAQ

## Is DD6 a replacement for discovery sessions?

No. DD6 governs how much discovery to do. It does not replace the sessions themselves.

---

## Does DD6 estimate time?

Not directly. DD6 maps to discovery depth (number of sessions), which has time implications. But duration is derived from depth, not scored directly.

---

## Can DD6 be used without CIRK?

Yes. DD6 is a standalone standard for problem classification. However, the full value emerges when DD6 (upstream) feeds into CIRK (downstream) as a unified framework.

---

## Is DD6 tied to Orbit618?

No. Orbit618 is one possible implementation environment for DD6, but DD6 is designed as a standalone open standard.

---

## Is DD6 a product?

No. DD6 is a standard and a shared classification language. Products and platforms may implement it, but the model itself is implementation-agnostic.

---

## Why six dimensions instead of four (like CIRK)?

CIRK has four dimensions because execution risk can be captured in four independent axes. Problem complexity requires more axes because the problem space has more independent variables: intent, domain, stakeholders, testability, precedent, and boundaries each vary independently and affect discovery depth differently.

---

## Why not use Cynefin directly?

Cynefin classifies problems into domains (Clear, Complicated, Complex, Chaotic) but does not provide a scoring model or dimensions specific to software. DD6 uses Cynefin's domains as depth labels but adds the six-dimensional scoring that makes classification systematic and auditable.

---

## Can I score DD6 with AI?

Yes. DD6 supports heuristic scoring (rules-based) and AI-assisted scoring (a model evaluates the intake and assigns scores). AI-assisted scoring is especially useful for high-volume intake triage.

---

## What is the most important dimension?

It depends on your context. For teams with many stakeholders, S is often the strongest signal. For teams with novel domains, D and P dominate. For vague requirements, I and B matter most.

---

## How does DD6 relate to ISO 29148?

DD6's discovery output maps to ISO 29148's BRS (Business Requirements Specification). The discovery trail provides the traceability that 29148 requires between stakeholder needs and system requirements.
