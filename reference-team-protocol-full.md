---
type: reference
status: fully specified — points/equity NOT yet active, see note in SYSTEM.md
completeness: full detail, not condensed — this is the reference copy
---

# CourseLi Team — Full Working System Reference

`organigram.md` has the quick-reference chart. This file has the complete
reasoning and protocol behind it, so nothing from the original design
discussion is lost.

## Why the Approval Matrix Works the Way It Does
Final authority (Alaaedeen: product/tech, Dazdaz: operations/external) does
not change under peer review. Every deliverable — including Alaaedeen's and
Dazdaz's own — passes through the other as a mandatory reviewer before
closing. If the reviewer objects, the objection is written down and
answered explicitly in the same file/PR; it is never silently overridden
and never silently ignored. This turns disagreement into a documented
exchange rather than a private veto or a private grudge.

## Why the Task State Machine Requires a Human Meeting
`meeting_date` is a required field on every `done`/`done-with-gaps`
decision. This is a human-discipline rule, not a fully technically
enforceable one — nothing can verify a meeting actually happened. The
closest technical enforcement available is refusing to accept a decision
record with that field empty, and Claude flagging the rule if asked to
record a decision without a meeting mentioned.

## Why CODEOWNERS + Branch Protection Matter
Claude can open a PR; it can never merge one. Branch protection on `main`
(PR required, CODEOWNERS approval required, no direct push, no self-merge)
is what makes "Claude never closes anything by itself" an enforced
technical rule instead of just a written one.

## Repo Access — Merged 2026-07-18

GitHub permissions are repository-wide, not folder-wide — there is no way
to give someone Write on part of a repo and nothing on another part of the
same repo. This principle is exactly why `courseli-platform` (product code)
stays a separate repo — Souhibe has no access there, and code needs
protecting from a non-technical role regardless of anything else.

It's also why, for a period, Phase Infinity content lived in a second,
Souhibe-restricted repo (`courseli-agency-os`) separate from this one. That
wall has since been removed by explicit decision: this repo now merges both
phases, and Souhibe has full read/write access to all of it, same as the
other 5. His CODEOWNERS entries scope *required-reviewer* status to
Marketing & Content paths — that governs merge approval, not read
visibility.

**What did not change:** his task ownership within the Phase Infinity
Foundation-phase equity carve-out (section 10 below) — he still owns 0
tasks there, since access and points/equity eligibility are separate
decisions. Reversing one does not automatically reverse the other.

---

## Points System — Full Formula (ACTIVE for Phase Infinity)

```
Task points = (timing points × task weight) + bonuses − penalties

Timing points:  early = 2 | on-time = 1 | late ≤24h = 0 (grace period) | late >24h = -1
Task weight:    1 light / 2 medium / 3 heavy — set when the task is created

Bonus: +1        task closes as "done" on the first pass, no "done-with-gaps" cycle
Extra penalty: -1 task has non-empty "blocks" AND is late >24h (it stalled other people's work)
Manual bonus: +2  initiative beyond what was asked, granted explicitly by the reviewer with a
                  written reason — never automatic

Strict rule: early-reporting a problem or mistake — including in someone else's task — is
             NEVER scored negatively. It should be logged as a separate positive contribution
             if it prevented a larger issue. Punishing early disclosure teaches people to hide
             problems instead of surfacing them.

Quality gate: on "done-with-gaps", points stay pending (0) until the gap is fixed and the task
              closes as done. This exists specifically to prevent rewarding fast-but-flawed
              work the same as careful, complete work.
```

No exemptions: every team member, including Alaaedeen and Dazdaz, is scored
under this exact formula on their own real tasks — there is no
reviewer-only role exempt from being scored.

## Equity — Full Protocol (NOT YET ACTIVE)

**Framing:** this entire section is a non-binding internal incentive system
for the MVP/validation stage. No paperwork, no legal commitment, no shares
actually issued, until the Freeze Point below is reached.

### The Split: 40% Fixed / 60% Performance-Based

| Person | Original reference % | Fixed weight within the 40% |
|---|---|---|
| Alaaedeen | 35% | 14% |
| Dazdaz | 20% | 8% |
| Nadji | 15% | 6% |
| Abdelaziz | 15% | 6% |
| Souhibe | 10% | 4% |
| Bilal | 5% | 2% |
| **Total** | 100% | **40%** |

```
Person's share of the 60% = (person's total points ÷ total team points) × 60
```
Calculated once, at the Freeze Point, using every point accumulated by
every person up to that exact moment.

### Freeze Point
**Triggering event:** the first real school (not Souhibe — he's part of the
team) actually pays for a CourseLi package.
**Fallback deadline:** 6 months from the start of active work with no
paying customer yet — points freeze automatically at that date regardless
of the reason for the delay.

**Why a sales event, not a technical milestone:** a technical "MVP is done"
milestone proves the product works, not that anyone will pay for it. A real
paying customer has one unambiguous date; "is the MVP technically ready"
can always be argued about.

### After the Freeze Point
- Final 40%+60% split formalized into an actual shareholder agreement,
  drafted with a lawyer, entirely outside GitHub
- Standard time-based vesting begins from that point forward (not
  retroactively), including Alaaedeen's own equity
- Everything before the Freeze Point was the internal incentive mechanism
  only, not a legal claim on anything

### Why the Points Engine Never Issues Equity Automatically
A continuously-recalculating formula from GitHub points straight to real
company shares would be gameable (splitting one large task into ten trivial
ones to inflate score), legally unfounded ("GitHub points" aren't a
recognized basis for ownership in a dispute), and liable to produce
outcomes nobody intended (out-scoring someone in a given month doesn't
automatically mean deserving more permanent ownership than someone carrying
founder-level risk). This is why the system freezes once, at one clearly
defined event, instead of reallocating ownership forever.

## Souhibe — Open Items Not Yet Resolved
- Exact profit-share percentage and conditions — separate, signed legal
  agreement, distinct from the 4%+performance equity above
- Whether a future CDO promotion changes his fixed 4% base or his approval
  scope beyond Marketing & Content

## Bilal — Design Note
Deliberately has 0% in the fixed-base reference table above is NOT
correct — he has 2% (5% of the original 40% reference pool, scaled). This
reflects an earlier design discussion where a 0%-fixed-base option was
considered for him specifically because his role isn't fixed yet, before
the team settled on the 5%/2% figures shown in the table. **If the team's
intent was actually 0% fixed for Bilal with entry only via the performance
pool, the table above needs a correction — this note exists so that
ambiguity isn't silently resolved one way without you catching it.**

---

## 10. Phase ∞ Foundation Carve-Out (added at single-repo merge)

### Equity governance — Phase ∞ Foundation carve-out
The company-wide split (§9 above, this same file) is
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
