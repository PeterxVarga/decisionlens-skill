# Wave 02 — V1 Decision Qualification Engine falsification

Date: 2026-08-30

## Final status

**FAIL — KEEP V0**

The proposed V1 Decision Qualification Engine was implemented as an isolated candidate and tested against a frozen hostile evaluation package.

The candidate was **not accepted for release and must not replace or modify the frozen V0 runtime**.

## Hypothesis under test

V1 tested a narrower product-decision qualification thesis:

> A product-decision qualification engine can materially improve product-architecture judgement by identifying the correct consequential decision, representing candidate-changing variables directionally, enforcing evidence/claim ceilings, stress-testing the preferred direction with disconfirming evidence, and freezing only the decision depth actually supported by evidence.

The intended value was not simply more cautious output.

The target was:

> fewer premature product decisions without a corresponding rise in false unresolved states, unnecessary research, or framework ceremony.

## Candidate mechanics

The V1 candidate focused on six mechanisms:

1. Decision Question Lock
2. Evidence / Claim Ceiling
3. Directional Discriminator Contract
4. Explicit Disconfirming Evidence
5. Minimum Discriminating Evidence
6. Downstream Scope Ceiling

The candidate deliberately did not add PDR persistence, decision graphs, generic PM frameworks, UX heuristic libraries, implementation conformance, or integration infrastructure.

## Frozen comparator set

Wave 02 tested six primary lanes on every case:

- **A** — frontier model, no dedicated skill
- **B** — minimal decision-discipline prompt baseline
- **C** — LobeHub Product Design
- **D** — Maoxuan Product Decision Agent
- **E** — LobeHub Product Design + Product Agents Evidence Loop composition
- **F** — PAR V1 candidate

A secondary high-risk lane used Agent Decision Gates / Consult on four cases.

Frozen public comparator commits:

- LobeHub Product Design: `322a462b26527de92918a01d24997429fc8dc815`
- Maoxuan Product Decision Agent: `4e73dff057ef24a1acc185b03e384769e3961e65`
- Product Agents Evidence Loop: `5a478f92e60019efbbfcd7f9062459d651c3e6c2`
- Agent Decision Gates: `29debeba423cda2078e5c9f730a8714c3255c7f5`

## Test size

- 8 hostile cases
- 6 primary lanes
- 48 primary executions
- 4 secondary challenge executions
- **52 total planned and completed executions**

The cases attacked:

- downstream confidence leakage;
- premature freeze;
- unnecessary questioning;
- evidence-modality laundering;
- research theater;
- false unresolved / caution tax;
- forced material UX distinctions;
- missed upstream reframing;
- aggregate evidence hiding meaningful cohort conflict.

## Candidate identity

Candidate ZIP SHA-256 produced by the isolated builder:

`4aa2e882155b4068a751e246425666cb180df00018b0f1712c9b2d1e9d887d55`

Harness-reported aggregate candidate SHA-256:

`65f58907f4536b66242962b513c7db56fd24c8a567ce658b4ce0c0bb3295c57c`

The candidate was frozen before Wave 02 execution.

## Final result

The frozen harness returned:

> **FAIL — KEEP V0**

Key observations:

- V1 had **0 fatal failures** across the primary evaluation.
- V1 passed **7 / 8 targeted behaviors**.
- It nevertheless failed mandatory **CASE-01** by overclaiming exact administration placement after correctly identifying the stronger upstream operating-context decision.
- V1 materially beat the **Minimal Prompt Baseline on 3 / 8 cases**; the frozen acceptance threshold required at least 4 / 8.
- V1 materially beat **LobeHub Product Design on 2 / 8 cases**; the frozen acceptance threshold required at least 3 / 8.
- Its 7 / 8 targeted result did not establish enough separation from the short baseline prompt.
- The candidate was materially longer / more ceremonial without a corresponding qualification-quality advantage, triggering the frozen **ceremony-tax** failure.

The core falsification result is therefore:

> The additional V1 framework did not demonstrate enough capability beyond a strong base model plus concise decision-discipline instructions to justify a new release-level engine.

## Why this matters

The V1 mechanics were not useless. The candidate behaved safely and reproduced most targeted behaviors.

But the acceptance question was not whether the framework could work.

It was whether the framework produced a **material, defensible capability delta** over strong public alternatives and a minimal prompt.

It did not.

The correct product decision is therefore to keep the smaller, already-qualified V0 rather than ship a larger method with insufficient incremental value.

## Decision

**Do not merge the V1 candidate into the model-visible runtime.**

V0 remains:

**FROZEN / PASS / AUTHORITATIVE**

The following files remain intentionally unchanged from the tested V0 candidate:

- `SKILL.md`
- `references/**`
- `templates/**`

No V1 methodology change is authorized by Wave 02.

## Surviving micro-hypothesis

One recurring failure signature remains worth observing in real-product use:

> **Downstream confidence should not automatically inherit upstream confidence.**

A strong upstream semantic or operating-model conclusion may justify an architectural implication without justifying an exact navigation, placement, or interaction pattern.

This appeared as a bounded weakness in Wave 01 and again in Wave 02 CASE-01.

It is **not authorized as a V0 patch** from this result alone.

If the same failure recurs independently in real-product use, it may justify a future single-mechanism micro-candidate tested directly against frozen V0.

## Next authority

The next evidence source is **real-product use**.

Do not continue synthetic methodology expansion merely to increase framework completeness.

A future change should be driven by a repeated observed failure in real reviews, then tested as the smallest possible intervention.

## Evidence boundary

This document records the frozen Wave 02 harness verdict and execution summary.

The full raw Wave 02 execution directory was produced locally by the harness and is not included in this repository record unless separately archived later.
