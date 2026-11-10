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