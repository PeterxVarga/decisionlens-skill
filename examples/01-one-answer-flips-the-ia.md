# One answer flips the IA

**Benchmark case:** OrbitOps — early multi-client agency product  
**Mechanic demonstrated:** decision-flip questioning

## Initial decision

The product had two credible early IA directions:

- **Client-first:** enter a client, then inspect campaigns, alerts, recommendations.
- **Work-first:** start from cross-client attention, then drill into client/campaign context.

The concept description did not establish which operating axis dominated recurring use.

## PAR's first move

Which best describes a typical returning agency user’s starting point: they usually have a specific client in mind, or they first need to discover urgent issues across their client portfolio?

## Evidence supplied after the question

In a typical morning session, operators usually do NOT start with a known client. They first scan across their portfolio for anomalies/urgent work, then drill into the affected client. Roughly three quarters of recurring operating sessions follow that pattern.

## PAR's review after the answer

# PRODUCT ARCHITECTURE NOTE

**Product:** OrbitOps  
**Surface:** EARLY  
**Maturity:** CONCEPT

## Evidence boundary

This recommendation uses the supplied concept and your stated operating-session pattern only. No external research was used because the evidence envelope is closed. The product’s data model, alert quality, permissions, and actual task behavior remain unvalidated.

## SUPPORTED

### D-01 — Should the primary operating entry point be client-first or work-first?

**Direction:** Make the default experience a cross-client attention/work queue, then drill into the relevant client and campaign.  
**Confidence:** MEDIUM

About three quarters of recurring operating sessions begin with portfolio-wide anomaly and urgent-work discovery rather than a known-client lookup. That makes “what needs action?” the dominant operating axis. A client-first structure would add an unnecessary selection step before the dominant job and risks hiding cross-client prioritization.

Client context still matters after triage: each queue item should resolve into a client and campaign workspace with history, related alerts, recommendations, and follow-up state.

**What would reopen this:** Reopen if representative usage shows that known-client investigation becomes the dominant recurring entry pattern, or if operators cannot prioritize cross-client issues meaningfully.

## REVISIT

### D-02 — Should “Clients” be removed from primary navigation?

**Recommended direction:** Keep **Clients** as a persistent secondary global destination, alongside the work queue; do not make it the home route.  
**Confidence:** MEDIUM

Client is a consequential durable object: users need client-specific campaigns and history, and likely revisit it independently. It should therefore remain directly reachable and deep-linkable. But it should not control the default operating route when most sessions are portfolio triage.

**Strongest counter-case:** If client account management, reporting, or planned campaign work consumes more time than anomaly response, client-first may become a better operating axis.

**What would change the recommendation:** Measure the share of sessions beginning with planned client work versus exception discovery, segmented by role.

## Recommended architecture under current evidence

Use a two-level model:

- **Home / Attention:** a cross-client queue of anomalies, operational problems, and recommendations; support prioritization, assignment/ownership, status, and drill-in.
- **Client:** a durable client workspace containing campaigns, performance/history, all alerts, recommendations, and resolved/open follow-up.
- **Campaign:** contextual investigation beneath its client, with relevant performance change and operational history.
- **Follow-up state:** attach it to the actionable issue/recommendation, while retaining links to its client and campaign. This prevents “work” from becoming a disconnected inbox.

In short: make work-first the operating surface, but preserve client-first as the product’s durable information hierarchy. The likely navigation spine is **Attention**, **Clients**, and any later reporting/settings areas—not a single hierarchy forced to serve both triage and investigation.

## Most consequential open question

What exactly is the unit of work—an alert, a recommendation, or a combined case that can contain investigation and follow-up? That semantic decision should be settled before designing queue rows, ownership, and resolution states.

## Why this example matters

The recommendation is not the distinctive behavior.

The distinctive behavior is that the system **refused to earn the recommendation by guessing**. It isolated the variable that could flip the architecture, asked for it, and only then converged.
