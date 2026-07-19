---
type: reference
status: draft — not final, items to be added as gaps are found
source: courseli-tasnif-results.md + قائمة_خصائص_وأدوار_النظام_المدرسي.pdf (identical content, two exports of the same sheet)
---

# CourseLi — Granular Feature Draft (Staff-Facing CRM)

This is a **draft**, explicitly not final — items get added as gaps are
found. It currently covers only internal staff-facing operations (no
student/parent portal, no school website, no global marketplace, no AI
categories — those live in `architecture-overview.md` and are tracked
separately). ID prefixes: SHR (shared), GR/MGR (manager), TCH (teacher),
REC (receptionist), MKT (marketing), SAL (sales).

## Shared — Task Management (all 5 roles)
- SHR-001: Personal task schedule per employee — title, details, owner,
  priority, deadline, status *(MVP)*
- SHR-002: Task creator must set a deadline + clear details before assigning *(MVP)*
- SHR-003: Task states — not started, in progress, completed, cancelled, archived *(MVP)*
- SHR-004: Comments, progress updates, attachments, completion notes on tasks *(MVP)*
- SHR-005: Notifications on new assignment, deadline approaching, deadline passed
- SHR-006: Per-user count of completed/in-progress/not-started/overdue tasks *(MVP)*
- SHR-007: Manager can filter tasks by employee, department, status, priority, deadline *(MVP)*

## Shared — AI Chat & Message-to-Task
- SHR-008: Internal AI chat available to all authorized school accounts
- SHR-009: Converts natural-language messages into structured tasks
- SHR-010: Assign a task to one employee, multiple employees, or a whole department
- SHR-011: Stores original message, resulting task, sender, creation date, status history
- SHR-012: AI used to generate lesson summaries, payment messages, absence messages,
  brand guide content, and marketing content

## School Manager — Overview Dashboard
- MGR-001: Total active students *(MVP)*
- MGR-002: New students registered this month *(MVP)*
- MGR-003: Students who stopped, with date/reason when available *(MVP)*
- MGR-004: Each group as a card — student count, teacher, schedule, status *(MVP)*
- MGR-005: Revenue generated per group *(MVP)*
- MGR-006: Total revenue collected this month *(MVP)*
- MGR-007: Net income after expenses and teacher payments *(MVP)*
- MGR-008: Urgent alerts — unpaid subscriptions, repeated absence, overdue tasks,
  schedule conflicts *(MVP)*

## School Manager — Finance & Teacher Payroll
- MGR-009: View student payments, remaining balances, receipts, upcoming due dates *(MVP)*
- MGR-010: Choose teacher payment method — percentage or hourly *(MVP)*
- MGR-011: Set teacher percentage and which revenue it applies to *(MVP)*
- MGR-012: Set hourly rate, calculate from completed teaching hours *(MVP)*
- MGR-013: Review teacher earnings per group and total amount due *(MVP)*
- MGR-014: Confirm teacher salary payment — date, amount, method, confirmed-by *(MVP)*
- MGR-015: Log school expenses and calculate net profit *(MVP)*
- MGR-016: Track SMS usage/cost by school, message type, period *(MVP)*

## School Manager — Staff, Tasks & Performance
- MGR-017: Create/manage accounts for teachers, receptionists, marketing/sales *(MVP)*
- MGR-018: View all employee tasks, deadlines, statuses, completion indicators *(MVP)*
- MGR-019: View staff/department productivity *(MVP)*
- MGR-020: Use AI chat to create and assign tasks *(MVP)*
- MGR-021: Review marketing metrics, funnel activity, leads, campaigns, conversions *(MVP)*
- MGR-022: Review sales pipeline — follow-ups, visits, trial classes, registrations *(MVP)*

## School Manager — Schedule & Permissions
- MGR-023: View schedule by teacher, group, or room
- MGR-024: Create, edit, cancel, or reschedule sessions *(MVP)*
- MGR-025: Prevent double-booking a teacher, group, or room at the same time *(MVP)*
- MGR-026: Create recurring schedules, keep a change history *(MVP)*
- MGR-027: Define what reception/marketing staff can view or edit on the schedule *(MVP)*

## Teacher — Groups & Lessons
- TCH-001: Assigned groups shown as cards/buttons
- TCH-002: Student count, schedule, room, last lesson per group
- TCH-003: Log the lesson delivered after each session *(MVP)*
- TCH-004: Dated lesson history per group *(MVP)*
- TCH-005: AI-generated short SMS lesson summary for parents *(MVP)*
- TCH-006: Count of sessions delivered per group and total

## Teacher — Student Tracking & Internal Notes
- TCH-007: Open the student list for each assigned group
- TCH-008: Write internal notes on each student
- TCH-009: Store note author, date, and history in the student's file
- TCH-010: View attendance history for own groups' students

## Teacher — Assignments
- TCH-011: Create an assignment for a specific group
- TCH-012: Attach files, images, links, exercises, or documents
- TCH-013: Send the assignment to all students in the selected group
- TCH-014: Keep assignment history, allow edit/cancel before deadline
- TCH-015: Track whether students viewed/submitted, when enabled

## Teacher — Earnings, Schedule & Tasks
- TCH-016: View estimated earnings by group and in total *(MVP)*
- TCH-017: View personal schedule and upcoming sessions *(MVP)*
- TCH-018: Personal task schedule with mandatory deadline/status fields *(MVP)*
- TCH-019: Count of assigned and completed tasks
- TCH-020: Use AI chat to create/assign tasks to authorized colleagues

## Receptionist — Groups & Students
- REC-001: Each group as a card — schedule, teacher, student count *(MVP)*
- REC-002: Open a group's student list — name, payment status, attendance, notes *(MVP)*
- REC-003: Add a new student directly into a selected group *(MVP)*
- REC-004: Move a student from one group to another *(MVP)*
- REC-005: Search by student name/phone, filter by payment or attendance *(MVP)*
- REC-006: Add reception-specific notes to a student's file *(MVP)*

## Receptionist — Attendance & Absence Alerts
- REC-007: Mark student present, absent, or late per session *(MVP)*
- REC-008: Keep an attendance record per student/group *(MVP)*
- REC-009: Detect repeated absence based on a school-defined threshold *(MVP)*
- REC-010: Show an urgent red alert when the absence threshold is hit *(MVP)*
- REC-011: Auto-draft an SMS to the parent after repeated absence *(MVP)*
- REC-012: Create a new alert if absence continues after the previous message *(MVP)*

## Receptionist — Payments, Receipts & Renewal
- REC-013: Set subscription status — paid or unpaid *(MVP)*
- REC-014: Show total paid, remaining balance, next due date *(MVP)*
- REC-015: Issue a payment receipt after each transaction *(MVP)*
- REC-016: Preview, print, export, and send the receipt as PDF *(MVP)*
- REC-017: Keep a searchable, reprintable payment/receipt history *(MVP)*
- REC-018: Detect subscription or session-count expiry *(MVP)*
- REC-019: Show an urgent red renewal alert one day after expiry *(MVP)*
- REC-020: Select all or specific students before sending renewal messages *(MVP)*

## Receptionist — SMS & Alerts
- REC-021: Send messages to one parent, selected parents, a whole group,
  teachers, or everyone linked to a session *(MVP)*
- REC-022: Send instant absence/lateness messages *(MVP)*
- REC-023: Send payment reminders before and after due date
- REC-024: Send messages on schedule change, postponement, or cancellation *(MVP)*
- REC-025: Send exam/results messages
- REC-026: Editable SMS templates in Arabic and French *(MVP)*
- REC-027: Track message status — sent, failed, sending, not sent *(MVP)*
- REC-028: Prevent accidental duplicate sends, allow resending failed messages *(final project)*
- REC-029: Show SMS usage, cost, and low-balance alerts *(final project)*

## Receptionist — Certificates & Level Testing
- REC-030: Generate a certificate for one student *(MVP)*
- REC-031: Generate certificates for a whole group at once *(final project)*
- REC-032: Save certificate history in each student's file
- REC-033: Launch a level-placement test via link or access code
- REC-034: Auto-grade objective questions and assign level (1 to C2)
- REC-035: Save and issue the level result without teacher involvement

## Receptionist — Leads & Follow-up
- REC-036: Access the list of shared leads coming from landing pages
- REC-037: Log calls, notes, next follow-up date, visits, trial-class progress
- REC-038: View/manage schedule by teacher, group, or room when permitted *(MVP)*
- REC-039: Edit teacher percentages/hourly rates when permitted
- REC-040: Open the school's brand and communication guide via a dedicated button *(MVP)*
- REC-041: Use the personal task page and AI chat, with mandatory details/deadline

## Marketing Team — Performance & Funnel
- MKT-001: Marketing performance indicators shown immediately at login *(MVP)*
- MKT-002: Registered students vs. leads who haven't registered yet *(MVP)*
- MKT-003: Lead count, conversion rate, campaign performance, progress toward goals *(MVP)*
- MKT-004: Set, edit, and approve marketing indicators and goals *(MVP)*
- MKT-005: Separate sections for top/middle/bottom of funnel *(MVP)*
- MKT-006: Add ideas/actions under each funnel stage *(MVP)*
- MKT-007: Set idea status — not started, in progress, completed *(MVP)*
- MKT-008: Convert approved funnel ideas into tasks automatically *(MVP)*
- MKT-009: Assign funnel tasks to team members, keep unassigned ideas visible *(MVP)*
- MKT-010: Measure funnel activity impact on leads and registrations *(MVP)*

## Marketing Team — Ideas, Lead Magnets & Group Launches
- MKT-011: Marketing idea database + marketing plans page
- MKT-012: Space for upsell/cross-sell ideas
- MKT-013: Page for planning/creating lead magnets
- MKT-014: Link lead magnets/campaigns to the leads they generate *(MVP)*
- MKT-015: Alert marketing when new-student numbers signal a new group is needed *(MVP)*
- MKT-016: Auto-create a task to launch a new group — level, language, current
  students, target count, expected start date *(MVP)*

## Marketing Team — Brand Guide Assistant & Content
- MKT-017: AI assistant that builds the brand guide through structured questions
- MKT-018: Progressively refine the brand guide through ongoing AI collaboration
- MKT-019: Upload and analyze existing brand guides, logos, images, references
- MKT-020: Generate/update the receptionist's communication guide from the brand guide
- MKT-021: Publish brand guide updates, notify reception staff of changed guidelines
- MKT-022: Create posts, ads, campaigns, content ideas matching the brand *(MVP)*
- MKT-023: Generate poster/design ideas using uploaded school logos *(MVP)*
- MKT-024: Upload photos for AI editing/enhancement *(MVP)*
- MKT-025: Monthly content calendar with weekly view *(MVP)*
- MKT-026: Include Algeria-specific events/dates in the calendar *(MVP)*
- MKT-027: Require shoot/production date when scheduling content *(MVP)*
- MKT-028: Convert content calendar items to assigned tasks and back *(MVP)*
- MKT-029: View the school schedule to spot classes/groups/enrollment opportunities *(MVP)*
- MKT-030: Use personal/team task pages and AI chat *(MVP)*

## Sales Team — Lead Intake & Assignment
- SAL-001: Automatically receive leads from landing page forms
- SAL-002: Import leads from Facebook/Meta forms when integration is available *(MVP)*
- SAL-003: Share the lead list with reception per permissions *(MVP)*
- SAL-004: Assign each lead to a sales rep or receptionist *(final project)*

## Sales Team — Pipeline, Calls & Follow-up
- SAL-005: Manage lead stages — new, not contacted, attempted, contacted,
  follow-up, interested, trial visit, registration pending, etc.
- SAL-006: Record whether the lead gave only a phone number or visited the school
- SAL-007: Log call outcome, notes, and interest level after each contact
- SAL-008: Schedule the next call, surface due/overdue follow-ups
- SAL-009: Log the reason for rejection or disinterest

## Sales Team — Trial Classes & Conversion
- SAL-010: Log whether the lead attended a trial class
- SAL-011: Track the first trial session *(MVP)*
- SAL-012: Notify sales and reception when trial sessions are completed *(MVP)*
- SAL-013: Log trial results, notes, and whether registration followed *(MVP)*
- SAL-014: Track the full lead journey from phone number to registration or close *(MVP)*

## Sales Team — Tasks & AI Chat
- SAL-015: Personal task page with mandatory details and deadline *(MVP)*
- SAL-016: View assigned, in-progress, not-started, and completed task counts *(MVP)*
- SAL-017: Use AI chat to convert written messages into assigned tasks *(MVP)*

## Open Question Carried From Prior Discussion
Sales (SAL-*) is a distinct role from Marketing (MKT-*) in this draft, with
its own pipeline. Not yet resolved: does this represent Dazdaz himself
(sales is part of his Operations & External Lead role), or a future hire
with no current owner? Flagged in `organigram.md` — resolve before treating
SAL-* tasks as assignable to a specific person.
