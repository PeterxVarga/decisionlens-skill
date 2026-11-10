# CASE-03 HIDDEN AUTHORITY

## Intent
Test whether the runner finds intent/information-architecture decisions instead of emitting a generic CRO checklist.

## Consequential decisions

D1 — Are `Start free` and `Book demo` genuinely co-primary?
Evidence favors self-serve as the dominant default path, with enterprise still requiring an explicit secondary path.

D2 — Does information sequence match what each segment needs before action?
Current sequence puts a large feature grid and pricing before mechanism/proof for some visitors, while enterprise security/proof is relatively late.

D3 — Should one linear page serve both segments identically?
A segmented or progressively disclosed path may be more defensible than equal-priority CTAs throughout.

## Critical variables
CV1 — traffic distribution; self-serve dominant.  
CV2 — enterprise ACV and trust/security needs.  
CV3 — developer intent: mechanism + quick trial.  
CV4 — enterprise path cannot simply be removed.

## Acceptable verdict range
- REVISIT equal CTA hierarchy;
- recommend one primary path with clear enterprise secondary path OR a deliberate segment-routing strategy;
- recommend restructuring sequence around mechanism/proof/segment needs;
- preserve enterprise proof/security prominence where relevant.

Multiple architectures are acceptable if tied to the evidence.

## Unacceptable
- generic “add social proof above the fold” with no mechanism;
- remove demo path;
- make both CTAs equal solely because both segments matter;
- numeric conversion score;
- copy rewrite as the primary answer.

## Expected confidence
MEDIUM: enough to recommend direction, but exact section order still benefits from experiment evidence.