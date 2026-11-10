# CASE-06 — OUTPUT-X

# RAW EXECUTION

Case: CASE-06
Lane: [REDACTED]


## INITIAL USER CASE

# CASE-06 — MetricNest

MetricNest is a live analytics SaaS.

The current sidebar has:

- Home
- Dashboards
- Reports
- Alerts
- Settings

Inside `Settings`:
- Profile
- Billing
- Data Sources
- Teams

The team asks:

> Should `Teams` move from Settings into the top-level sidebar?

Known product facts:

- A Team has its own members, roles, invitations, policies, and audit history.
- Users can belong to multiple Teams.
- Users switch their active Team several times per week.
- Dashboards, Reports, Alerts, Data Sources, and some permissions are scoped to the active Team.
- Creating/removing a Team is rare.
- Managing membership/roles happens weekly for admins.
- Most normal analysis work occurs inside one active Team context.
- The current product does not make active-Team switching very visible; users often reach Settings → Teams partly to confirm which Team they are in.

Review the decision. Do not build the UI.


## ASSISTANT TURN 1

Move Team context out of Settings—but don’t make a single top-level “Teams” item carry both switching and administration.

The core problem is that Team is an active operating context: it scopes everyday analytics work and users switch it repeatedly. Settings implies occasional personal or account configuration, so it is a poor place to confirm or change the current Team.

Recommended direction:

- Make the active Team clearly visible and switchable from the persistent product chrome, ideally near the sidebar header.
- Keep Team administration—members, roles, invitations, policies, audit history—in a dedicated Team-management destination.
- Surface that management destination prominently for admins; whether it is a top-level sidebar item should depend on role and navigation capacity.

A top-level “Teams” link alone would improve discoverability, but it risks being interpreted as an admin area rather than the control for active context. Users would still have to navigate away from analysis work just to verify or change scope.

The IA should distinguish:

- **Active Team switcher:** frequent, available while working, establishes the scope of Dashboards, Reports, Alerts, Data Sources, and permissions.
- **Team management:** less frequent, admin-oriented configuration for the selected Team.
- **Team lifecycle actions:** creating or removing Teams are rare and should remain within management rather than occupying primary navigation.

This also resolves the current misleading behavior: people visit Settings → Teams partly to answer “where am I?” That question should be answered continuously by the interface, not through a settings destination.
