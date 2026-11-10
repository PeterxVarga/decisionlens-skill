# CASE-01 — OUTPUT-Y

# RAW EXECUTION

Case: CASE-01
Lane: [REDACTED]


## INITIAL USER CASE

# CASE-01 — QueuePilot

You are reviewing the information architecture of **QueuePilot**, a live B2B operations SaaS used by managers responsible for 8–40 physical locations.

Current primary navigation:

- Home
- Locations
- Jobs
- Customers
- Reports
- Settings

`Home` is a KPI dashboard:
- open jobs;
- jobs completed this week;
- revenue;
- average response time;
- location performance chart.

Observed product data from the last 90 days:

- 68% of returning sessions begin within 30 minutes of an operational alert.
- In those sessions, the first meaningful action is cross-location triage of overdue, unassigned, blocked, or failed jobs.
- 78% of escalations require comparing or acting across more than one location.
- Only 19% of returning sessions begin with a known location already in mind.
- Managers still use aggregate KPI reporting weekly, especially on Monday and month-end.
- `Jobs` currently defaults to one selected location and requires a location switcher to inspect another location.
- Users can act on a job directly once it is found.

The product team asks:

> Should `Home` remain a KPI dashboard, or should the default returning-user surface become a cross-location “Needs Attention” work queue? How should this affect the surrounding IA?

Review the product architecture. Do not design pixel-level UI and do not write code.


## ASSISTANT TURN 1

QueuePilot’s default returning-user surface should become a cross-location **Needs Attention** work queue. The current dashboard is useful, but it does not align with the dominant returning-session intent: alert-driven, multi-location operational triage.

The evidence is unusually clear:

- 68% of returning sessions start near an operational alert.
- The first meaningful action in those sessions is cross-location job triage.
- 78% of escalations span multiple locations.
- Only 19% begin with a known location.
- The existing Jobs experience starts from a single location, creating friction precisely where multi-location action is most common.

Make **Needs Attention** the default landing surface for returning managers, organized around actionable exceptions such as overdue, unassigned, blocked, and failed jobs. It should support comparing, filtering, prioritizing, and acting across locations without first choosing one. Location should be a filter and grouping dimension, not the initial scope constraint.

Keep KPI reporting, but reposition it as an intentional review destination rather than the primary operational entry point. “Home” can either become the Needs Attention queue or be renamed accordingly; the KPI dashboard should remain readily available as “Overview” or within Reports. Avoid treating it as merely a secondary widget within the queue, because its weekly and month-end use represents a distinct review mode.

The surrounding IA should separate these two jobs:

- **Needs Attention / Home:** cross-location exception triage and direct action.
- **Jobs:** the complete job-management workspace, defaulting to cross-location scope rather than one preselected location.
- **Locations:** location-specific operational context, performance, and drill-down.
- **Reports / Overview:** aggregate KPI review, trends, and scheduled-period analysis.
- **Customers** and **Settings:** remain utility destinations.

The key architectural change is that cross-location work becomes the product’s default operational model. A manager can still narrow into a location after identifying an issue, but the system should not make that location decision before the manager can see where intervention is needed.

One open product decision is whether the KPI dashboard should retain a top-level destination or live under Reports. Given its regular weekly use, retaining a prominent “Overview” destination is likely safer than burying it. Validate the transition by measuring time to first triage action, rate of location switching, multi-location issue resolution, and whether Monday/month-end KPI workflows remain easy to reach.
