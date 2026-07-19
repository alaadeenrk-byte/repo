---
type: task
id: T2
procedure_ref: PR1
owner: nadji
depends_on: [build-preregistration-inbox]
blocks: [link-seat-check-to-logistics]
weight: 2
status: done
start_date: 2026-07-22
due_date: 2026-07-25
completed_date: 2026-07-25
points: null
---

## Description
Accept/reject logic for pre-registration requests, including rejection reason capture.

## Definition of Done
- [ ] Accept transitions request to confirmed status
- [ ] Reject requires a reason, stored for later analysis
- [ ] Reviewed by Abdelaziz for data-structure compatibility

## Change Log
- 2026-07-22 (Wed) — Work started (nadji)
- 2026-07-25 (Sat) — Completed. Note: due date spans Wed→Sat because Friday
  (2026-07-24) is a non-working day per reference-working-calendar.md, not
  because the task took longer than planned.
