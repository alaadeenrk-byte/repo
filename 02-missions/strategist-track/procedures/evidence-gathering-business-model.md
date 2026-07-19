---
type: procedure
id: EVIDENCE_GATHERING_BUSINESS_MODEL
process: business-model-design
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
Evidence Gathering — locks the actual model decisions before anything gets written up: subscription confirmed as the revenue model with rationale, the unit economics (CAC, LTV, payback, gross margin, scenarios), the 3-tier pricing architecture off the 100-150 DZD/student/month figure, the GTM motion (PLG/SLG/blended), and a falsifiable 90-day revenue hypothesis with kill criteria.

## Requirements for Completion
- All child tasks below marked complete
- Completion meeting held to stress-test the unit economics and pricing assumptions before they're compiled into external deliverables, with `meeting_date` and `verified_by` filled in above
- Once all child tasks show `done`, Claude sends a Telegram notification to Alaaedeen (and Dazdaz) flagging that this procedure is ready for its closing meeting — using the notification channel logic already defined in `CLAUDE.md` (owner's connected channel, falling back to Deen's Telegram bot). This is a prompt to schedule the meeting, not a substitute for holding it — the procedure still only closes after the meeting actually happens and `meeting_date`/`verified_by` are filled in.

## Child Tasks
- [ ] revenue-model-selection — Revenue model selection with rationale (dazdaz)
- [ ] unit-economics-model — Unit economics model (alaaedeen)
- [ ] pricing-architecture — Pricing architecture — 3-tier (dazdaz)
- [ ] gtm-motion-decision — GTM motion decision (dazdaz)
- [ ] revenue-hypothesis-90day — 90-day revenue hypothesis with kill criteria (alaaedeen)

## Change Log
- Procedure created as part of Phase Infinity — Foundation mini SMART goal
