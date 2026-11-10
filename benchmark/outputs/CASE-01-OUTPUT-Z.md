# CASE-01 — OUTPUT-Z

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

# PRODUCT ARCHITECTURE NOTE

**Product:** QueuePilot  
**Surface:** PRODUCT  
**Maturity:** LIVE  

## Evidence boundary

The supplied operational data is sufficient for the default returning-user entry point and cross-location work model. It does not establish detailed behavior for Customers or Settings, nor prescribe a visual layout. No external research is needed: the decision turns on QueuePilot’s observed task distribution.

## SUPPORTED

### D-01 — What should returning managers encounter first?

**Direction:** Make a cross-location **Needs Attention** work queue the default returning-user surface; do not retain the KPI dashboard as the primary landing surface.  
**Confidence:** HIGH

68% of returning sessions begin soon after an alert, and their first meaningful action is triage across overdue, unassigned, blocked, or failed jobs. In addition, 78% of escalations span multiple locations, while only 19% begin with a known location. A KPI dashboard supports orientation and reporting, but it inserts an interpretation step before the dominant urgent job.

The credible counter-case is a dashboard-first model for managers who need broad situational awareness. It loses here because the supplied behavior says the urgent, actionable cross-location task dominates returning sessions.

**What would reopen this:** Reassess if alert-driven sessions materially decline, or if most alert sessions begin with KPI interpretation rather than acting on jobs.

### D-02 — Should Jobs remain location-scoped by default?

**Direction:** Make cross-location job access the default. Treat a selected-location Jobs view as a scoped view, not the global starting state.  
**Confidence:** HIGH

The current location switcher conflicts with a workflow where escalations commonly require comparison and action across locations. Since managers can act directly on a found job, the product should preserve the cross-location triage context through action and return, rather than force repeated location changes.

**What would reopen this:** Reassess if job volume makes a cross-location queue unreliable to prioritize, or if most managers shift to known-location work.

### D-03 — Where should KPI reporting live?

**Direction:** Keep aggregate KPIs and performance analysis as a reporting/orientation destination, rather than the default work surface.  
**Confidence:** MEDIUM

Weekly Monday and month-end reporting is meaningful, but it is a recurring reporting job with a different cadence from alert-driven operational triage. It belongs under **Reports**, with location performance and aggregate metrics available there. A lightweight operational summary can coexist near the work queue only if it does not displace actionable attention items.

**What would reopen this:** Reassess if reporting data shows daily KPI review is a prerequisite to operational action.

## Recommended architecture under current evidence

Use a work-first primary IA:

- **Needs Attention** — default destination; cross-location queue for overdue, unassigned, blocked, and failed jobs, with direct action and return to the queue context.
- **Jobs** — complete cross-location job inventory for search, browsing, and non-exception work; allow optional location scoping rather than requiring it.
- **Locations** — object-first workspace for managers entering with a known location; show that location’s jobs, performance, and relevant history.
- **Customers** — retain as a separate domain; there is not enough evidence to change its role.
- **Reports** — aggregate KPIs, revenue, response time, and performance analysis for weekly/month-end review.
- **Settings** — retain as administrative configuration.

The key change is semantic, not cosmetic: “Needs Attention” is a cross-location operational work queue, while “Jobs” is the broader job resource and “Locations” is the known-object route. Alert links should enter the relevant queue state or job while preserving a clear route back to cross-location triage.

## Most consequential open question

How should the queue prioritize competing exceptions when several locations are affected? Measure whether urgency, business impact, SLA risk, or manager ownership best predicts the next action; this affects queue ordering, not the decision to make cross-location triage the default.
