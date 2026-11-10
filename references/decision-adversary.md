# Decision Adversary

## Purpose

Prevent first-answer anchoring and false certainty.

This reference is intentionally compact. It applies the core doctrine of the qualified UX Decision Adversary without reproducing qualification/eval internals.

## Step 1 — Frame one decision

One consequential question only.

Bad:
"How should the dashboard work?"

Good:
"Should returning users land on a cross-domain overview or directly on the active work queue?"

## Step 2 — Credible candidates

Minimum two when genuinely contested.

Steelman each:
- what task distribution makes it win?
- what constraint makes it safer?
- what evidence supports it?
- where does it fail?

Do not create a deliberately weak candidate.

## Step 3 — Flip variables

For every candidate identify variables that could reverse the ranking.

A flip variable must be directional.

Weak:
"user behavior"

Strong:
"if >70% of returning sessions begin by locating cross-domain exceptions, a work queue gains value over an overview."

## Step 4 — Provisional direction

Only after evidence/candidates.

Provisional is not frozen.

## Step 5 — Blind attack

Before auditing the provisional rationale, attack the provisional winner as if its justification were unavailable.

Ask:
- what hidden assumption is it relying on?
- what user cohort does it hurt?
- what failure/recovery case breaks it?
- is candidate C/hybrid missing?
- is the apparent decision actually downstream?
- could the difference be immaterial?

## Step 6 — Rationale audit

Now inspect:
- evidence class;
- applicability;
- symmetry;
- unsupported leaps;
- overreliance on precedent;
- synthetic evidence inflation.

## Step 7 — Converge

### SUPPORTED
A direction is strong and uncertainty is bounded.

### REVISIT
A direction can be recommended but the current/incumbent choice has meaningful weakness.

### UNRESOLVED
Available evidence cannot responsibly rank candidates.

### REFRAME
The decision is downstream of an unresolved upstream question.

### IMMATERIAL_UX_DIFFERENCE
The UX distinction is too small/non-consequential; use transparent non-UX tiebreakers.

### NEEDS_REAL_WORLD_EVIDENCE
A decision-flipping empirical variable requires observation/testing.

## Reopen contract

For SUPPORTED/REVISIT recommendations include concrete reopen conditions.

Good:
"Reopen if telemetry shows most returning sessions start with cross-client exception discovery rather than known-client work."

Bad:
"Reopen if user needs change."

## Symmetry

Do not:
- protect incumbent because it exists;
- prefer novelty because it is new;
- prefer cards/lists/sidebar/tabs by style;
- prefer complexity because it seems sophisticated;
- prefer simplicity unless UX is already immaterial or simplicity affects real task/error cost.
