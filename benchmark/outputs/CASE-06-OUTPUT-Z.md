# CASE-06 — OUTPUT-Z

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

Move team context into the persistent top-level navigation, but don’t promote a generic “Teams” settings page as a peer to Home and Reports.

Use a highly visible active-Team switcher in the sidebar header. It should show the current team, allow switching, and make the scope of Dashboards, Reports, Alerts, Data Sources, and permissions unmistakable. Include “Manage team” within that control for admins.

Why:

- Switching teams is frequent and changes the meaning of most of the product.
- Users are currently using Settings as a workaround to answer “which team am I in?”—a navigation failure, not a settings need.
- Membership, roles, invitations, policies, and audit history are team administration, not personal/account settings.
- Creating or deleting teams is rare, so keep those actions inside the management area rather than exposing them as a primary destination.

Recommended structure:

```text
[ Current team ▾ ]
  Switch team
  Manage current team

Home
Dashboards
Reports
Alerts
Settings
```

“Manage current team” can contain Members, Roles, Invitations, Policies, and Audit history, with destructive or rare organization-level actions clearly separated. For non-admins, show only the switcher and team details they are allowed to see.

The main risk is adding “Teams” as a sixth destination without clarifying whether it means switching context or administering teams. That creates a second, competing model. Make team selection persistent; make team management contextual.
