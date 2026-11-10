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