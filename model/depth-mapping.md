# Depth Mapping

DD6 scores map to discovery depth — the recommended level of exploration before spec generation.

---

## Score to depth

| Score | Domain | Depth | Sessions | Human involvement |
| ----- | ------ | ----- | -------- | ----------------- |
| 6–8 | Clear | None | 0 | Optional spot-check |
| 9–11 | Complicated | Shallow | 1–2 | Expert review |
| 12–14 | Complex | Standard | 2–4 | Stakeholder + expert input |
| 15–17 | Deep | Deep | 4+ | Continuous collaboration |
| 18 | Chaotic | Emergency | — | Human-led stabilization |

---

## What each depth means

### None (Clear)

The problem is well-understood. Skip discovery entirely. Generate a spec from the intake description using a template. Common for bug fixes, hotfixes, and trivial changes.

### Shallow (Complicated)

The problem is solvable with focused expertise. One or two targeted sessions to clarify scope and identify risks. Common for well-scoped bug fixes and small features.

### Standard (Complex)

The problem has multiple facets that need structured exploration. Two to four sessions with phases (intent, scope, risk). Common for feature requests and enhancements.

### Deep (Deep)

The problem is emergent. Multiple iterative sessions with stakeholder alignment, hypothesis testing, and architectural exploration. Common for platform changes and complex features.

### Emergency (Chaotic)

The problem is actively destabilizing. Do not attempt structured discovery. Stabilize first, discover after. Human leads, AI assists. Common for incidents and outages.

---

## Methodology routing

Different depths benefit from different discovery methodologies:

| Depth | Recommended approach |
| ----- | -------------------- |
| None | Template-based spec generation |
| Shallow | ISO 29148 checklist + BDD scenarios |
| Standard | Structured phases (intent → scope → risk) + hypothesis tracking |
| Deep | Opportunity Solution Tree + AI Bubbles + multi-session iteration |
| Emergency | Incident triage protocol — stabilize, root-cause, plan |

DD6 acts as a methodology router — it determines which discovery approach fits the problem.

---

## Relationship to CIRK

DD6 depth determines discovery investment.
Discovery sessions produce the context that makes CIRK scoring accurate.

A problem classified as Deep (DD6 16) that goes through full discovery will produce specs with more precise CIRK vectors than if discovery had been skipped.

```text
DD6 → Discovery depth → Sessions → Spec quality → CIRK accuracy → Execution safety
```
