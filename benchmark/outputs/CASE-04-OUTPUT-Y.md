# CASE-04 — OUTPUT-Y

# RAW EXECUTION

Case: CASE-04
Lane: [REDACTED]


## INITIAL USER CASE

# CASE-04 — OrbitOps concept

I am designing an early-stage SaaS called **OrbitOps** for marketing agencies.

What I know so far:

- Agencies manage campaigns for multiple client businesses.
- OrbitOps ingests campaign/ad-platform data.
- It detects unusual performance changes and operational problems.
- It should help agency staff decide what needs action, investigate it, and follow up.
- Users will also need to view a specific client's campaigns and history.
- No navigation or object hierarchy is locked yet.

I am deciding between two early IA directions:

**A — Client-first**
The main navigation is Clients. Users enter a client, then inspect campaigns, alerts and recommendations inside it.

**B — Work-first**
The default experience is a cross-client attention/work queue. Users discover what needs action, then drill into the relevant client/campaign.

Help me decide the architecture.

Ask only what you genuinely need before making the recommendation.


## ASSISTANT TURN 1

Choose **B — Work-first** as the primary architecture, with Client as a strong secondary context.

OrbitOps’ core promise is detecting exceptions and helping agencies act. Agency staff typically begin with, “What needs attention across my book of business?” A client-first entry point makes urgent cross-client work harder to discover and prioritize.

Recommended structure:

- **Attention** — default landing: prioritized cross-client queue of anomalies, operational issues, and follow-ups.
- **Investigate** — an issue workspace showing evidence, affected campaigns, recent history, owner, and recommended next step.
- **Clients** — directory and client health overview for account reviews and proactive exploration.
- **Client detail** — campaigns, alerts, recommendations, activity/history, and client-specific filtering.
- **Campaign detail** — performance context, change history, linked issues, and actions.

The key interaction is a drill-in path:

`Attention item → issue investigation → client/campaign context → take or assign action → tracked follow-up`

Make “client” a persistent, visible context—not a navigation prison. Every work item should expose its client and campaign prominently, with one-click movement into their histories.

Why not A as the primary model: it fits planned account reviews, but risks burying time-sensitive issues across many clients. Staff would have to remember where to look before OrbitOps can show them what changed.

The main product decision still to validate is prioritization: whether the queue can reliably rank issues by urgency, impact, confidence, and ownership. If it cannot, users will retreat to client-by-client checking regardless of the IA.
