---
type: procedure
id: EVIDENCE_GATHERING_DISCOVERY
process: discovery-intelligence
owner: [alaaedeen, bilal, dazdaz]
status: pending
tasks_total: 5
tasks_done: 0
start_date:
completed_date:
meeting_date:
verified_by:
---

## Description
Evidence Gathering — collects the raw inputs the Feasibility Study will be built on: the founder interview, Algeria-specific TAM/SAM/SOM, competitor audit (positioning, pricing, SWOT), JTBD research sourced from Souhibe's network, and a pain-point hierarchy ranked by frequency × severity × willingness to pay.

## Requirements for Completion
- All child tasks below marked complete
- Completion meeting held to check the evidence is actually sourced from real conversations/data, not assumed, before it's compiled, with `meeting_date` and `verified_by` filled in above
- Once all child tasks show `done`, Claude sends a Telegram notification to Alaaedeen (and Dazdaz) flagging that this procedure is ready for its closing meeting — using the notification channel logic already defined in `CLAUDE.md` (owner's connected channel, falling back to Deen's Telegram bot). This is a prompt to schedule the meeting, not a substitute for holding it — the procedure still only closes after the meeting actually happens and `meeting_date`/`verified_by` are filled in.

## Child Tasks
- [ ] founder-interview-synthesis — Deep founder interview (alaaedeen)
- [ ] market-sizing-tam-sam-som — Market sizing (TAM/SAM/SOM), Algeria-specific (alaaedeen)
- [ ] competitor-audit — Competitor audit — positioning, pricing, SWOT (bilal)
- [ ] jtbd-research — JTBD customer archetype research (dazdaz)
- [ ] pain-point-hierarchy — Pain point hierarchy (alaaedeen)

## Change Log
- Procedure created as part of Phase Infinity — Foundation mini SMART goal
