# Quick Examples

Copy-paste patterns for common intake types.

---

## Bug fix — known reproduction

```text
Task: fix null pointer in payment webhook handler
I1 D1 S1 T1 P1 B1 → 6 (skip)
```

---

## Bug fix — intermittent

```text
Task: random 500 errors on checkout under load
I2 D2 S1 T2 P2 B2 → 11 (shallow)
```

---

## Feature — small

```text
Task: add export CSV button to reports page
I1 D1 S1 T1 P1 B1 → 6 (skip)
```

---

## Feature — medium

```text
Task: add role-based access control to project settings
I2 D2 S2 T1 P2 B1 → 10 (shallow)
```

---

## Feature — large

```text
Task: implement real-time collaborative editing
I2 D3 S3 T2 P3 B2 → 15 (deep)
```

---

## Refactor

```text
Task: extract authentication into a shared library
I1 D2 S1 T1 P2 B2 → 9 (shallow)
```

---

## Platform change

```text
Task: add Kubernetes horizontal pod autoscaling
I1 D3 S1 T1 P2 B1 → 9 (shallow)
```

---

## Exploration / spike

```text
Task: evaluate whether GraphQL would improve our API performance
I3 D2 S2 T3 P3 B3 → 16 (deep)
```

---

## Incident

```text
Task: database connection pool exhausted in production
I1 D3 S1 T1 P2 B1 → 9 (shallow — but if actively down, treat as emergency)
```
