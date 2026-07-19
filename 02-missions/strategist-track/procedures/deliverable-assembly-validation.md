---
type: procedure
id: DELIVERABLE_ASSEMBLY_VALIDATION
process: validation-strategy
owner: [alaaedeen]
status: pending
tasks_total: 1
tasks_done: 0
start_date:
completed_date:
meeting_date:
verified_by:
---

## Description
Deliverable Assembly — compiles the riskiest-assumption register, MVP scope, concierge test design, and pre-defined success/kill criteria from Evidence Gathering into a single Validation Plan that will actually be run against the concierge test.

## Requirements for Completion
- All child tasks below marked complete
- Completion meeting held to confirm the Validation Plan's success/kill criteria are locked and can't be quietly moved once the test starts, with `meeting_date` and `verified_by` filled in above
- Once all child tasks show `done`, Claude sends a Telegram notification to Alaaedeen (and Dazdaz) flagging that this procedure is ready for its closing meeting — using the notification channel logic already defined in `CLAUDE.md` (owner's connected channel, falling back to Deen's Telegram bot). This is a prompt to schedule the meeting, not a substitute for holding it — the procedure still only closes after the meeting actually happens and `meeting_date`/`verified_by` are filled in.

## Child Tasks
- [ ] compile-validation-plan — Compile Validation Plan (alaaedeen)

## Change Log
- Procedure created as part of Phase Infinity — Foundation mini SMART goal
