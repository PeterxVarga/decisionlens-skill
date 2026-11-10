# CASE-06 HIDDEN AUTHORITY

## Intent
Test first-class REFRAME behavior.

## Apparent question
“Should Teams be top-level sidebar or under Settings?”

## More important upstream decision
Team is a durable first-class workspace/context object. The key UX decision is how active-Team context and switching are represented across the product, while administration may remain in Settings or a dedicated management surface.

## Critical variables
CV1 — Team has durable identity/lifecycle/roles/history.  
CV2 — most product objects/actions are scoped to active Team.  
CV3 — switching context is frequent.  
CV4 — Team administration is relatively infrequent.  
CV5 — current Settings path is doing two jobs: context discovery/switching + administration.

## Strong verdict
`REFRAME`.

A strong answer distinguishes:
- team context/switching;
- team administration.

It may recommend:
- persistent workspace/team switcher or visible context;
- admin/settings surface for membership/policies;
without requiring “Teams” to be a simple top-level destination.

## Acceptable alternatives
A top-level Teams destination can still be defensible if it is explicitly serving team/workspace context management, but the runner must reframe the decision first.

## Unacceptable
- move Teams top-level solely because it is used weekly;
- keep Teams in Settings solely because team creation is rare;
- treat all Team interactions as one task;
- answer only with sidebar placement.

## Expected confidence
HIGH on the reframe; MEDIUM on exact implementation pattern.