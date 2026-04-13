# References

Theoretical foundations and industry context for DD6 and CIRK.

These references are shared across both standards. Each is cited where relevant in the respective model documentation.

---

## Academic and book references

### Huyen, C. (2025). *AI Engineering: Building Applications with Foundation Models*. O'Reilly Media.

Comprehensive guide to building production AI applications. Key contributions to DD6/CIRK:
- **Compound mistakes** (p.278): agent accuracy drops exponentially with steps (95% per step → 60% over 10 steps). Justifies DD6's proportional discovery — better problem understanding reduces agent steps and compound errors.
- **Planning granularity** (p.289): "A detailed plan is harder to generate but easier to execute." DD6 depth determines the level of planning detail invested in discovery.
- **Agent failure modes** (pp.298-300): wrong tool, wrong plan, compound errors, efficiency waste. CIRK dimensions map directly to these failure categories.
- **Guardrails architecture** (pp.451-455): input and output guardrails as standard AI engineering pattern. Validates DD6's guardrail-first discovery approach.
- **Model router** (pp.456-460): routing queries to different models based on complexity. CIRK's model tier mapping (Trivial→cheap, Complex→max quality) implements this pattern.
- **AI pipeline orchestration** (pp.472-474): components definition and chaining. Both DD6 and CIRK serve as classification inputs to orchestrated pipelines.

### Snowden, D.J. & Boone, M.E. (2007). "A Leader's Framework for Decision Making." *Harvard Business Review*.

Introduced the Cynefin framework — four complexity domains (Clear, Complicated, Complex, Chaotic) with domain-appropriate response strategies. DD6's depth mapping (None, Shallow, Standard, Deep, Emergency) adapts Cynefin's domains specifically for AI-assisted software discovery, with original dimensions replacing VUCA.

### Snowden, D.J. (2021). *Cynefin — Weaving Sense-Making into the Fabric of Our World*. Cognitive Edge.

Extended treatment of sense-making in complex systems. DD6's core thesis — that different problem types require fundamentally different discovery strategies — derives from Snowden's principle that you must understand the domain before choosing a response.

### Torres, T. (2021). *Continuous Discovery Habits*. Product Talk.

Establishes cadence-based discovery with hypothesis tracking and Opportunity Solution Trees. Influences DD6's structured session phases and the principle that discovery should be continuous and proportional, not a one-time event.

### Stacey, R.D. (1996). *Strategic Management and Organisational Dynamics*. Pitman Publishing.

The Stacey Matrix (Agreement × Certainty) for classifying organizational problems. DD6's two-axis nature (clarity dimensions × complexity dimensions) draws conceptual inspiration from Stacey's insight that both agreement and certainty must be assessed independently.

### Evans, E. (2003). *Domain-Driven Design: Tackling Complexity in the Heart of Software*. Addison-Wesley.

Bounded Contexts and Event Storming as discovery techniques for complex domains. DD6's Domain depth (D) and Boundary clarity (B) dimensions directly address DDD's concern: you must understand the domain boundaries before designing the solution.

### Adzic, G. (2011). *Specification by Example*. Manning Publications.

Examples as specifications — concrete instances that define behavior. DD6's Testability (T) dimension assesses whether the outcome can be verified through examples, a prerequisite for agents that execute against spec.

### Adzic, G. (2012). *Impact Mapping*. Provoking Thoughts.

WHY → WHO → HOW → WHAT structure for connecting business goals to deliverables. Influences DD6's recommended discovery template phases (Intent → Scope → Risk).

### Johansen, B. (2007). *Get There Early: Sensing the Future to Compete in the Present*. Berrett-Koehler.

Formalized the VUCA framework (Volatility, Uncertainty, Complexity, Ambiguity) for strategic leadership. DD6 acknowledges VUCA as theoretical inspiration but deliberately creates original dimensions — VUCA's dimensions overlap significantly (Emerald systematic review, 2022) and lack the specificity needed for software discovery classification.

### Bühler, E.R. (2024). "AI Bubbles: Augmenting Cynefin with AI for Enhanced Decision-Making." *Enterprise Agility Magazine*.

Proposes using AI to create localized "bubbles" of enhanced sense-making within complex domains. DD6's Deep discovery depth uses parallel AI-assisted sessions as sense-making probes — each exploring a different facet of the problem.

### Yawson, R.M. & Goryunova, E. (2025). "Nested Complexity: A Conceptual Framework for Leveraging AI for Sustainable Organizations." *SAGE Journals*.

Multi-layered complexity model spanning technological, ethical, regulatory, and environmental dimensions. Validates DD6's multi-dimensional approach — single-axis complexity measures are insufficient for AI-assisted development.

---

## Industry standards and frameworks

### OWASP Agentic AI Top 10 (December 2025)

First formal taxonomy of risks specific to autonomous AI agents. Identifies: goal hijacking, tool misuse, identity abuse, supply chain risks, code execution, memory poisoning, insecure communications, cascading failures, human-agent trust exploitation, rogue agents. CIRK's K (Integration Risk) and R (Review) dimensions map directly to several of these categories. DD6's discovery process helps prevent goal hijacking by clarifying intent before execution.

### Microsoft Agent Governance Toolkit (April 2026)

Open-source runtime security governance for AI agents. Maps all 10 OWASP risks with deterministic, sub-millisecond policy enforcement. Validates that execution governance (CIRK's domain) and pre-execution classification (DD6's domain) are recognized industry needs, not theoretical constructs.

### Singapore Model AI Governance Framework for Agentic AI (IMDA, January 2026)

Government framework structured around four dimensions: risk bounding upfront, human accountability, transparency, ecosystem trust. DD6 aligns with "risk bounding upfront" — classifying the problem before agents act. CIRK aligns with "human accountability" — defining when humans must review agent output.

### McKinsey 2026 AI Trust Maturity Survey (March 2026)

Survey of ~500 organizations: only 30% report governance maturity level ≥ 3; 64% of companies with revenue > $1B reported losses > $1M associated with AI system failures in 2025. Establishes the business case for both DD6 (prevent failures through better discovery) and CIRK (prevent failures through execution governance).

### NIST AI Risk Management Framework 1.0 (January 2023)

Four functions: Govern, Map, Measure, Manage. DD6 operates in the "Map" function (understanding the problem space before development). CIRK operates in the "Measure" function (quantifying execution risk). Together they span two of the four NIST functions.

### ISO/IEC 42001:2023 — AI Management Systems

First certifiable AI management system standard. Plan-Do-Check-Act governance structure with 38 controls. DD6's discovery governance and CIRK's execution governance provide the operational layer that ISO 42001 requires at the process level.

### ISO/IEC/IEEE 29148:2018 — Requirements Engineering

Standard for requirements quality and documentation structure: BRS, StRS, SyRS, SRS. DD6's discovery output maps to BRS (Business Requirements Specification). CIRK's execution input maps to SRS (Software Requirements Specification). The discovery trail provides the traceability that 29148 requires.

### EU AI Act (August 2026 — high-risk obligations)

First enforceable, risk-based AI regulatory regime. Requires documentation, monitoring, traceability, and human oversight for high-risk systems. DD6's discovery audit trail provides traceability. CIRK's R3 and K3 scores can trigger compliance review requirements.

---

## Software engineering references

### Richardson, C. (2026). "Why GenAI-based coding agents are a complex domain in Cynefin." *microservices.io*.

Argues that using AI coding agents is inherently complex in Cynefin terms — consequences of decisions are only visible through testing and real-world use. Validates DD6's premise that problem classification must precede agent execution.

### Emerald Publishing (2022). "Clarifying the conceptual map of VUCA: a systematic review." *International Journal of Organizational Analysis*.

First systematic review of VUCA. Concludes that "there is no clear distinction among the constructs, and they do overlap with each other." This finding motivated DD6's decision to create original dimensions rather than reuse VUCA's overlapping V-U-C-A.

### Cascio, J. (2020). "Facing the Age of Chaos." *Medium*.

Proposed BANI (Brittle, Anxious, Non-linear, Incomprehensible) as a successor to VUCA. Demonstrates ongoing dissatisfaction with VUCA's specificity, further supporting DD6's original dimensions.

### INCOSE (2025). "A Systems Engineering Framework for Navigating Complexity." *INCOSE International Symposium*.

Introduces the Pleko framework as a systems engineering evolution of Cynefin. Demonstrates that domain-specific adaptations of sense-making frameworks are an active area of development — DD6 is the adaptation for AI-assisted software discovery.

---

## Related standards

### CIRK — Execution Classification Model

Companion standard to DD6. Classifies execution risk across four dimensions (Context, Iteration, Review, Integration Risk). Score range 4–12.

Repository: [github.com/core-618/cirk](https://github.com/core-618/cirk)
Website: [cirk.dev](https://cirk.dev)

### DD6 — Deep Discovery Classification Model

Classifies problem complexity across six dimensions (Intent, Domain, Stakeholder, Testability, Precedent, Boundary). Score range 6–18.

Repository: [github.com/core-618/dd6](https://github.com/core-618/dd6)
Website: [dd6.dev](https://dd6.dev)
