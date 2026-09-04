# Case — Four Products, 744 Classified Intakes

The authors of DD6 apply it to their own work. This is that data, collected on
2026-09-04 from the four repositories at their `dev` HEAD.

**This is dogfooding, not third-party adoption.** All four codebases belong to
the team that wrote the standard. Read the numbers as "what happened when the
authors used their own model", not as independent validation. Where the data is
unflattering it is reported anyway — a case study that only confirms its own
standard is worth nothing.

---

## The four products

### core618 — shared platform foundation

Reusable Django apps and React/TypeScript packages consumed by every other
product in the group: multi-tenancy, a plugin loader, a BPMN workflow engine, a
messaging platform, a dynamic configuration system.

| | |
| --- | --- |
| **Stack** | Python 3.11 · Django 5 · DRF · PostgreSQL + pgvector · Celery · React 19 · Next.js 15 · TypeScript |
| **Started** | 2026-02-28 |
| **Commits** | 773 |
| **Specs · ADRs** | 306 · 73 |
| **Source files** | 2 171 (1 586 Python, 572 TS/TSX) |

Infrastructure work: no end users, high internal blast radius. Changes here
propagate to four consumers.

### orbit618 — AI-native development governance engine

The product built to enforce exactly the kind of discipline DD6 describes:
intake classification, spec governance, agent execution policy.

| | |
| --- | --- |
| **Stack** | Python 3.11 · Django · DRF · PostgreSQL · React · TypeScript |
| **Started** | 2026-02-14 (the oldest of the four) |
| **Commits** | 425 |
| **Specs · ADRs** | 222 · 30 |
| **Source files** | 1 364 (737 Python, 619 TS/TSX) |

Included deliberately, because it produces the worst number in this document.

### myastralmap — consumer mobile product

An astrology product with generated long-form readings and narrated audio, live
in the App Store. The only one of the four with real users and real revenue.

| | |
| --- | --- |
| **Stack** | Django backend · React Native / Expo mobile · Next.js landing · LLM generation + TTS pipeline |
| **Started** | 2026-02-28 |
| **Commits** | 2 548 (3× the next repository) |
| **Specs · ADRs** | 471 · 3 |
| **Source files** | 958 (519 Python, 431 TS/TSX) |

Highest commit volume, most specs, and the highest rate of follow-up fixes —
which is what a shipped consumer product looks like.

### connectus — services marketplace

The newest repository, started six months after the others and after DD6 was
already in use.

| | |
| --- | --- |
| **Stack** | Planned: Django · PostGIS · React Native |
| **Started** | 2026-08-24 |
| **Commits** | 32 |
| **Specs · ADRs** | 26 · 5 |
| **Source files** | **4** |

**Read that last row before reading connectus's score below.** It has 26 specs
and four source files: it is specified but essentially unbuilt. Its perfect
classification rate is worth much less than it appears.

---

## Coverage

| Product | Specs | Carrying a DD6 vector | |
| ------- | ----: | --------------------: | ---: |
| core618 | 314 | 272 | 87% |
| orbit618 | 223 | 216 | 97% |
| myastralmap | 471 | 230 | 49% |
| connectus | 26 | 26 | 100% |
| **Total** | **1 034** | **744** | **72%** |

---

## The number that matters is not 744

A DD6 vector only measures something if it was assigned **before** the work.
Scoring finished work is retrospective description, not classification.

So: how many of those 744 carried the vector on the day the spec file was
created?

| Product | With a vector | Scored at birth | Backfilled | Real |
| ------- | ------------: | --------------: | ---------: | ---: |
| connectus | 26 | 26 | 0 | **100%** |
| myastralmap | 230 | 170 | 60 | 74% |
| core618 | 272 | 84 | 188 | 31% |
| orbit618 | 216 | 27 | 189 | **12%** |
| **Total** | **744** | **307** | **437** | **41%** |

**41%.** Fewer than half the scores in these repositories were decisions. The
rest are descriptions written afterwards.

**orbit618 is worst, at 12%** — and orbit618 is the governance engine. The
product built to enforce this discipline is the one that skipped it, adopting
DD6 after most of its specs already existed and backfilling the rest.
connectus is at 100% because it began under the discipline rather than
acquiring it — but see its source-file count above before drawing a conclusion
from that.

*Method: for each spec file, find the commit that created it, read the file as
it existed in that commit, check whether the vector was already present. Files
whose creation commit is unreachable under their current path (renames) are
excluded, which is why this totals 744 where a plain content scan finds 806.*

---

## Backfilled scores are biased, and the bias has a direction

307 scored-at-birth vectors and 437 backfilled ones, in the same repositories,
can be compared directly.

| Axis | Scored at birth | Backfilled | Delta |
| ---- | --------------: | ---------: | ----: |
| **I** — Intent clarity | 1.87 | 1.42 | **−0.45** |
| **D** — Domain depth | 1.82 | 2.50 | **+0.68** |
| **S** — Stakeholder convergence | 1.62 | 2.00 | +0.38 |
| **B** — Boundary clarity | 1.68 | 2.00 | +0.31 |
| **P** — Precedent | 1.85 | 2.01 | +0.16 |
| **T** — Testability | 1.71 | 1.84 | +0.13 |

**Hindsight makes intent look clearer and everything else look harder.**

That is a coherent signature rather than noise. Once the work is finished you
know what was actually wanted, so `I` falls. You also know how much specialist
knowledge it consumed, how far it sprawled and who had to be consulted — so `D`,
`S` and `B` rise. `I` moving *against* the other five is what distinguishes this
from people simply rating old work as harder.

### Controlling for the repository

Backfilled specs are older work, which might genuinely have been harder.
Comparing within each repository removes that confound:

| Repository | n (birth / backfill) | I | D |
| ---------- | -------------------: | - | - |
| core618 | 84 / 188 | 2.07 → **1.37** | 1.99 → **2.82** |
| orbit618 | 27 / 189 | 2.11 → **1.40** | 2.19 → **2.33** |
| myastralmap | 170 / 60 | 1.68 → **1.63** | 1.65 → **2.02** |

`I` falls in all three. `D` rises in all three. The direction survives.

### What does not survive

The composite sum. Across the whole set, backfilled vectors average 11.76
against 10.55 — but within orbit618 the sum *falls* (12.15 → 11.65), and the
overall gap is driven by myastralmap, whose scored-at-birth specs describe
genuinely smaller work (9.51).

So the bias lives in the **shape of the vector, not in its total** — which is
what [the model already says](../model/dd6.md#important-note):

> The vector matters more than the total.

That line was written as guidance. This is the first measurement supporting it.

---

## Distribution

Across all 744 vectors:

| Band | Domain | Count |
| ---- | ------ | ----: |
| 6–8 | Clear | 122 |
| 9–11 | Complicated | 293 |
| 12–14 | Complex | 312 |
| 15–17 | Deep | 77 |
| 18 | Chaotic | 2 |

Two intakes at 18 out of 744 is the reassuring figure. A band reserved for
"stabilize first" should be nearly empty; if it held eighty, the scale would be
broken.

---

## Rework index — what we tried, and why there is no number here

The question worth answering is whether classifying before the work reduces
rework afterwards. If it does not, the model is decoration.

We measured rework as follow-up `fix:` and `revert:` commits referencing a
spec ID after that spec first appeared, then split by scored-at-birth versus
backfilled:

| Repository | Group | fix/spec | % with any fix | median age |
| ---------- | ----- | -------: | -------------: | ---------: |
| core618 | at birth | 0.20 | 17% | 99 d |
| core618 | backfilled | 0.07 | 5% | 187 d |
| orbit618 | at birth | 0.44 | 20% | 102 d |
| orbit618 | backfilled | 0.05 | 4% | 175 d |
| myastralmap | at birth | 0.97 | 62% | 14 d |
| myastralmap | backfilled | 0.25 | 15% | 130 d |

Read naively, classifying up front *triples* rework. That conclusion is wrong,
and the reason it is wrong is instructive.

**The two disciplines are entangled.** Writing the spec ID into the commit
message and scoring the intake before starting arrived in these repositories at
the same time. Specs from before that period did get fixed — those fixes just
carry no spec ID, so they are uncountable. A 187-day-old spec showing a 5% fix
rate while a 99-day-old spec in the same codebase shows 17% is not a property of
the code; it is a property of the commit convention.

**So rework cannot be recovered retrospectively here, and we are not publishing
a number that does not hold.** Measuring one discipline through an instrument
that arrived with it is circular.

What would work is forward-looking: fix the commit convention as a hard gate,
wait for a cohort of specs long enough to have accumulated their fixes, and only
then compare. That is instrumentation, not analysis, and it is the honest next
step.

---

## What we would tell an adopting team

1. **Start on day one, or do not count it.** connectus at 100% and orbit618 at
   12% is the same team, the same period, the same tooling. The only difference
   is whether the repository existed before the discipline did.
2. **Do not backfill.** Not because it is dishonest, but because it produces
   confidently wrong vectors — clearer intent and deeper domain than the work
   actually presented at the time.
3. **If you already backfilled, mark those scores.** They remain useful as
   description. They are not usable as calibration data, and mixing the two
   populations silently corrupts any calibration you attempt later.
4. **Instrument rework before you need it.** We could not measure the one thing
   that would prove the model pays for itself, because the instrument arrived
   with the practice. Do not repeat that.
