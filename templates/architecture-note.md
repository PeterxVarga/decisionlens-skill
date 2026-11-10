# PRODUCT ARCHITECTURE NOTE

**Product:** {{product}}  
**Surface:** {{surface}}  
**Maturity:** {{maturity}}

## Evidence boundary

{{what_can_and_cannot_be_established}}

{{#supported}}
## SUPPORTED

### {{decision_id}} — {{decision_question}}

**Direction:** {{direction}}  
**Confidence:** {{confidence}}

{{reasoning}}

**What would reopen this:** {{reopen_condition}}
{{/supported}}

{{#revisit}}
## REVISIT

### {{decision_id}} — {{decision_question}}

**Recommended direction:** {{direction}}  
**Confidence:** {{confidence}}

{{reasoning}}

**Strongest counter-case:** {{counter_case}}

**What would change the recommendation:** {{reopen_condition}}
{{/revisit}}

{{#unresolved}}
## UNRESOLVED

### {{decision_id}} — {{decision_question}}

{{why_unresolved}}

**Missing decision-flip evidence:** {{missing_evidence}}
{{/unresolved}}

{{#reframe}}
## REFRAME

### {{decision_id}} — {{apparent_question}}

The more important decision is:

**{{reframed_question}}**

{{why}}
{{/reframe}}

{{#immaterial}}
## IMMATERIAL UX DIFFERENCE

### {{decision_id}} — {{decision_question}}

{{why_immaterial}}

If implementation must choose, use: {{non_ux_tiebreaker}}
{{/immaterial}}

{{#real_world}}
## NEEDS REAL-WORLD EVIDENCE

### {{decision_id}} — {{decision_question}}

**Unknown:** {{flip_variable}}  
**Minimum evidence:** {{test}}  
**Decision rule:** {{decision_rule}}
{{/real_world}}

## Recommended architecture under current evidence

{{synthesis}}

## Most consequential open question

{{open_question}}
