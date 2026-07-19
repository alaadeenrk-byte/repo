---
type: procedure
id: EVIDENCE_GATHERING_VALIDATION
process: validation-strategy
owner: [alaaedeen, dazdaz]
status: pending
tasks_total: 5
tasks_done: 0
start_date:
completed_date:
meeting_date:
verified_by:
---

## Description
Evidence Gathering — defines the riskiest-assumption register, the MVP scope (sized to test the core hypothesis, not to comfort), the concierge test design using Souhibe's school as the manual-delivery site, and the success/kill criteria — all written down before the test runs.

## Requirements for Completion
- All child tasks below marked complete
- Completion meeting held to confirm success/kill criteria were genuinely set before the test started, not adjusted in hindsight, with `meeting_date` and `verified_by` filled in above
- Once all child tasks show `done`, Claude sends a Telegram notification to Alaaedeen (and Dazdaz) flagging that this procedure is ready for its closing meeting — using the notification channel logic already defined in `CLAUDE.md` (owner's connected channel, falling back to Deen's Telegram bot). This is a prompt to schedule the meeting, not a substitute for holding it — the procedure still only closes after the meeting actually happens and `meeting_date`/`verified_by` are filled in.

## Child Tasks
- [ ] riskiest-assumption-register — Riskiest assumption register (alaaedeen)
- [ ] mvp-scope-definition — MVP scope definition (alaaedeen)
- [ ] concierge-test-design — Concierge test design (dazdaz)
- [ ] success-metrics-pre-test — Success metrics defined pre-test (alaaedeen)
- [ ] kill-criteria-pre-test — Kill criteria defined pre-test (alaaedeen)

## Change Log
- Procedure created as part of Phase Infinity — Foundation mini SMART goal
