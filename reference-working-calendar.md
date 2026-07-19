---
type: reference
status: CRITICAL — governs every date field in every repo
effective_date: 2026-07-20
---

# CourseLi — Working Calendar (CRITICAL)

This file governs **every** `start_date`, `due_date`, `completed_date`, and
`meeting_date` field on every Task, Procedure, Process, Mission, and SMART
Goal in this repo — both Phase 0 and Phase Infinity work. No date field
anywhere in this repo may violate the rules below.

## Project Start Date
**Monday, 2026-07-20.** This is the anchor date for all active scheduling
from this point forward. The illustrative example in
`02-missions/mvp-reception-core/` has been corrected to start from this
date and comply fully with this calendar (as of 2026-07-18) — it previously
contained dates predating this file and one date landing on a Friday
(2026-07-17), both now fixed. Treat it as a compliant example, not a live
commitment — Phase 0 itself remains on-hold.

## Work Week
| Day | Status |
|---|---|
| Saturday | Working day |
| Sunday | Working day |
| Monday | Working day |
| Tuesday | Working day |
| Wednesday | Working day |
| Thursday | Working day |
| **Friday** | **Full day off — no work, no deadlines, no meetings** |

## Working Hours
**09:00–18:00**, Algeria local time (Africa/Algiers, UTC+1, no DST).

## Hard Rules — Apply to Every Level (Task/Procedure/Process/Mission/Goal)
1. **No `due_date`, `start_date`, or `meeting_date` may fall on a Friday.**
   If a calculation would land on a Friday, roll forward to the next
   Saturday.
2. **No date/time may fall outside 09:00–18:00.** A task "due end of day"
   is due at 18:00, not midnight.
3. **Fridays do not count toward any duration calculation** — task weight
   estimates, the "≤24h late = 0 points" grace period, and any "N days"
   language anywhere in either repo all mean **working days**, not
   calendar days.

## ⚠️ Assumption Flagged for Confirmation — Grace Period Mechanics
The points formula (`reference-team-protocol-full.md` §Points System) uses
a "late ≤24h = 0 points, late >24h = -1" rule. Applying the working-hours
rule above, I'm treating this as **≤1 full working day past `due_date`**,
measured only across 09:00–18:00 working-day windows, skipping Friday
entirely. Example: a task due Thursday 18:00 gets its grace period through
Saturday 18:00 (Friday doesn't count), not Friday 18:00.

**This is my interpretation, not something you stated explicitly — confirm
it's correct, since it directly affects how the points system scores
lateness and that has downstream equity implications once the Freeze Point
is reached.**

## What This Changes Going Forward
- Any new Task/Procedure/Process/Mission/Goal created from 2026-07-20
  onward must have its dates checked against this file before being
  written
- Claude must refuse to write a Friday date into any date field and
  should say so explicitly if asked to
- Applies to Phase Infinity scheduling (`strategist-track`/
  `ux-engineering-track`) exactly the same as Phase 0 — this file governs
  the whole merged repo, no phase is exempt
