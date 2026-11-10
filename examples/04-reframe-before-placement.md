# Reframe before placement

**Benchmark case:** CASE-06  
**Mechanic demonstrated:** upstream semantic reframe

## Situation

The team asks whether Teams should move from Settings into the primary sidebar.

## Tested PAR V0 output

# PRODUCT ARCHITECTURE NOTE

**Product:** MetricNest  
**Surface:** PRODUCT  
**Maturity:** LIVE  

## Evidence boundary

This uses only the supplied product facts. The active-Team control and exact current flows were not observed; no external research is needed because the remaining uncertainty is product-specific behavior.

## REVISIT

### D-01 — Should Teams move from Settings into the top-level sidebar?

**Recommended direction:** Promote Teams out of Settings, but do not treat a sidebar destination as the primary solution to Team switching. Make the active Team visible and switchable globally; expose a top-level Teams destination for Team-level membership, roles, invitations, policies, and history.  
**Confidence:** MEDIUM

Teams are a first-class product object: they have durable identity, membership, roles, policies, audit history, and scope most operational resources. Multiple memberships plus repeated switching make burying the concept under Settings semantically misleading and operationally costly.

However, “Teams” serves two distinct jobs:

- switching the active operational context, which should be available wherever analysis work occurs;
- administering a Team, which merits a dedicated destination but is primarily an admin workflow.

A simple Settings → Teams sidebar move improves discoverability, but can still leave switching indirect if users must enter a management page merely to confirm or change context.

**Strongest counter-case:** If nearly all Team changes are infrequent administrative work by a small admin cohort, keeping management in Settings would preserve a simpler primary sidebar.

**What would change the recommendation:** Revisit if usage shows Team switching is rare, or that a global context control creates confusion or harmful scope mistakes.

## NEEDS REAL-WORLD EVIDENCE

### D-02 — Should the top-level Teams destination be a primary work destination for everyone, or mainly an admin destination alongside a global switcher?

**Unknown:** The distribution of switching versus membership/policy-management sessions, by role.  
**Minimum evidence:** Instrument active-Team changes, visits to Team management, and role-specific entry paths; then test a visible global switcher with representative analysts and admins.  
**Decision rule:** If switching is common across normal analysis sessions, prioritize a persistent global switcher and keep the Teams destination management-oriented. If most visits are administrative and switching is rare, make Team management less prominent.

## Recommended architecture under current evidence

Treat active Team as global product context, not a Settings detail or a page users visit just to orient themselves. Put the current Team and switching affordance in persistent product chrome, with clear scope visibility for dashboards, reports, alerts, data sources, and permission-sensitive actions. Add a top-level Teams destination for the Team object and its administration; keep rare creation/removal actions appropriately constrained there.

This changes the architecture from “settings for organizational configuration” to “a first-class operating boundary with dedicated management.”

## Most consequential open question

Do non-admin analysts need to switch Teams during ordinary work often enough that a global switcher materially reduces wrong-context work and navigation detours?

## Why this example matters

The apparent navigation-placement question is downstream of a first-class context/object decision.
