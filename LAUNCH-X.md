# X Launch Copy

## Recommended launch post

Most AI UX reviews have a failure mode:

**they answer every question.**

I built **Product Architecture Review** to do something harder:

- find the product decisions that actually matter;
- ask only questions that could change those decisions;
- refuse to manufacture certainty when the evidence is insufficient.

I tested V0 in a frozen 6-case blind hostile bake-off against a base model and preselected case-matched public UX skills.

**PAR materially beat the public comparator on 5/6 cases, with zero evidence-integrity failures.**

The interesting part wasn't “better UX advice.”

It was behavior like:

→ asking one question before choosing the IA  
→ refusing to infer authenticated navigation from a marketing site  
→ defending a dense table when cards would make the workflow worse  
→ reframing “where should this nav item go?” into the upstream product-model question

It's free.

**Give it a product. See which architecture decisions you can actually defend.**

https://github.com/PeterxVarga/product-architecture-review

---

## Thread version

### 1/7

I built a free agent skill called **Product Architecture Review**.

The premise:

> The goal isn't to produce more UX recommendations.  
> The goal is to identify the strongest architecture defensible from the available evidence.

### 2/7

Its atomic unit isn't a screen or heuristic violation.

It's a **consequential decision**.

Examples:

- client-first vs work-first operating model;
- global object vs scoped view;
- dashboard vs attention queue;
- first-class workspace context vs admin destination.

### 3/7

The rule I care about most:

**Don't ask a question unless plausible answers could materially change the architecture.**

In one benchmark case, the entire first move was basically:

> Does the operator normally know the client, or first discover urgent work across the portfolio?

The answer flipped how the IA should be organized.

### 4/7

Second rule:

**Uncertainty is a valid output.**

The skill can return:

SUPPORTED  
REVISIT  
UNRESOLVED  
REFRAME  
IMMATERIAL_UX_DIFFERENCE  
NEEDS_REAL_WORLD_EVIDENCE

If a marketing site doesn't tell us how the authenticated product works, it doesn't invent it.

### 5/7

I tried to falsify the idea before publishing it.

Frozen test:

- 6 hostile cases
- 3 lanes
- 18 fresh executions
- base model
- preselected case-matched public skill
- PAR V0
- blind X/Y/Z adjudication before lane reveal

### 6/7

Result:

- 18/18 valid
- 0 PAR evidence-integrity failures
- PAR > baseline materially on 4/6
- PAR > public comparator materially on 5/6
- 6/6 targeted behaviors passed

This is a controlled methodology test, not a claim of universal UX superiority.

### 7/7

Now the useful test is real products.

Reply with:

- a URL,
- screenshots,
- or an early product concept.

I'll run Product Architecture Review and publish the most consequential decision it finds.

https://github.com/PeterxVarga/product-architecture-review

---

## Short variant

Built a free skill: **Product Architecture Review**.

It doesn't score your UX.

It finds the architecture decisions you can defend — and the ones you can't yet.

Blind hostile bake-off:
- 18/18 valid runs
- 0 evidence-integrity failures
- 5/6 material wins vs preselected case-matched public UX skills

Now I want to break it on real products.

Reply with a URL / screenshots / product concept.

https://github.com/PeterxVarga/product-architecture-review

---

## Reply CTA

Drop a product URL, 3–8 screenshots, or an early concept.

I'll return a Product Architecture Note focused on the **one or two decisions most likely to change the product**, not a generic UX checklist.
