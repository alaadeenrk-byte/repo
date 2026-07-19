---
type: task
id: T4
procedure_ref: PR2
owner: nadji
depends_on: []
blocks: []
weight: 2
status: done
start_date: 2026-07-27
due_date: 2026-07-28
completed_date: 2026-07-28
points: null
---

## Description
Reception-facing form for direct walk-in registration: same seat-availability
check as the pre-registration path (reuses the check built in
link-seat-check-to-logistics), but skips the accept/reject step since the
student is already physically present and confirmed.

## Definition of Done
- [ ] Form creates a confirmed student record directly, no "pending" state
- [ ] Reuses the existing seat-availability check, not a duplicate implementation
- [ ] Reviewed by Abdelaziz for consistency with the pre-registration flow's data structure

## Change Log
- 2026-07-27 (Mon) — Work started (nadji)
- 2026-07-28 (Tue) — Approved: done (alaaedeen)
