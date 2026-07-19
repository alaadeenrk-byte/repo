# courseli

The team's complete operating system for CourseLi — **one project, two
phases, merged into a single repo.**

- **Phase Infinity (live)** — Agency OS methodology applied to CourseLi
  itself: market validation, brand strategy, business model design. Lives
  in `02-missions/strategist-track/` and `02-missions/ux-engineering-track/`.
- **Phase 0 (on-hold)** — the actual MVP build. Lives in `02-missions/
  mvp-reception-core/` (and future mission folders as they're added).
  Resumes once Phase Infinity's validation work confirms CourseLi is worth
  building.

Product code itself is **not** here — that's `courseli-platform`, a
separate repo created when Phase 0 build resumes.

**Start here:** read `SYSTEM.md` in full before doing anything else. If
you're setting up Claude Desktop, paste `SYSTEM.md` into your Project's
custom instructions so it loads automatically every session.

## Who has access

**Full read/write for all 6 core team members, including Souhibe** —
Alaaedeen, Dazdaz, Nadji, Abdelaziz, Bilal, Souhibe. This is a deliberate
merge decision (2026-07-18): earlier versions of this system split Phase
Infinity content into a separate, Souhibe-restricted repo; that wall has
been removed entirely. He now sees everything here, same as everyone else.
CODEOWNERS still scopes his *required-reviewer* status to Marketing &
Content paths — that governs merge approval, not read visibility.

**`courseli-platform` remains a separate repo, Souhibe: no access there.**
That split is about protecting source code from a non-technical role and
is unrelated to the Phase 0/Phase Infinity question this merge resolved.

**Note on task ownership vs. access:** Souhibe currently owns 0 tasks in
the Phase Infinity Foundation work (3 tasks were reassigned away from him
earlier, per the equity carve-out rules — see `reference-team-protocol-full.md`
section 10 and `team/souhibe.md`). That is a *separate* decision from
today's access change and was not automatically reversed by it. If you also
want those 3 tasks back with him, say so explicitly.

## Structure
```
SYSTEM.md                         → Claude's operating rules — read first
reference-working-calendar.md     → CRITICAL — governs every date in this repo, read second
CODEOWNERS                         → enforces the approval matrix on every merge
organigram.md                      → quick-reference team structure + approval matrix
reference-team-protocol-full.md    → full points/equity protocol + Phase Infinity carve-out (ACTIVE)
00-brand/                          → production brand assets (logo, colors, type)
01-product/
  architecture-overview.md          → full, unabridged 15-category product architecture
  feature-spec-draft.md             → granular staff-facing feature draft (~180 items)
  project-history.md                → evolution trail from original demo to current architecture
01-goals/
  smart-goals.md                    → Phase 0 SMART goal (on-hold)
  smart-goal-foundation.md          → Phase Infinity SMART goal (live)
02-missions/
  mvp-reception-core/                → Phase 0 example mission tree
  strategist-track/                  → Phase Infinity — market/business strategy
  ux-engineering-track/              → Phase Infinity — research/design/UX
  convergence-synthesis.md           → Phase Infinity closing task, both tracks
framework/
  agency-os-reference.md             → Agency OS methodology structural index + equity carve-out
brand-identity/
  brand-identity-full.md             → full strategic brand work (naming exploration, rationale)
team/                              → one file per person — role, responsibilities, authority,
                                       job requirements, equity, languages, live task index
```

## Workflow
Every task moves `pending → under-review (Claude) → done/done-with-gaps
(human, after a meeting)`. Procedures/Processes/Missions/Goals auto-close
once their children close, confirmed at a short verification meeting. Every
Mission/Goal file is tagged `phase: 0` or `phase: infinity` in its
frontmatter. Full detail in `SYSTEM.md`.

## Points & Equity
40% fixed / 60% performance-based split, frozen at first paying customer or
6-month fallback. **Active** for Phase Infinity work specifically (a
10-percentage-point carve-out of the 60% pool, scored now) — full mechanics
in `reference-team-protocol-full.md` section 10. "Active" means points are
tracked and staged, not that real equity has been issued — nothing is
legally binding until the actual Freeze Point.

## Working Calendar
Project start **2026-07-20** (Monday). Work week **Saturday–Thursday**,
**Friday fully off**, hours **09:00–18:00** Algeria time. Applies to every
date field in every file, both phases, no exceptions. Full detail:
`reference-working-calendar.md`.
