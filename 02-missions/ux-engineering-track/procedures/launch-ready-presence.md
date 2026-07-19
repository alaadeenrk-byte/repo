---
type: procedure
id: LAUNCH_READY_PRESENCE
process: online-presence-build
owner: [alaaedeen, bilal, nadji, souhibe]
status: pending
tasks_total: 5
tasks_done: 0
start_date:
completed_date:
meeting_date:
verified_by:
---

## Description
Launch-Ready Presence — builds the landing page hierarchy (hero → problem → solution → social proof → CTA), pressure-tests it with an above-fold 5-second comprehension check, and lays the SEO/analytics groundwork (meta/OG/schema, GA4 + heatmaps + session recording) plus a waitlist hook with a real value exchange — all before the site actually goes live.

## Requirements for Completion
- All child tasks below marked complete
- Completion meeting held to review the 5-second test results and confirm SEO/analytics are actually instrumented, not just planned, before deployment, with `meeting_date` and `verified_by` filled in above
- Once all child tasks show `done`, Claude sends a Telegram notification to Alaaedeen (and Dazdaz) flagging that this procedure is ready for its closing meeting — using the notification channel logic already defined in `CLAUDE.md` (owner's connected channel, falling back to Deen's Telegram bot). This is a prompt to schedule the meeting, not a substitute for holding it — the procedure still only closes after the meeting actually happens and `meeting_date`/`verified_by` are filled in.

## Child Tasks
- [ ] landing-page-hierarchy — Landing page hierarchy (alaaedeen)
- [ ] above-fold-5sec-test — Above-fold 5-second comprehension test (bilal)
- [ ] seo-foundation — SEO foundation (nadji)
- [ ] analytics-stack — Analytics stack (nadji)
- [ ] waitlist-capture — Waitlist / pre-launch capture (souhibe)

## Change Log
- Procedure created as part of Phase Infinity — Foundation mini SMART goal
