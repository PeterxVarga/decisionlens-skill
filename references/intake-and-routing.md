# Intake and Routing

## Goal

Get enough context to identify consequential decisions without turning the review into an onboarding questionnaire.

## Observe-first rule

Before asking anything:
- inspect supplied URL/screenshots/text;
- reuse facts from the conversation;
- treat an existing product's visible terminology and behavior as the current observable truth;
- distinguish observed behavior from marketing claims.

## Surface routing

### LANDING
Use when the supplied surface is primarily public acquisition/marketing.

Typical decision families:
- what must be understood first;
- category/offer mental model;
- information sequence;
- one vs multiple primary conversion intents;
- proof/trust timing;
- public navigation;
- relationship between marketing promise and real product.

Do not infer authenticated IA from this mode alone.

### PRODUCT
Use when reviewing authenticated or operational product surfaces.

Typical decision families:
- primary navigation axis;
- object hierarchy;
- recurring jobs;
- dashboard vs work queue;
- local vs global navigation;
- action hierarchy;
- state and recoverability;
- permissions;
- density/comparison;
- responsive transformation.

### EARLY
Use when the user supplies an idea, brief, partial mock, PRD or evolving product without stable current architecture.

Typical decision families:
- primary actor/job;
- core objects;
- operating axis;
- cross-object vs object-first work;
- initial navigation model;
- first-class resource vs view;
- what should remain undecided until evidence exists.

Do not "audit" missing UI as if it were a defect.

### HYBRID
Use when more than one surface is legitimately in scope.

Separate claims:
- public acquisition architecture;
- authenticated product architecture;
- early product-model assumptions.

## Maturity routing

### CONCEPT
No incumbent by default.

### EVOLVING
Some decisions are provisional. Ask which are already locked only when that matters.

### LIVE
Treat existing structure as incumbent, not authority.

### UNKNOWN
Do not guess. Use only if maturity affects the decision.

## Question gate

A question may be asked only if:

1. its answer is unavailable;
2. it maps to a named consequential decision;
3. two plausible answers would cause a material difference.

Material differences:
- flip preferred candidate;
- change confidence;
- trigger REFRAME;
- trigger/avoid real-world escalation.

## Question budget

Prefer 0–3.
Normal hard maximum: 7.

Ask a compact batch.
Only ask a second batch when answers reveal a genuinely new upstream decision.

## High-value question forms

### Recurring-job axis
"When a returning user starts a normal session, are they usually entering with a known object/client/project in mind, or trying to discover what needs attention across many objects?"

### Frequency/distribution
"Is this action part of the dominant repeated workflow, or a rare administrative task?"

### Consequence/recovery
"If this action is wrong, can the user reliably undo/recover before an external effect occurs?"

### Object semantics
"Is X something users manage over time with its own lifecycle, permissions and history, or mainly a view/configuration of another object?"

### Audience split
"Do the users who need this advanced capability represent the dominant operating cohort or a small specialist cohort?"

## Low-value question forms

Avoid:
- "What style do you like?"
- "Do you prefer sidebar or tabs?"
- "Should it feel modern?"
- "What color should it be?"
- questions already answered by the product.

These may be valid visual-design questions, but they are not Product Architecture Review questions unless they materially control a consequential decision.
