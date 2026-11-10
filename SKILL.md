---
name: product-architecture-review
description: Review a landing page, SaaS/product interface, screenshots, or an early product concept by identifying the consequential UX and product-architecture decisions behind it. Use when the user wants product architecture, IA, navigation, UX structure, landing-page structure, product critique, a product teardown, or help deciding how an evolving product should be organized. Inspect available evidence first, ask only questions whose answers could materially change a consequential decision, compare credible alternatives, research only decision-flipping uncertainty, and explicitly return unresolved/reframe/immaterial/real-world-evidence outcomes instead of manufacturing certainty. Do not use for pure visual styling, pixel polish, coding a UI, or a full accessibility/CRO audit unless those are directly decision-relevant.
---

# Product Architecture Review

Status: V0 EXPERIMENTAL

## Purpose

Turn a product surface or concept into the small set of consequential UX/product-architecture decisions that matter, then determine which are supportable from available evidence.

This is not a universal senior designer and not a UI builder.

The core unit is a **consequential decision**, not a screen, issue count, heuristic score, or visual preference.

## Core outcomes

Use these public statuses:

- `SUPPORTED`
- `REVISIT`
- `UNRESOLVED`
- `REFRAME`
- `IMMATERIAL_UX_DIFFERENCE`
- `NEEDS_REAL_WORLD_EVIDENCE`

Never force every run to contain every status.

## Hard rules

1. Never claim an objectively best UX/IA.
2. Never infer authenticated product behavior from a marketing surface alone.
3. Never ask a question unless plausible answers could materially change a consequential decision.
4. Never treat competitor prevalence or generic best practice as product-specific truth.
5. Never present derived reasoning, model simulation, or internal adversarial agreement as real user evidence.
6. Never force a winner when decisive evidence is missing.
7. Never force a material UX distinction when the difference is immaterial.
8. Never answer a downstream layout/navigation question when an upstream semantic/product question controls it.
9. Never research merely to decorate the report.
10. Never silently become a builder/prototyper.
11. Existing observed product facts outrank generic patterns and visual convention.
12. Explicit uncertainty is a valid result.

## Workflow

### Phase 0 — Observe before asking

Use all context already available:
- user prompt;
- supplied URL or screenshots;
- supplied product description;
- repository/product docs when explicitly available;
- existing research/analytics supplied by the user.

Do not ask for information already present.

Read `references/intake-and-routing.md`.

### Phase 1 — Classify surface and maturity

Classify the input as one or more:

- `LANDING`
- `PRODUCT`
- `EARLY`
- `HYBRID`

And maturity:

- `CONCEPT`
- `EVOLVING`
- `LIVE`
- `UNKNOWN`

State any evidence boundary that materially limits the review.

### Phase 2 — Build the minimum product model

Do not build a giant ontology.

Recover only what is needed to reason:
- primary actors;
- dominant and recurring jobs;
- consequential objects;
- primary actions;
- known constraints;
- observed structure/flows;
- important evidence gaps.

Unknown is allowed.

Read `references/product-and-ia-analysis.md`.

### Phase 3 — Identify consequential decisions

Select only decisions where a different answer could materially affect:
- task success;
- discoverability;
- comprehension;
- error/consequence risk;
- recurring operator efficiency;
- product semantics;
- information architecture;
- navigation;
- user control;
- accessibility;
- responsive behavior;
- conversion intent;
- implementation direction in a way that meaningfully changes UX.

Do not inflate trivial polish choices into consequential decisions.

### Phase 4 — Evidence sufficiency and question gate

For each consequential decision:
- record what is known;
- identify decision-flip variables;
- determine whether missing information is externally researchable, user-answerable, or requires real-world observation.

Ask follow-up questions only when necessary.

Prefer 0–3 questions.
Normal hard maximum: 7.

Every question must map to at least one named decision and have a plausible answer that changes:
- candidate ranking;
- confidence;
- frame;
- or escalation state.

Read `references/evidence-and-research.md`.

### Phase 5 — Build credible alternatives

For each contested consequential decision:
- construct at least two credible candidates;
- steelman each;
- avoid cosmetic variants;
- preserve a current incumbent only if it is genuinely one of the strongest candidates.

If candidate generation is premature because the actual question is upstream, return `REFRAME`.

If the user-facing difference is not consequential, return `IMMATERIAL_UX_DIFFERENCE`.

### Phase 6 — Targeted research

Research only when it can materially change a decision.

Default budget:
- 0–3 narrow research questions;
- 2–3 strong comparator/reference products maximum.

Stop when:
- the decision is supportable;
- the remaining unknown is behavioral/product-specific;
- or new research is unlikely to change the result.

Competitors are precedent, not authority.

### Phase 7 — Adversarial convergence

Read `references/decision-adversary.md`.

For each important decision:
1. identify a provisional direction if one exists;
2. attack it before treating its own rationale as established;
3. find the strongest path by which another candidate could win;
4. test whether the candidate set is incomplete;
5. audit evidence/rationale;
6. freeze only if the remaining uncertainty is bounded.

If the unresolved variable is real behavior/distribution and materially decision-flipping:
`NEEDS_REAL_WORLD_EVIDENCE`.

### Phase 8 — Synthesize architecture

Do not simply list decisions.

Explain how the supported/revisit/reframe decisions combine into the recommended architecture under current evidence.

Do not pretend unresolved decisions are solved.

### Phase 9 — Output

Default:
read `templates/architecture-note.md`.

Use `templates/deep-review.md` only when the user asks for a deep/full report or the decision set is too complex for the short note.

## Mode-specific guidance

Read only the relevant section of `references/product-and-ia-analysis.md`:

- LANDING: acquisition/comprehension/CTA/public-IA decisions.
- PRODUCT: object model/navigation/workflows/states/actions/density/responsive decisions.
- EARLY: operating axis/core objects/jobs/initial IA/evidence-before-commitment.
- HYBRID: separate public and authenticated claims; do not collapse them.

## Evidence discipline

Use the evidence classes in `references/evidence-and-research.md`.

Do not upgrade:
- precedent into product fact;
- synthetic examples into user behavior;
- internal model agreement into independent evidence;
- user preference into universal usability evidence.

## Scope boundary

This skill may identify the need for:
- usability testing;
- tree testing;
- card sorting;
- telemetry;
- accessibility testing;
- prototype comparison;
- visual design work.

It does not automatically perform all of them.

The review stops at product-architecture judgement and a bounded evidence plan unless the user explicitly asks for further work.
