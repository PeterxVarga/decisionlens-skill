# CASE-05 — OUTPUT-Y

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

Contracts, Approvals, Renewals, and Analytics should not automatically all be top-level destinations. The public site establishes product areas, not how often authenticated users use them, which roles use them, or whether each needs a standalone workspace.

A responsible starting navigation is:

- Contracts — top-level: likely the core object/workspace.
- Approvals — top-level only if users routinely triage and act on approvals; otherwise a Contracts view/state.
- Renewals — top-level only if renewal owners manage a recurring queue and calendar; otherwise a Contracts view/state.
- Analytics — top-level for operational/admin roles; otherwise a secondary destination or role-gated view.

Recommended authenticated structure:

```text
Home
Contracts
Work queue
  └ Approvals / renewals needing action
Insights
  └ Risk analytics and reporting
```

“Work queue” is the stronger default than separate Approvals and Renewals because it organizes around a user’s immediate job—what needs attention—rather than around the company’s feature taxonomy. Within it, users can filter by approval, renewal, risk, owner, and due date. This also prevents duplicated notifications and competing task lists.

Keep Contracts independently accessible because it plausibly contains the repository and is likely the place users search, create, review, and manage contract records. Place detail-level approvals, renewal terms, and risk signals on each contract as well as in their cross-contract queues.

The key unresolved question is role and task frequency: if legal ops, procurement, sales, and executives each use different areas daily, a role-aware navigation may justify more destinations. Without authenticated-product evidence, avoid committing to a four-item feature-based navigation or a detailed information architecture.

The riskiest assumption is that “Risk analytics” is a frequent operational workflow rather than periodic reporting. Validate cheaply with a short role/task inventory: ask each intended role what they open first, what they act on daily, and what they check weekly or monthly. If Approvals or Renewals dominate daily work for a distinct role, promote them; if not, keep them in the unified work queue.
