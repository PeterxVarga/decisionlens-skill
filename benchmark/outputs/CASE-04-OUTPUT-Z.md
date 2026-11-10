# CASE-04 — OUTPUT-Z

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

Choose **B — Work-first** as the primary architecture, with strong client drill-down views.

OrbitOps’ distinct value is detecting changes and helping staff decide, investigate, and follow up. That is inherently a cross-client workflow: the first question is “what needs attention now?”, not “which client should I open?”

A client-first structure risks burying urgent issues inside separate client spaces and makes portfolio-level prioritization harder. It fits lookup and account-review tasks, but those are secondary to the product’s stated operational loop.

Recommended hierarchy:

- **Work / Attention** — default landing area; prioritized alerts, operational problems, recommendations, ownership/status, and follow-up.
- **Clients** — directory and client health/history view for intentional lookup and reviews.
- **Client detail** — campaigns, alerts, recommendations, and historical activity scoped to that client.
- **Campaign detail** — performance context and the investigation trail for a specific campaign.

The key is not to make this a choice between two disconnected products. Treat the work queue as the system of action and the client as the system of context. Every queue item should clearly expose its client and campaign, while every client page should show current and resolved work.

Use shared object relationships rather than duplicating content:

`work item → client → campaign → performance/history`

A useful validation criterion: can a staff member both (1) process all attention-worthy items across clients and (2) answer “what has happened for this client?” without changing mental models? This hybrid meets both, with Work-first providing the clearer product center of gravity.
