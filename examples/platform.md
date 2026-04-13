# Platform Change Examples

## Infrastructure change — moderate discovery

Intake: migrate from Redis to Valkey for session caching

```text
I1 D2 S1 T1 P2 B1
```

Score: 8 → **skip or shallow**. Clear intent, bounded scope, testable.

---

## Architecture change — deep discovery

Intake: decompose monolith user service into microservices

```text
I2 D3 S3 T2 P3 B3
```

Score: 16 → **deep discovery**. Every dimension is elevated. Multiple sessions across teams required.

---

## Migration — skip discovery

Intake: migrate from PostgreSQL 14 to 16

```text
I1 D2 S1 T1 P1 B1
```

Score: 7 → **skip discovery**. Well-documented upgrade path, clear scope, strong precedent.
