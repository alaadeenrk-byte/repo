---
type: task
id: T1
procedure_ref: PR1
owner: nadji
depends_on: []
blocks: [build-accept-reject-logic]
weight: 2
status: done
start_date: 2026-07-20
due_date: 2026-07-22
completed_date: 2026-07-22
points: null
---

## Description
Pre-registration inbox UI: list of incoming requests (new/under review/
accepted/rejected), with filtering and search.

## Scope Detail
- Table view: student name, requested course, request date, status
- Filter by status, text search by name/phone
- Default sort: most recent first
- Out of scope for this task: the accept/reject logic itself (next task)

## Definition of Done
- [x] UI renders correctly with test data
- [x] Filtering and search work without errors
- [x] Reviewed by Abdelaziz for data-structure compatibility

## Change Log
- 2026-07-20 (Mon) — Work started (nadji)
- 2026-07-22 (Wed) — Moved to under-review (Claude, automatic)
- 2026-07-22 (Wed) — Approved: done (alaaedeen)
