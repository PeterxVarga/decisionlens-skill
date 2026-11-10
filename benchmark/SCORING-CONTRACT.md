# ADJUDICATION SCORING CONTRACT

## Purpose

Score blind outputs against the case authority and the capability thesis.

Do not score:
- visual polish;
- verbosity;
- agreement with a preferred aesthetic;
- number of recommendations.

## Per-output dimensions

Score each 0–4.

### D1 — Consequential decision discovery — weight 20%
4: isolates the true high-impact product/UX decisions and avoids trivial noise.  
3: mostly correct with minor omissions.  
2: mixed consequential and generic findings.  
1: mostly issue/checklist-level.  
0: misses the governing decision.

### D2 — Decision-flip question quality — weight 15%
Score especially where follow-up was possible.
4: asks minimal, directional questions that materially change the decision.  
0: asks generic/taste questions or confidently guesses instead.

If genuinely no question was needed, score based on correct restraint.

### D3 — Evidence discipline — weight 15%
4: cleanly distinguishes supplied facts, missing evidence, inference and precedent.  
0: fabricates or upgrades weak evidence into fact.

### D4 — Correct uncertainty / refusal — weight 10%
4: calibrates confidence and refuses when evidence is insufficient.  
0: false certainty.

### D5 — Reframe quality — weight 10%
4: identifies the upstream question when the apparent UX question is downstream.  
0: remains trapped in the presented frame.

### D6 — Candidate quality / steelmanning — weight 10%
4: credible alternatives, no strawman, relevant incumbent preserved when warranted.

### D7 — Adversarial strength — weight 5%
4: materially tests the preferred direction and recognizes missing candidate/hybrid risks.

### D8 — Non-obvious decision value — weight 5%
4: produces a useful judgement beyond generic UX advice.

### D9 — Founder/designer usefulness — weight 5%
4: actionable decision clarity without overclaiming.

### D10 — Shareability / public-interest value — weight 5%
4: contains at least one concise, discussion-worthy judgement suitable for a public Product Architecture Note.

## Weighted score

`SUM(dimension_score / 4 * weight)`

Maximum 100.

## Fatal gates

Mark `FATAL` if any occur:

F1 — fabricated real user behavior/telemetry/product fact.  
F2 — marketing/public surface presented as authenticated product behavior.  
F3 — competitor/best-practice prevalence used as decisive product-specific proof.  
F4 — forced confident winner in a case intentionally underdetermined by authority.  
F5 — ignores explicit decisive telemetry/constraint.  
F6 — majority of follow-up questions are low-value and the run fails to reach the decisive variable when it was available.  
F7 — prohibited authority/retrieval contamination.  
F8 — substitutes implementation/redesign output for the requested architecture judgement.

A fatal does not necessarily mean the prose has no useful content; it means the run fails this benchmark's core thesis.

## Pairwise judgement

After scoring the three anonymous outputs for a case, rank:
1st / 2nd / 3rd.

Also answer:
- Which output best identified the consequential decision?
- Which showed the strongest epistemic behavior?
- Which would a strong founder/designer most want to read?
- Was the difference MATERIAL or IMMATERIAL?

Do not infer which lane produced which output.
