# Evidence and Research

## Evidence classes

Use these internally.

### E0 — Observed product fact
Directly observed in supplied/live product, source, screenshot, state or behavior.

### E1 — Real behavioral/user evidence
Telemetry, user research, support evidence, observed task behavior, experiment result.

### E2 — External research
Standards, research literature, authoritative guidance.

### E3 — Comparable product pattern
Observed pattern from other products.

### E4 — Derived reasoning
Inference from E0–E3.

### E5 — Synthetic/simulated signal
Model-generated scenario, simulated user, adversarial stress.

### E6 — Preference
Taste, aesthetic preference, stakeholder preference.

## Rules

- E4/E5 are not independent evidence.
- E3 is precedent, not proof of product fit.
- E6 can decide genuine taste questions but not behavioral facts.
- When sources conflict, explain applicability instead of counting votes.

## Evidence sufficiency

For each consequential decision ask:

1. What variable would make A beat B?
2. Do we know it?
3. If not, can the user answer reliably?
4. Can external research answer it?
5. Does it require real behavior/product distribution?

## Research trigger

Research only if:
- missing fact is external;
- impact is HIGH or MEDIUM;
- result could flip/reframe/escalate the decision.

Do not research:
- to produce citations;
- to look comprehensive;
- when direct product evidence already decides the mechanism;
- behavioral/product-distribution unknowns that web research cannot resolve.

## Comparator selection

Prefer 2–3 strong comparators.

Choose for mechanism similarity:
- same recurring job;
- similar consequence/risk;
- similar density;
- similar object model;
- similar audience expertise;
not merely same industry.

Classify each comparator:
- APPLICABLE_PRECEDENT
- CONTEXT_MISMATCHED
- WEAK
- NO_DECISION_VALUE

## Research question format

Good:
"Under what conditions do persistent labels outperform icon-only navigation for mixed-expertise repeated-use applications?"

Bad:
"What are UI navigation best practices?"

Good:
"What evidence supports an extra confirmation step for irreversible destructive actions?"

Bad:
"What do popular apps do for delete?"

## Real-world escalation

Use `NEEDS_REAL_WORLD_EVIDENCE` when the decision depends materially on unknown real behavior.

Possible minimum evidence:
- telemetry;
- event distribution;
- search/log analysis;
- tree testing;
- card sorting;
- small comparative usability test;
- safe task simulation with real representative users;
- limited pilot.

Specify:
- variable measured;
- minimal method;
- precommitted decision rule when practical.

## Confidence

HIGH:
decisive mechanisms supported; remaining uncertainty unlikely to flip.

MEDIUM:
direction is defensible; meaningful but bounded uncertainty remains.

LOW:
important decision-flip uncertainty unresolved.

HIGH-risk + LOW confidence must not freeze.
