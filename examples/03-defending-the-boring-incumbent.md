# Defending the boring incumbent

**Benchmark case:** CASE-02  
**Mechanic demonstrated:** avoid novelty bias

## Situation

A stakeholder wants to replace a dense reconciliation table with cards because tables feel old.

## Tested PAR V0 output

# PRODUCT ARCHITECTURE NOTE

**Product:** LedgerGrid  
**Surface:** PRODUCT  
**Maturity:** LIVE  

## Evidence boundary

The supplied evidence covers reconciliation behavior, display distribution, and tested preferences. It does not establish whether cards would improve a separate, detail-oriented task; this review concerns the main reconciliation workspace.

## SUPPORTED

### D-01 — Should the main reconciliation workspace use cards instead of a dense table?

**Direction:** Retain the dense table as the primary workspace.  
**Confidence:** HIGH

Reconciliation is repeated cross-row comparison work: users spend long sessions comparing 5–7 attributes across adjacent groups of 8–12 rows, then resolve items largely through inline or bulk actions. A table makes those relationships continuously visible and supports efficient scanning, sorting, filtering, multi-select, and bulk assignment.

Cards steelman well when a user needs to understand one transaction deeply and independently. But they fragment cross-row comparison, consume more vertical space, and make bulk/inline workflows less direct—the opposite of the observed dominant job. “Modern” is not a task condition that outweighs those operational costs.

**What would reopen this:** Evidence that the dominant reconciliation workflow shifts from cross-row triage to single-transaction investigation, or that table use causes material comprehension or error problems.

## REVISIT

### D-02 — Should the same dense workspace be used at every breakpoint?

**Recommended direction:** Keep the full reconciliation table desktop-first; provide a reduced mobile status/checking experience rather than forcing the complete reconciliation workflow into cards.  
**Confidence:** HIGH

92% of sessions occur on displays at least 1440px wide, while mobile represents 2% and is used mostly for status checks. The desktop workspace should optimize dense comparison and repeated action. On tablet, preserve a table where possible with deliberate column prioritization, horizontal access to secondary attributes, and persistent selection/action state. On mobile, prioritize status, assigned exceptions, and a route into item detail; do not imply that a card layout is an equivalent full-reconciliation substitute.

**Strongest counter-case:** If tablet or mobile users must regularly perform time-sensitive, full reconciliation, a purpose-built mobile workflow may be necessary.

**What would change the recommendation:** Telemetry or task observation showing meaningful mobile/tablet completion of comparison-heavy reconciliation work.

## Recommended architecture under current evidence

Treat the dense table as LedgerGrid’s core operational surface, not legacy visual debt. Preserve visible comparison columns and nearby-row context; keep bulk and inline exception resolution close to selected rows. Offer detail expansion or a side panel for transaction-specific investigation when needed, without replacing the comparison surface.

Responsive behavior should follow the job: full table on desktop, constrained table support on tablet, and a focused monitoring/status experience on mobile.

## Most consequential open question

Which columns are indispensable to the repeated 5–7-column comparison sets? That evidence should determine default column priority and responsive disclosure—not a generic preference for cards.

## Why this example matters

The skill does not redesign for novelty. It defends an incumbent when the recurring workflow and observed behavior support it.
