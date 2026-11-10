# CASE-05 — OUTPUT-X

# RAW EXECUTION

Case: CASE-05
Lane: [REDACTED]


## INITIAL USER CASE

# CASE-05 — ClauseFlow

I only have access to the public marketing site of **ClauseFlow**, a contract-operations SaaS.

The public site says:

- “One workspace for contracts, approvals, renewals, and risk.”
- Product pages exist for:
  - Contract repository
  - Approval workflows
  - Renewal tracking
  - Risk analytics
- The marketing navigation includes:
  - Product
  - Solutions
  - Customers
  - Resources
  - Pricing
- Screenshots are polished marketing composites, not enough to reconstruct real workflows.
- I do NOT have an authenticated account, product telemetry, user interviews, a PRD, or real app screenshots.

The founder asks:

> Based on this site, design the best authenticated product navigation and tell me whether Contracts, Approvals, Renewals, and Analytics should all be top-level destinations.

Review what can responsibly be decided from the available evidence.


## ASSISTANT TURN 1

The public site supports an initial information architecture, but not a claim that it reflects proven user workflows. Treat this as a hypothesis to validate once authenticated-product evidence exists.

Recommended authenticated navigation:

- Home — personalized work queue: pending approvals, upcoming renewals, contract activity, and risk alerts.
- Contracts — repository, search, contract records, documents, obligations, and lifecycle status.
- Approvals — inbox and workflow management for requests requiring action.
- Renewals — renewal calendar/list, ownership, notices, and renewal work.
- Risk — contract-level risk signals, exceptions, and portfolio analytics.
- Create / Import — a prominent global action, not a navigation destination.
- Settings — integrations, templates, users, permissions, workflow configuration.

Contracts should be top-level: it is the likely system of record and primary object users need to find and manage.

Approvals and Renewals should also begin as top-level destinations. Both describe time-sensitive, repeatable work with distinct users, queues, and planning views; hiding either under Contracts risks making urgent work harder to discover.

“Analytics” should not automatically be top-level under that exact name. The site’s wording is “Risk analytics,” which suggests a risk-oriented capability rather than a broad reporting product. I’d make this a top-level **Risk** destination if risk signals and portfolio oversight are a core recurring job; otherwise, place risk insights within Contracts and expose reporting through dashboards. The available evidence does not resolve that choice.

The key distinction is between navigation by product capability and navigation by work. A polished initial model can use Contracts, Approvals, Renewals, and Risk, but the authenticated home should unify cross-cutting work so users do not need to visit every section just to know what requires attention.

What cannot responsibly be determined from the site:

- Which role is primary, and whether all roles need all destinations.
- Whether approvals are primarily contract approvals or a general request workflow.
- Whether renewals are independent work or simply a contract lifecycle view.
- Whether “risk analytics” is sufficiently frequent and actionable to justify persistent top-level navigation.
- The labels, ordering, permissions, and default landing page that best fit actual usage.

Before committing beyond this hypothesis, validate with authenticated screenshots or task evidence for: finding a contract, approving a request, preparing a renewal, and investigating a risk alert. That evidence should determine whether Risk remains top-level and whether role-based navigation is needed.
