---
type: reference
---

# CourseLi — Project History / Evolution Trail

For traceability — how the project got from a single-school demo template
to the current 15-category multi-tenant architecture.

## 1. Original Demo Template (courseli-website.zip)
Vanilla HTML/CSS/JS, localStorage as the database, no backend. Public site
(6 pages, French): Accueil, Formations, course detail, Carrières, À propos,
Contact. Admin panel (8 pages) including a director-only AI analytics
assistant. Floating AI chat widget on OpenRouter's free tier, API key
embedded client-side — an explicitly accepted demo-only tradeoff, not
carried into the real architecture (server-side-only API keys is now a
hard rule, see `01-product/architecture-overview.md` cross-cutting rules).

Deep audit found and fixed: frozen seed dates, UTC/local timezone mismatch
in date helpers, course numbering using array index instead of real IDs,
unescaped public AI link rendering (fixed with an escape-first,
allowlist-promote approach), missing per-course breakdowns in director AI.
One bug flagged but not fixed at the time: `addEnrollment`/`addJob`/
`addJobApplication`/`addTutorApplication` still used UTC-based dates
(`toISOString()`) inconsistently with the corrected local-date helper —
worth checking this is actually fixed if any of that original code is
reused.

One further finding not fixed: unescaped comment rendering on the public
course page (stored XSS risk if ever backed by a shared database instead of
local-only storage) — same class of risk the AI widget already handles
correctly elsewhere in that codebase.

## 2. The Pivot — Single Template to Multi-Tenant SaaS
Realization: CourseLi shouldn't be a one-off site per client, but one
platform serving many schools, each with an auto-generated branded site,
feeding into a shared global marketplace site. This is what forced the
architecture to become genuinely multi-tenant (`school_id` isolation
everywhere) rather than a per-client build.

## 3. Category Definition (→ 01-product/architecture-overview.md)
Iteratively built from "enrollment, certificates, reception, finance,
logistics, roles, AI" up to the full 15-category structure, splitting
Student/Parent into separate roles, adding Notifications, Certificates, and
the AI Visitor Assistant as their own categories.

## 4. Team & Governance (→ organigram.md, reference-team-protocol-full.md)
Org chart evolved through several iterations (a mistake was caught and
fixed once — Souhibe was dropped from a diagram redraw without intent).
Landed on dual authority (Alaaedeen: product/tech, Dazdaz: operations/
external) with mandatory peer review, Souhibe elevated from advisor to full
Head of Marketing & Content domain authority, and a full points/equity
protocol designed but deliberately not yet activated.

## 5. GitHub Architecture (→ SYSTEM.md, this repo's structure)
Settled on: one file per mission/process/procedure/task (not just GitHub
Issues), a strict human-only approval gate for closing anything, and a
3-repo split once the "GitHub permissions are repo-wide, not folder-wide"
constraint became unavoidable (first for `courseli-platform`, later for
`courseli-agency-os`). **Later reversed (2026-07-18):** the Phase Infinity
split was merged back into this repo by explicit decision, with Souhibe
gaining full access to it — see `README.md` and `reference-team-protocol-full.md`.
`courseli-platform` remains the one standing repo split.

## 6. Agency OS / Phase ∞ (→ merged into this repo as of 2026-07-18)
CourseLi treated as its own first client under the team's own Agency
Operating System consulting methodology, starting with the Foundation phase
(Strategist + UX Engineering tracks), running in parallel to — and
currently gating — the Phase 0 MVP build.

## Current State (as of this file's creation)
Phase 0 MVP work is intentionally on hold. Phase ∞ Foundation validation is
the active work — its outcome determines whether Phase 0 resumes.
