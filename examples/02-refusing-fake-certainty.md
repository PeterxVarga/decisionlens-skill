# Refusing fake certainty

**Benchmark case:** CASE-05  
**Mechanic demonstrated:** evidence sufficiency / refusal

## Situation

The founder asks for authenticated product navigation using only a public marketing site.

## Tested PAR V0 output

# PRODUCT ARCHITECTURE NOTE

**Product:** ClauseFlow  
**Surface:** LANDING (authenticated product requested)  
**Maturity:** UNKNOWN

## Evidence boundary

The supplied site establishes ClauseFlow’s public offer: contracts, approvals, renewals, and risk are important capabilities. It does not establish authenticated workflows, user roles, object relationships, task frequency, or navigation behavior. External research is excluded by the closed evidence envelope and would not resolve those product-specific unknowns anyway.

## REFRAME

### D-01 — Should Contracts, Approvals, Renewals, and Analytics all be top-level destinations?

The more important decision is:

**What is the dominant returning work axis: managing known contracts, triaging work requiring attention across contracts, or monitoring a portfolio?**

“Contracts,” “Approvals,” and “Renewals” could be distinct first-class destinations, but they could also be contract states, work queues, or saved views. “Analytics” could be a cross-product reporting area, a dashboard, or role-specific content. The marketing taxonomy is not sufficient evidence to choose among these meanings.

## NEEDS REAL-WORLD EVIDENCE

### D-02 — What should authenticated global navigation optimize for?

**Unknown:** Whether most returning sessions begin with a known contract, an approval/renewal exception, or portfolio-level monitoring.  
**Minimum evidence:** A small set of representative task interviews or usability sessions using realistic scenarios, supplemented by early event tracking of first destination and task completion.  
**Decision rule:** Make the dominant repeated entry mode persistent in global navigation; expose less-frequent cross-cutting work as a labeled queue, view, or role-specific destination.

## Recommended architecture under current evidence

Do not freeze an authenticated navigation from the public site.

A defensible provisional model is:

- **Contracts** as the likely durable core object and candidate top-level destination.
- **Work** as a potential cross-contract queue for approvals and upcoming renewals, if those are primarily attention/exception tasks.
- **Insights** as a potential portfolio reporting destination, if analytics is routinely used by its intended roles.
- Keep approval workflows and renewal tracking as product capabilities until evidence establishes that users enter them independently and frequently enough to justify separate global destinations.

This is a product-model hypothesis, not a recommendation to implement. The current evidence supports the public promise, not a four-item authenticated IA.

## Most consequential open question

When a normal user returns, do they usually start with a specific contract, or by finding approvals, renewals, and risks that need attention?

## Why this example matters

The skill remains useful while saying the requested decision is not supportable from the available evidence.
