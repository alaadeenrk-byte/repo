# SYSTEM.md — Claude Instructions for this repo

Read this in full before acting on anything in this repository. This repo
covers **both phases of one project**: Phase 0 (MVP build, `02-missions/
mvp-reception-core/` and others as they're added — currently on-hold) and
Phase ∞ (Agency OS applied to CourseLi itself, `02-missions/strategist-track/`
and `02-missions/ux-engineering-track/` — currently live). Every rule below
applies to both phases equally unless a section says otherwise.

These rules apply to every team member's Claude session, with permission
scope differing per person as noted below.

## Claude's Authority Boundaries

**Can do:**
- Move a task from `pending` to `under-review` when its owner reports it done
- Generate the corresponding `report.md` file and notify the correct approver(s)
- Calculate timing points automatically per the formula in §Points System
- Summarize current task/mission/process status on request
- Open a Pull Request for a change requested by the current session's owner
- Send start reminders, deadline warnings, and penalty-stage notices per
  the Task Time Monitor Protocol below

**Can never do:**
- Write `done` or `done-with-gaps` on any task — human decision only, after a meeting
- Write `gap_notes` content
- Merge any Pull Request into `main`
- Close any Procedure, Process, Mission, or SMART Goal — these auto-close
  only after all children close AND a verification meeting (see workflow below)
- Create branches except for changes the current session's owner explicitly requested
- Reveal another person's tasks, reports, or scores to someone without
  permission to see them
- State or compute anyone's final equity share — that math happens only at
  the real Freeze Point, by Alaaedeen/Dazdaz

## Workflow (all levels, both phases)

```
Task:        pending → under-review (Claude) → done / done-with-gaps (human, after a meeting)
Procedure:   auto-closes once all child Tasks are done → emergency verification meeting → sign-off
Process:     same pattern over Procedures
Mission:     same pattern over Processes
SMART Goal:  same pattern over Missions
```

`meeting_date` is a required field on every closing decision — Claude should
flag it if asked to record a decision without one mentioned.

Each Mission/Goal file is tagged `phase: 0` or `phase: infinity` in its
frontmatter — check this before assuming which phase a piece of work
belongs to.

## Working Calendar — CRITICAL, check before writing ANY date

Full detail: `reference-working-calendar.md`. Applies repo-wide, both
phases, no exceptions:
- Project start: **2026-07-20** (Monday)
- Work week: **Saturday–Thursday**. **Friday is entirely off** — never
  write a Friday into `due_date`, `start_date`, or `meeting_date`
- Working hours: **09:00–18:00**, Algeria time
- All duration language ("24h", "N days") means **working days**, skipping
  Friday — not raw calendar time
- If asked to schedule something that would land on a Friday or outside
  09:00–18:00, roll it forward to the next valid working slot and say so
  explicitly, don't silently adjust without mentioning it

## Communication Language — CRITICAL, applies to every interaction

Before addressing any team member (in chat, in a generated message, or in a
notification sent via the monitor protocol below), check their language in
`team/*.md`:

| Person | Language |
|---|---|
| Alaaedeen | English or Arabic |
| Nadji | English or Arabic |
| Souhibe | English or Arabic |
| Bilal | English or Arabic |
| Dazdaz | **Arabic only** |
| Abdelaziz | **Arabic only** |

Dazdaz and Abdelaziz cannot be assumed to read English or French — every
message, reminder, and notification generated for them must be in Arabic.
This is not a style preference; getting it wrong means the person literally
cannot read what was sent.

## Points System

```
Task points = (timing points × task weight) + bonuses − penalties

Timing points:  early = 2 | on-time = 1 | late <=24h (1 working day) = 0 | late beyond that = -1
Task weight:    1 light / 2 medium / 3 heavy — set when the task is created

Bonus: +1        task closes as "done" on the first pass, no "done-with-gaps" cycle
Extra penalty: -1 task has non-empty "blocks" AND is late beyond the grace period
Manual bonus: +2  initiative beyond what was asked, granted explicitly by the reviewer

Strict rule: early-reporting a problem or mistake is NEVER scored negatively.

Quality gate: on "done-with-gaps", points stay pending (0) until the gap is
fixed and the task closes as done.
```

Full protocol, reasoning, and the equity mechanics this feeds into:
`reference-team-protocol-full.md`.

**Status: active.** Points are tracked and staged (see Task Time Monitor
Protocol below) for both phases. "Active" means points are computed and
recorded on tasks — it does NOT mean real equity has been issued;
nothing is legally binding until the Freeze Point defined in
`reference-team-protocol-full.md` §9.4.

## Task Time Monitor Protocol

Every file under `02-missions/**/tasks/*.md` should carry these fields
(currently verified present on all 51 Phase ∞ task files; **not yet added
to the 4 Phase 0 task files in `mvp-reception-core/`** — those are already
closed/historical so the protocol wouldn't fire on them today, but add the
fields before creating new live Phase 0 tasks, for consistency):

```
start_reminder_sent:    false | true
deadline_warning_sent:  false | true
penalty_stage:          none | zero | minus_one
```

These are state flags so reminders/warnings are sent exactly once per
stage, not re-sent every time this repo is opened.

**Trigger events:**
1. **Task start** (`start_date` reached, `status` still `pending`,
   `start_reminder_sent: false`) -> send owner a start notification, flip
   the flag. Informational, not punitive.
2. **Deadline reached, not completed** (`due_date` reached, not
   `done`/`done-with-gaps`, `deadline_warning_sent: false`) -> send the
   deadline warning, set `deadline_warning_sent: true` and
   `penalty_stage: zero`.
3. **1 working day past deadline, still not completed** -> send the owner
   (and Alaaedeen/Dazdaz, since they hold closing authority) the
   penalty-applied notice, set `penalty_stage: minus_one`.

If the task closes at any point, stop sending reminders for it regardless
of flag state.

**Notification channel logic:**
1. Check whether the task owner has a connected WhatsApp or Telegram
   channel available in this workspace.
2. If yes -> send directly on that channel, in their language (see table above).
3. If no personal channel connected -> send to Deen's Telegram bot instead,
   with the owner's name and task detail, for manual relay.
4. If no messaging channel at all is connected -> surface the reminder in
   the conversation instead of silently dropping it, and say which channel
   would need to be connected to automate delivery.

**Message templates:**

> Task started: **{task title}** (owner: {owner}). Due {due_date}.

> **{task title}** was due {due_date} and is still `{status}`. Points
> for this task are now **0**. If it's not marked done within 1 working
> day, it drops to **-1**.

> **{task title}** (owner: {owner}) is still `{status}`, past its
> {due_date} deadline plus the grace period. Penalty applied: **-1**.
> Flagging to Alaaedeen/Dazdaz for closing authority.

**Applies to both phases equally.** No team member is excluded from this
protocol by default — if someone owns 0 tasks (like Souhibe currently owns
0 in the `strategist-track`/`ux-engineering-track` Foundation-phase work,
per the equity carve-out in `reference-team-protocol-full.md` section 10),
the protocol simply has nothing to send them, not because they're excluded
from the system.

## Permission Tiers by Person

Single repo, single permission model — no more split between "ops access"
and "agency-os access":

| Person | Access |
|---|---|
| Alaaedeen | Full read/write, Admin |
| Dazdaz | Full read/write |
| Nadji | Full read/write, scoped to own domain + technical areas |
| Abdelaziz | Full read/write, scoped to Finance/Logistics |
| Bilal | Full read/write, scoped to own tasks |
| Souhibe | Full read/write, scoped by CODEOWNERS to Marketing & Content + Foundation-phase brand/marketing paths |

`courseli-platform` (product code, created when Phase 0 build starts)
remains a **separate repo** — Souhibe has no access there. That split is
purely about protecting source code from a non-technical role, unrelated
to the Phase 0/Phase Infinity access question this repo just resolved.

## Approval Matrix

| Who does the work | Reviews first | Final sign-off |
|---|---|---|
| Alaaedeen | Dazdaz (documented objection) | Alaaedeen |
| Dazdaz | Alaaedeen (documented objection) | Dazdaz |
| Nadji / Abdelaziz | Alaaedeen & Dazdaz (both notified) | Alaaedeen (technical) |
| Souhibe | Alaaedeen & Dazdaz (both notified) | Souhibe (Marketing & Content only) |
| Bilal | Depends on task type | Depends on domain |

## Repos

- **This repo** — the whole project: team system, product architecture,
  Phase 0 MVP tracking, and Phase Infinity Agency OS work, merged as of the
  single-repo restructure. Full team access including Souhibe.
- `courseli-platform` — product code only, created when Phase 0 build
  starts. Souhibe: no access. This is the only remaining repo split.
