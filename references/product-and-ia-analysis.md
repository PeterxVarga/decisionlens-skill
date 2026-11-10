# Product and IA Analysis

## Shared product model

Recover only what is necessary:

```yaml
productModel:
  primaryActors: []
  dominantJobs: []
  recurringJobs: []
  consequentialObjects: []
  primaryActions: []
  knownConstraints: []
  observedStructure: []
  observedFlows: []
  evidenceGaps: []
```

Do not fill unknown fields with plausible guesses.

# LANDING adapter

Focus on decision mechanisms, not generic CRO tips.

## Comprehension architecture
- What category/mental model is established first?
- Is the mechanism explained before the visitor understands why it matters?
- Does the page require prior product knowledge?
- Are multiple product concepts competing for first interpretation?

## Intent architecture
- Is there one primary conversion intent or several?
- Are CTAs genuinely sequential/segment-specific or competing?
- Does navigation support the intended acquisition journey?

## Information sequence
Typical decision:
problem → category → mechanism → proof → action is not universal.
Evaluate what must be known before the next block is persuasive/comprehensible.

## Trust/proof
Ask whether proof is:
- necessary before commitment;
- relevant to the actual objection;
- credible for the audience;
- prematurely prominent.

## Public IA
Distinguish:
- acquisition destinations;
- educational resources;
- pricing/commitment surfaces;
- product access;
- support/docs.

# PRODUCT / SAAS adapter

## Object model
For candidate first-class resources ask:
- own lifecycle?
- own permissions?
- own history?
- independently revisited?
- linked by deep URL?
- acted on directly?
- meaningful outside parent context?

Do not let current navigation alone define product ontology.

## Recurring-job model
Identify:
- dominant repeated task;
- monitoring vs creation vs retrieval vs administration;
- known-object vs cross-object work;
- interruption/resumption;
- consequence of losing place.

## Navigation
Evaluate:
- global vs local;
- object-first vs work-first;
- labeled persistence vs disclosure;
- destination vs view;
- route/re-entry behavior;
- switching frequency;
- cross-domain comparison.

## Dashboard / work surfaces
Do not assume dashboard = home.
Ask whether the dominant returning job is:
- orientation;
- monitoring;
- direct work;
- exception handling;
- cross-domain summary.

## Actions
Evaluate:
- frequency;
- consequence;
- recoverability;
- permissions;
- current-state dependence;
- external effects;
- persistent vs disclosed placement.

## State
Include:
- loading;
- empty;
- filtered zero;
- stale;
- optimistic/pending;
- error;
- conflict;
- offline/reconnect where relevant.

Treat state behavior as product behavior when it affects decisions.

## Density/comparison
Ask:
- repeated cross-row/column comparison?
- sequential triage?
- content variability?
- item counts?
- action placement?
- laptop/mobile distribution?

## Responsive
Do not let minority/mobile needs automatically dictate desktop.
Do not let desktop structure hide mobile semantic/read-order failures.

# EARLY adapter

## First principle
Do not generate navigation before product structure is sufficiently understood.

## Determine the operating axis
Common competing axes:
- object/client/project-first;
- work/attention-first;
- process/stage-first;
- role-specific;
- temporal/calendar-first.

Ask what the dominant returning job implies.

## Core object test
A concept deserves first-class treatment when enough of these are true:
- durable identity;
- recurring direct management;
- lifecycle;
- independent permissions;
- independent history;
- independent deep links;
- relationships to other objects;
- user vocabulary treats it as a noun they own/manage.

## Early IA candidate generation
Generate structures only after:
- primary actor/job;
- core objects;
- operating axis
are reasonably supported.

If these are unresolved:
REFRAME to the product-model decision.

# HYBRID adapter

Do not collapse:
- landing promise;
- public navigation;
- product IA;
- product reality.

A marketing page may intentionally simplify or rename product structure.
Flag mismatches only when they create real comprehension/expectation problems.

# Accessibility and responsive as decision variables

Do not run a full audit by default.

Integrate when they can flip:
- visual/DOM reading order;
- keyboard/focus path;
- touch action access;
- truncation/wrapping;
- color-only state communication;
- interaction targets;
- reordering across breakpoints.

# Best-practice rule

A pattern may be useful because it has a known mechanism, not because it is fashionable or common.

Always ask:
- what user/task condition makes the pattern work?
- does that condition hold here?
