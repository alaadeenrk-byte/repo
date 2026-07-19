---
type: reference
---

# CourseLi Team — Organigram & Approval Matrix

```
        Dazdaz — Operations & External Lead        Alaaedeen — Product & Tech Lead
        (face of the project, sales, external        (final say on product decisions,
         relationships, day-to-day team operations)    architecture, tech direction,
                                                          brand identity)
                        └──────────────┬──────────────┘
                           Joint decisions: pricing/packages,
                           hiring, roadmap timing
                                        │
        ┌───────────────────┬──────────┼──────────────────┬────────────────────┐
        │                   │          │                  │                    │
 Alaaedeen ↔ Nadji      Abdelaziz    Souhibe             Bilal
 (MVP build engine)   (finance/    (Marketing &         (floating QA +
                       logistics —  Content — full        requirements
                       full domain  domain authority)      gathering)
                       authority)
```

Full detail for each person's role, requirements, and success markers: see
`/team/*.md`.

## Approval Matrix

| Who does the work | Reviews first | Final sign-off |
|---|---|---|
| Alaaedeen | Dazdaz (documented objection) | Alaaedeen |
| Dazdaz | Alaaedeen (documented objection) | Dazdaz |
| Nadji / Abdelaziz | Alaaedeen & Dazdaz (both notified) | Alaaedeen (technical) |
| Souhibe | Alaaedeen & Dazdaz (both notified) | Souhibe (Marketing & Content only) |
| Bilal | Depends on task type | Depends on domain |

## Default Rule
Any decision whose ownership is unclear defaults to a **joint decision**
between Alaaedeen and Dazdaz until explicitly settled otherwise.

## Repos This Team Uses
- **This repo** (`courseli`) — the whole project, both phases, merged
  2026-07-18. Full team access, including Souhibe.
- `courseli-platform` — product code only, created when Phase 0 build
  resumes. Souhibe: no access. The only remaining repo split.

## Points & Equity
The points/reward and equity system (40% fixed / 60% performance-based
split) is **active for Phase Infinity work** (a 10-point carve-out of the
60% pool) — full protocol, formula, and reasoning in
`/reference-team-protocol-full.md`, including section 10. It applies to
both phases; the full formula and rules are also restated in `SYSTEM.md`.
