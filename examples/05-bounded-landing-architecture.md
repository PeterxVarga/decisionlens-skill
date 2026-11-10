# Bounded landing architecture

**Benchmark case:** CASE-03  
**Mechanic demonstrated:** direction without false convergence

## Situation

A landing page serves both self-serve developers and high-ACV enterprise prospects with two equal CTAs.

## Tested PAR V0 output

# PRODUCT ARCHITECTURE NOTE

**Product:** RelayFox  
**Surface:** LANDING  
**Maturity:** UNKNOWN

## Evidence boundary

This review uses the supplied page structure and stated segment behavior only. It can assess the logic of the acquisition journey, but cannot establish conversion performance, segment value, or the optimal CTA treatment without real traffic evidence.

## REVISIT

### D-01 — Should both commercial paths remain equally prominent in the hero?

**Recommended direction:** Keep both paths, but make the developer-led path primary and make the enterprise path explicitly segment-specific.  
**Confidence:** MEDIUM

With 65% developer-led inbound, “Start free” should be the dominant first action. Equal buttons make visitors resolve the company’s sales routing themselves. Preserve enterprise access, but label it for its job—e.g. “Enterprise demo”—and pair it with a nearby route to security/deployment evidence.

**Strongest counter-case:** If enterprise opportunities generate disproportionately more value and outbound visitors routinely land directly on this page, equal prominence may be commercially justified.

**What would change the recommendation:** Segment CTA clicks, workspace activation, demo qualification, and revenue attribution show equal treatment outperforms a developer-led hierarchy.

### D-02 — Should feature cards and pricing precede explanation of the mechanism?

**Recommended direction:** Move “How it works” ahead of feature detail and pricing.  
**Confidence:** MEDIUM

Developer-led visitors arriving from technical content need to validate the operating mechanism before evaluating a feature inventory or price. A compact mechanism section should explain what is autonomous, what humans control, and where RelayFox operates in the incident workflow. Feature cards can then substantiate that model.

**Strongest counter-case:** If the inbound links already explain the mechanism in detail and the landing page is primarily a conversion destination, an earlier feature/pricing path could be sufficient.

**What would change the recommendation:** Entry-page and scroll evidence shows most technical visitors already understand the mechanism and move directly to pricing or signup.

### D-03 — Should enterprise trust material remain late in the page?

**Recommended direction:** Surface enterprise proof earlier as a clearly accessible route; retain the fuller proof sequence later.  
**Confidence:** MEDIUM

Security, deployment, auditability, and customer proof are decision prerequisites for enterprise prospects—not supporting details after pricing. They need not displace the developer-led narrative, but should be available from the hero/navigation and introduced before a demo commitment. The current late placement risks asking enterprise visitors to convert before answering their core feasibility questions.

**Strongest counter-case:** A dense enterprise-first page may distract developer-led visitors and weaken self-serve activation.

**What would change the recommendation:** Enterprise session evidence shows prospects reliably consume the current lower-page material before booking, without material abandonment.

## NEEDS REAL-WORLD EVIDENCE

### D-04 — Is one shared page with segmented paths sufficient, or should RelayFox create a dedicated enterprise landing path?

**Unknown:** Whether enterprise visitors can reach required trust evidence without harming the dominant developer-led journey.  
**Minimum evidence:** Compare the current/shared-page path with a campaign-specific enterprise page or route; measure qualified-demo rate, security-review progression, and self-serve workspace activation by acquisition segment.  
**Decision rule:** Create a dedicated enterprise path if it materially improves qualified enterprise progression without reducing developer-led activation on the shared page.

## Recommended architecture under current evidence

Use one landing page with two intentional journeys:

1. Hero establishes the category and makes “Start free” primary; “Enterprise demo” is a visible secondary path.
2. Immediately explain the incident-response mechanism and human-control boundary.
3. Show product capabilities as evidence of that mechanism.
4. Present self-serve pricing once technical visitors can assess fit.
5. Introduce proof: customer evidence, security/compliance, deployment, and auditability.
6. Provide a stronger enterprise proof-and-demo path, including the case study.
7. End with segment-specific CTAs again, but not equal, generic duplicates.

Public navigation should help visitors self-route: Product/How it works, Pricing, Security, Enterprise, and Sign in/Start free. This is acquisition architecture only; it does not establish anything about the authenticated product’s navigation or behavior.

## Most consequential open question

Do enterprise prospects need a distinct proof-led acquisition experience, or can a shared page serve them through explicit routing and earlier trust evidence?

## Why this example matters

The skill can support changes to CTA hierarchy and information sequence while leaving the exact shared-vs-segmented architecture unresolved.
