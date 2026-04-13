# Bug Fix Examples

## Trivial bug — skip discovery

Intake: fix typo in error message

```text
I1 D1 S1 T1 P1 B1
```

Score: 6 → **skip discovery**. Clear, testable, precedented, bounded.

---

## Standard bug — shallow discovery

Intake: fix Safari WebSocket disconnect on idle timeout

```text
I1 D2 S1 T1 P2 B1
```

Score: 8 → **skip or shallow**. Mostly clear, but D2 signals browser-specific expertise needed.

---

## Complex bug — needs investigation

Intake: intermittent data corruption in batch processing

```text
I3 D3 S1 T2 P3 B3
```

Score: 15 → **deep discovery**. Intent is vague, domain is deep, no precedent, boundaries completely unclear. Multiple investigation sessions needed.
