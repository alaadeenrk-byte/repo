---
type: process
id: DISCOVERY_INTELLIGENCE
mission: strategist-track
owner: [alaaedeen, bilal, dazdaz]
status: pending
procedures_total: 2
procedures_done: 0
start_date:
completed_date:
meeting_date:
verified_by:
---

## Description
Discovery & Intelligence — first step in the Strategist track. Builds the evidence base for whether CourseLi is worth building at all: founder interview, Algeria-specific TAM/SAM/SOM, competitor audit (positioning, pricing, SWOT), JTBD research pulled from Souhibe's existing conversations and network, and a pain-point hierarchy ranked by frequency × severity × willingness to pay. This evidence is what everything downstream — business model, validation strategy — gets checked against, so it has to be gathered before it's compiled.

## Requirements for Completion
- All child procedures below marked complete (evidence-gathering-discovery, deliverable-assembly-discovery)
- Completion meeting held to review the compiled Feasibility Study against the raw evidence, with `meeting_date` and `verified_by` filled in above
- Once all child procedures show `done`, Claude sends a Telegram notification to Alaaedeen (and Dazdaz) flagging that this process is ready for its closing meeting — using the notification channel logic already defined in `CLAUDE.md` (owner's connected channel, falling back to Deen's Telegram bot). This is a prompt to schedule the meeting, not a substitute for holding it — the process still only closes after the meeting actually happens and `meeting_date`/`verified_by` are filled in.

## Child Procedures
- [ ] evidence-gathering-discovery — Evidence Gathering
- [ ] deliverable-assembly-discovery — Deliverable Assembly

## Change Log
- Process created as part of Phase Infinity — Foundation mini SMART goal
