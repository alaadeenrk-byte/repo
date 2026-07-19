---
type: procedure
id: CARRY_FORWARD_BRAND
process: brand-architecture
owner: [alaaedeen, souhibe]
status: pending
tasks_total: 3
tasks_done: 0
start_date:
completed_date:
meeting_date:
verified_by:
---

## Description
Carry-Forward Registration — logs the already-finished `CourseLi-brand-identity.html` work (naming rationale, positioning elements, tone signals) into the internal database as evidence, then writes down two artifacts that were implicit but never made explicit: the positioning statement and the tone-of-voice pillars. No new brand design, just formalizing what already exists.

## Requirements for Completion
- All child tasks below marked complete
- Completion meeting held to confirm the registered evidence, positioning statement, and tone pillars are consistent with the existing brand identity doc, with `meeting_date` and `verified_by` filled in above
- Once all child tasks show `done`, Claude sends a Telegram notification to Alaaedeen (and Dazdaz) flagging that this procedure is ready for its closing meeting — using the notification channel logic already defined in `CLAUDE.md` (owner's connected channel, falling back to Deen's Telegram bot). This is a prompt to schedule the meeting, not a substitute for holding it — the procedure still only closes after the meeting actually happens and `meeting_date`/`verified_by` are filled in.

## Child Tasks
- [ ] register-existing-brand-work — Register CourseLi-brand-identity.html as evidence (alaaedeen)
- [ ] formalize-positioning-statement — Formalize brand positioning statement (alaaedeen)
- [ ] formalize-tone-of-voice — Formalize tone of voice system (souhibe)

## Change Log
- Procedure created as part of Phase Infinity — Foundation mini SMART goal
