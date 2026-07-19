---
type: reference-and-governance
source: agency-os.html (methodology) + ../reference-team-protocol-full.md
  (team, points, equity — both now stored in this folder)
scope: Phase Infinity governance, merged into this repo's overall scope 2026-07-18
last_updated: 2026-07-17
---

## Agency OS — Structural Reference & Governance (Phase ∞)

This document is the canonical reference **and** governance record for how
the Agency OS methodology applies to Phase ∞. The full narrative source
(insights, rationale, abbreviation glossary, for all four phases) now lives
in-repo at `framework/agency-os.html` — it is no longer an external file
tracked only by pointer. This `.md` file stays a structural index for quick
lookup while working; the `.html` is the source of truth for content.

### Governing scope

- **Merged 2026-07-18:** this governance now applies repo-wide, alongside
  the Phase 0 rules already in `SYSTEM.md` — this is no longer a separate,
  restricted repo. Souhibe has full read/write access to this content,
  same as the other 5, per the explicit merge decision recorded in root
  `README.md` and `reference-team-protocol-full.md`.
- Access restriction, historical: for a period, the core 5 — Alaaedeen,
  Dazdaz, Nadji, Abdelaziz, Bilal — were the only members with any access
  to this content, in a separate repo (`courseli-agency-os`). That
  restriction has been lifted; kept here as historical context only.
- Decision authority: Claude may move a task to `under-review` and produce
  a report. Only Alaaedeen or Dazdaz may close a task as `done` or
  `done-with-gaps`, and only after an actual meeting — `meeting_date` is a
  required field on any such closure. This applies to all four phases below,
  not just the current Foundation phase.
- Points/reward protocol (§8–9 of `../reference-team-protocol-full.md`) is
  **active** for Phase Infinity as of 2026-07-17 — tasks are scored per the
  §8 formula, and Foundation-phase points feed the 10%-of-60% equity
  carve-out below. (This supersedes the earlier deferral; see "Equity
  governance" section.)

### Phase 01 — Foundation *(current phase, see 02-missions/)*
"Build it right before you build it big"
- **Strategist:** Discovery & Intelligence → Brand Architecture → Business
  Model Design → Validation Strategy
- **UX Engineering:** User Research & Mapping → Information Architecture →
  Design System Foundation → Online Presence Build

### Phase 02 — Launch *(not yet started)*
"Get to market with precision, not perfection"
- **Strategist:** Launch Playbook → Content & Distribution → Sales &
  Conversion Strategy → KPI Dashboard Design
- **UX Engineering:** Onboarding Engineering → Core Product UX → Conversion
  Optimization → Feedback Loop Systems

### Phase 03 — Growth *(not yet started)*
"Systematize what works, eliminate what doesn't"
- **Strategist:** Growth Model Architecture → Channel Scaling → Team &
  Operations Design → Competitive Moat Building
- **UX Engineering:** Product-Led Growth Engineering → Platform &
  Scalability → Advanced Design System → Intelligence Layer

### Phase 04 — Scale *(not yet started)*
"Multiply across markets, segments & structure"
- **Strategist:** Strategic Scaling Plan → Capital & Investor Strategy →
  Brand at Scale → Exit & Long-Term Value
- **UX Engineering:** Enterprise UX → Multi-Product Architecture → Quality &
  Reliability at Scale → Future-Proofing & Innovation

### Master Principle
The internal database (evidence, decisions, rationale) is the brain; the
external deliverables are the hands. Deliverables without a documented
evidence base behind them are decoration, not strategy — this is why every
mission/process/procedure/task in this repo carries its rationale inline
rather than just a checkbox.

### Convergence Principle
At the end of each phase, the two tracks converge: the Strategist identifies
pain points through JTBD research, the UX Engineer validates them through
discovery interviews — same users, different questions. This repo's
Foundation goal ends with an explicit convergence task for exactly this
reason.

### Task time monitoring
Every task in `02-missions/*/tasks/*.md` carries `start_date`, `due_date`,
`completed_date`, and `points`, plus reminder/penalty state flags
(`start_reminder_sent`, `deadline_warning_sent`, `penalty_stage`). The
protocol for start reminders, deadline warnings, and the 0 → -1 penalty
escalation lives in root `CLAUDE.md` — this governance file states the
authority (who can close/score), `CLAUDE.md` states the mechanics (when to
notify, who to notify, over which channel).

### Task time monitoring
Every task in `02-missions/*/tasks/*.md` carries `start_date`, `due_date`,
`completed_date`, and `points`, plus reminder/penalty state flags
(`start_reminder_sent`, `deadline_warning_sent`, `penalty_stage`). The
protocol for start reminders, deadline warnings, and the 0 → -1 penalty
escalation lives in root `CLAUDE.md` — this governance file states the
authority (who can close/score), `CLAUDE.md` states the mechanics (when to
notify, who to notify, over which channel).

### Points system (source: `../reference-team-protocol-full.md` §8)
Points are **not** invented specially for Phase Infinity — they are the
exact same formula used company-wide, everywhere in this repo:

```
Task points = (timing points × task weight) + bonuses − penalties

Timing points:  early = 2 | on-time = 1 | late ≤24h = 0 (grace) | late >24h = -1
Task weight:    1 light / 2 medium / 3 heavy — set at task creation (`weight:` field)
Bonus:          +1 if closed "done" first pass, no "done-with-gaps" cycle
Extra penalty:  -1 if `blocks:` is non-empty AND late >24h
Manual bonus:   +2 for initiative beyond scope — human-granted only, written reason required
Quality gate:   "done-with-gaps" holds points at 0 until the gap is fixed and it closes as done
```

Early-reporting a problem — including in someone else's task — is never
scored negatively. Claude calculates the timing component automatically and
flags it; only Alaaedeen or Dazdaz write the final `points` value into a
task, at the same meeting where they close it.

### Equity governance — Phase ∞ Foundation carve-out
The company-wide split (`../reference-team-protocol-full.md` §9) is
**40% fixed / 60% performance-based**, frozen only at the real Freeze Point
(first paying customer, or a 6-month fallback) — non-binding internal
incentive accounting until then, exactly as stated there. Phase ∞ does not
change that split; it defines how the **Foundation phase specifically**
draws from the 60% performance pool:

```
Of the 60% performance pool:
  10 percentage points  → reserved for Phase ∞ / Foundation task points
                            (this phase only), split ONLY among
                            the 5 people who actually work Phase ∞ tasks:
                            Alaaedeen, Dazdaz, Nadji, Abdelaziz, Bilal
  50 percentage points  → reserved for Phase ∞'s remaining phases
                            (Launch, Growth, Scale) and any non-Phase-∞
                            work — not yet split further. Souhibe's
                            performance-based equity is earned from this
                            50% pool instead of the 10%, since Marketing &
                            Content work isn't part of Foundation-phase
                            scope.

Person's share of the 10% = (person's Foundation-phase points ÷ sum of the
                              5 eligible people's Foundation-phase points,
                              at this phase's own closing point) × 10
```

**✅ Resolved (see `team/souhibe.md`):** the 3 tasks previously owned by
Souhibe (`formalize-tone-of-voice`, `setup-social-media`,
`waitlist-capture`) were reassigned to Alaaedeen, Bilal, and Dazdaz
respectively, since he isn't in the 10%-pool group. He now owns 0 tasks in
`strategist-track`/`ux-engineering-track`, consistent with this carve-out.
**Note as of the single-repo merge:** Souhibe now has full repo access
(read/write) like everyone else — this carve-out's task-ownership
exclusion is a separate, still-standing decision from repo *access*; the
two are not the same thing.

This 10-point pool is scored only from points earned on tasks inside
`02-missions/strategist-track/` and `02-missions/ux-engineering-track/`,
under the exact points formula above — it
is a sub-allocation of the same 60% pool, not a separate equity pool with
its own rules. It is still subject to the same Freeze Point mechanics as
the rest of §9: nothing here is real equity until that event happens, and
Alaaedeen/Dazdaz still hold sole authority to record final points.

### Change control for this document
Any edit to phase/step names or governance rules above must originate from a
change in `agency-os.html` (content) or the root `README.md` / team working
system (governance rules) — this file should never drift ahead of either
source. When both are updated, bump `last_updated` above.
