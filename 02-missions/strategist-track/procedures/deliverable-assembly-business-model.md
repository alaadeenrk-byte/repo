---
type: procedure
id: DELIVERABLE_ASSEMBLY_BUSINESS_MODEL
process: business-model-design
owner: [alaaedeen, dazdaz]
status: pending
tasks_total: 7
tasks_done: 0
start_date:
completed_date:
meeting_date:
verified_by:
---

## Description
Deliverable Assembly — takes the evidence produced upstream (revenue model, unit economics, pricing, GTM motion, 90-day hypothesis) and compiles it into the external-facing set: full business plan, one-page canvas, pricing strategy doc, GTM strategy doc, budget breakdown, and one-pager. Investor pitch deck is conditional — only built if fundraising is actually on the table.

## Requirements for Completion
- All child tasks below marked complete (pitch deck excluded from the count if fundraising isn't on the table — note that decision in the Change Log)
- Completion meeting held to review each compiled deliverable against the underlying evidence-gathering procedure, with `meeting_date` and `verified_by` filled in above
- Once all child tasks show `done`, Claude sends a Telegram notification to Alaaedeen (and Dazdaz) flagging that this procedure is ready for its closing meeting — using the notification channel logic already defined in `CLAUDE.md` (owner's connected channel, falling back to Deen's Telegram bot). This is a prompt to schedule the meeting, not a substitute for holding it — the procedure still only closes after the meeting actually happens and `meeting_date`/`verified_by` are filled in.

## Child Tasks
- [ ] compile-business-plan — Compile Full Business Plan (alaaedeen)
- [ ] compile-business-model-canvas — Compile Business Model Canvas (alaaedeen)
- [ ] compile-pricing-strategy-doc — Compile Pricing Strategy Document (dazdaz)
- [ ] compile-gtm-strategy-doc — Compile GTM Strategy Document (dazdaz)
- [ ] compile-budget-breakdown — Compile Budget Breakdown (dazdaz)
- [ ] compile-one-pager — Compile One-Pager (alaaedeen)
- [ ] compile-pitch-deck-conditional — Compile Investor Pitch Deck (CONDITIONAL) (alaaedeen)

## Change Log
- Procedure created as part of Phase Infinity — Foundation mini SMART goal
