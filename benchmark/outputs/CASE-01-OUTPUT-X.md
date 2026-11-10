# CASE-01 — OUTPUT-X

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

Make **Needs Attention** the default returning-user surface. The observed behavior is operational triage, not KPI consumption: alerts trigger most sessions, and most escalations span multiple locations. Sending those users first to a dashboard adds a navigation step before the job they came to do.

Recommended primary navigation:

- Needs Attention
- Jobs
- Locations
- Customers
- Reports
- Settings

“Home” should be retired as the primary label. If needed, preserve its KPI dashboard as a **Performance overview** within Reports or as a secondary tab from Needs Attention—not as the default landing surface.

Needs Attention should be a cross-location queue for overdue, unassigned, blocked, and failed jobs, with location shown on every row and filters that retain a multi-location scope by default. A manager should be able to compare, assign, escalate, and resolve directly from this queue. Do not make users choose a location before seeing urgent work.

Jobs should become the complete operational inventory: default to all locations, support saved views, and allow narrowing to a location when the manager has one in mind. The current one-location default conflicts with the cross-location nature of escalation work.

Locations remains the place for location-specific context: staffing, health, performance, and its jobs—but it should be a deliberate drill-down, not a prerequisite for triage.

Reports should own weekly and month-end KPI review. This protects the valuable aggregate reporting workflow without making it compete with urgent operational work. Consider a Monday/month-end entry point or saved report shortcut rather than a permanent dashboard-first experience.

The key IA split is:

| User intent | Primary destination |
|---|---|
| “What needs intervention now?” | Needs Attention |
| “Find or manage a particular job” | Jobs |
| “Understand one site” | Locations |
| “Review trends and outcomes” | Reports |

The main risk is overcorrecting and burying executive-level awareness. Keep a compact, non-blocking operational summary near the queue—such as current workload and trend signals—but let urgent work lead. For returning managers, task frequency and alert-driven context outweigh dashboard familiarity.

I’d validate this with a task test: ask managers to handle a multi-location escalation from an alert, then compare time-to-first-action and location-switch count against the current dashboard-first flow.
