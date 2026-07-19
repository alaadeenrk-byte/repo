---
type: reference
status: conceptual — not yet a finalized schema or tech spec
completeness: full detail, not condensed — this is the reference copy
---

# CourseLi — Full Product Architecture (15 Categories)

Multi-tenant SaaS CRM/ERP for Algerian in-person schools. No online payment
in this phase — enrollment via the platform is pre-registration only;
students/parents confirm and pay physically at the school. Every table in
the eventual schema must carry a `school_id` and be strictly isolated per
tenant — enforced at the data layer, not just app logic.

## 1. Reception
- Pre-registration inbox: incoming requests, statuses (new/under review/accepted/rejected), filter/search
- Accept/reject: accept creates confirmed enrollment + student file; reject requires a stored reason
- Automatic seat-availability check on accept (via Logistics)
- Walk-in registration (direct confirmed entry, no pre-registration step)
- Permanent student file, linked to parent if minor
- Manual first-payment logging (amount/method/date) — not a real payment gateway
- Group/schedule assignment, dependent on Logistics seat data
- Automatic notification trigger on accept/reject
- Limited permissions: no full financial reports, no management dashboard, no teacher data edits

## 2. Logistics
- Room management: name, capacity, type, status (available/maintenance/disabled)
- Group/class management: room + teacher + max capacity + current enrollment per group
- Scheduling with a conflict-detection engine (no double-booking room or teacher)
- Visual weekly calendar per room/teacher
- Teacher availability management, system suggests only compatible slots
- Equipment/resource management with conflict alerts
- Capacity overview dashboard for the manager (fill rate per course)
- Student transfer between groups, with automatic seat check before transfer

## 3. Finance
- Per-student ledger: full price, paid, remaining, itemized payment lines
- Installment plans with due dates and automatic reminders
- Overdue list, sorted by lateness
- Operating expense logging (rent, salaries, bills, equipment), fixed/variable tagged
- Teacher payroll (simplified): tied to teaching hours (Logistics) and student count (Reception)
- Refunds: percentage per policy and remaining duration, with stored withdrawal reason
- Basic financial reports: revenue over time, expenses vs. revenue, revenue by course
- **Technical note:** amounts must use integer cents, not floats, to avoid rounding errors

## 4. Management
- Dashboard/KPIs: new registrations, accept/reject rate, group fill rate, revenue, overdue — read-only
- Staff account management + granular permissions + activity log
- Course/program catalog: create, price, archive
- Approval authority: new group openings, price changes, large refunds
- School policies (refund policy, attendance policy) applied automatically by other categories
- Automatic periodic reports (weekly/monthly), exportable
- Multi-branch visibility (future-proofing, not active yet)

## 5. Notifications
- Centralized notification engine — single point other categories call, not duplicated per category
- Channels: SMS (most reliable locally), WhatsApp (rich interaction), email (lower priority)
- Editable templates matching school branding, in Arabic and French
- Automatic triggers per event, designed as extensible "events" so future categories can subscribe
- Delivery log: sent/failed/sending/not sent, automatic retry with a cap
- Preference separation: mandatory operational vs. optional marketing notifications
- Usage limits per package tier (cost control)

## 6. Certificates
- Automatic eligibility check: attendance minimum, assessment pass, full payment (ties to Finance)
- Generation with school-branded template, dynamic data, serial number, PDF output
- Serial number + QR/verification link for third-party checking — anti-forgery
- Permanent archive, partially independent of live student record (frozen snapshot at issuance)
- Reissue on loss, same serial number preserved
- Multiple certificate types: completion, distinction, participation
- Teacher/manager approves eligibility; reception prints/delivers only

## 7. Teacher
- Dashboard: weekly schedule (read-only), assigned groups
- Attendance/absence logging per session, historical record — feeds certificate eligibility
- Grading: numeric or complete/incomplete depending on course setup
- Certificate eligibility approval, with reason logged if not eligible
- Private notes per student, visible only to teacher + manager
- Schedule-change requests — teacher requests, manager approves (Logistics stays centralized)
- Parent communication via the existing notification engine, not a new channel
- Own-earnings view only, no other financial data

## 8. Student Portal (adult, direct login)
- Registration status tracking (from Reception)
- Schedule view (from Logistics)
- Attendance view, read-only (from Teacher)
- Financial status: total/paid/remaining, upcoming installments (from Finance)
- Certificate view/download + verification link (from Certificates)
- Personal notification history
- Direct account access, no intermediary
- Direct schedule-change/withdrawal requests, no parent required

## 9. Parent Portal (for minors — no independent student login)
Same read surface as Student Portal, plus:
- Link multiple children to one account
- Receive financial/attendance notifications on behalf of the minor
- Sole approval authority for withdrawal or major changes affecting the minor
- **Design rule:** a minor never has an independent login — all their interaction routes through the parent account. An adult student has their own independent account; a parent wanting to follow an adult child needs that child's explicit consent, not automatic access.

## 10. School Website
- Block-based template engine (not hardcoded per school) — sections toggle/reorder per school
- Branding applied from one config file per school (logo, name, colors, font)
- Course display pulled automatically from Management + Logistics — no manual entry
- Pre-registration form feeding directly into that school's Reception inbox
- Certificate verification page linked to Certificates category
- Flexible additional pages without hand-written HTML per school
- Automatic subdomain (school-name.courseli.app); custom domain as a later paid option (DNS+SSL — the hardest infra piece, deliberately deferred)
- Basic SEO: auto-generated titles/descriptions per course page

## 11. Global CourseLi Website
- Aggregation engine: pulls courses marked "public" from every participating school, near-real-time
- Search/filter: region, course type, age group, price — requires a unified tag taxonomy across schools' own internal naming
- Per-school profile page: summary + link to that school's own site — "storefront inside a marketplace"
- Ranking/recommendation: geographic proximity, rating, or paid promotion (business decision, not yet made) — natural future tie-in to the AI Data Analyst category
- Centralized certificate verification (one place works across all schools, instead of duplicating per school)
- Cross-school lead capture: a visitor who doesn't know which school to pick gets auto-routed by search criteria, lands in that specific school's Reception inbox like any other lead
- Marketing blog for platform-wide SEO

## 12. Marketing & Content (owned by Souhibe)
- Social media account linking via Meta Graph API — **access tokens live server-side only, never in client code**
- Periodic performance metrics pull (followers, engagement, reach), stored as a time series, not a snapshot
- The category's actual value: linking marketing activity timing to real enrollment/churn timing — without this link the social data is isolated and not actionable
- Scheduled report export (PDF/Excel) for content creators/marketers
- Ready-made content asset library matching each school's brand identity automatically
- UTM-tracked campaign links to know exactly which source produced which pre-registration

## 13. AI Data Analyst (owned by Nadji)
- Owns no data itself — reads and aggregates from every other category
- Data aggregation/cleaning layer — the actual hard/important step, before any AI analysis happens
- Operational trend analysis: accept/reject rate over time, peak request times, most/least requested courses
- Churn analysis: aggregate withdrawal/refund reasons to find repeat patterns
- Real financial performance: actual profitability per course/group (revenue minus attached costs), not raw revenue
- Marketing-to-outcome correlation, using UTM + timing data
- Generates written recommendations from **aggregated summaries only** — never raw student PII sent to any external AI API
- Automatic periodic insight report, layered on top of the Marketing export mechanism
- Platform-wide cross-school analysis restricted to the Platform/Super-Admin role only
- School managers see only their own school's analysis

## 14. AI Visitor Assistant (owned by Nadji)
- Per-school chat widget, answers only using that specific school's data (courses, prices, hours, enrollment conditions)
- Global marketplace assistant, recommends across all schools, layered on top of the Global Website's search engine
- Strict data isolation: a per-school assistant must never access another school's data even if directly asked
- Primary commercial goal: convert conversation into an actual pre-registration submission, not just answer questions
- Auto-generated FAQ answers sourced directly from Management/Logistics data, no manual FAQ maintenance
- Conversation log (no PII where avoidable), feeding back into AI Data Analyst
- Usage cap per school per package tier (real per-call cost)

## 15. Platform (Super-Admin — CourseLi's own team only)
- Tenant management: add/suspend a school, automatic subdomain, first manager account
- Subscription/package management and billing to CourseLi itself (this is the one place real payment processing exists — CourseLi charging schools, not schools charging students)
- Custom domain management (DNS verification + SSL) — hardest infra piece in the whole system
- System health monitoring across all schools
- Support ticketing channel with schools
- Template/feature rollout control across all tenants
- Compliance: data export policy on school departure, mandatory access-audit logging any time Platform staff touch a specific school's data
- Cross-school aggregate analytics, feeding platform growth strategy

## Cross-Cutting Rules (apply to all 15 categories)
1. Tenant isolation (`school_id` on every table) enforced at the data layer
2. No online payment processing anywhere except Platform↔School billing (category 15)
3. All external AI API calls happen server-side only — no client-embedded keys, ever
4. Minors never get independent logins — always routed through a parent account
5. A per-school AI assistant's data isolation from other schools is non-negotiable, same standard as the backend itself

## Relationship to the Granular Draft
`01-product/feature-spec-draft.md` implements pieces of categories 1-5 above
(Reception, Logistics, Finance, Management, Notifications, plus the
Teacher/Marketing/Sales-facing surfaces) at a much more granular,
MVP-feature level of detail, organized by staff role rather than by
category. Categories 8-15 (student/parent portals, both websites, AI) are
not yet represented in that granular draft — they exist only at this
architectural level until someone writes the equivalent staff-role-style
breakdown for them.
