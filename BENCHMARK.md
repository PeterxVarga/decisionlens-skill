# Product Architecture Review V0 — Hostile Bake-off Wave 01

## Verdict

# PASS — PUBLISH V0

Wave 01 was a controlled falsification test of one narrow hypothesis:

> Does Product Architecture Review produce materially better consequential product-decision judgement and epistemic behavior than a strong base model and a strong case-matched public UX/product-design skill?

## Design

Six frozen cases × three lanes:

- **Lane A:** frontier model without a dedicated UX skill
- **Lane B:** public case-matched comparator frozen before outputs were observed
- **Lane C:** exact Product Architecture Review V0 runtime

Every execution used a fresh model thread.

The first wave was closed-evidence: no lane could browse for additional product facts. This isolated decision methodology rather than research retrieval.

Outputs were anonymized into X/Y/Z before case adjudication. Lane identities were revealed only after all six case judgements were locked.

## Results

| Measure | A | B | PAR V0 |
|---|---:|---:|---:|
| Mean rubric score* | 75.21 | 74.17 | 99.38 |
| Material PAR wins against lane | — | **5/6** | — |

Additional gates:

- valid executions: **18/18**
- PAR evidence-integrity fatals: **0**
- PAR material wins vs baseline A: **4/6**
- PAR material wins vs comparator B: **5/6**
- PAR targeted behavior passes: **6/6**
- PAR discussion-worthy outputs: **6/6**

\*The rubric is deliberately aligned to the capability thesis and should not be interpreted as a universal UX quality/accuracy percentage.

## Case results

| Case | Capability under attack | C > A material | C > B material | PAR targeted behavior |
|---|---|---:|---:|---:|
| 01 | overturn weak incumbent from recurring-work evidence | YES | YES | PASS |
| 02 | defend sound dense incumbent / avoid novelty bias | NO | NO | PASS |
| 03 | landing architecture without false convergence | YES | YES | PASS |
| 04 | decision-flip questioning before commitment | YES | YES | PASS |
| 05 | refuse authenticated-IA hallucination | YES | YES | PASS |
| 06 | reframe navigation into upstream Team/context semantics | NO | YES | PASS |

## Frozen public comparators

The Lane B mapping was chosen before outputs were observed:

| Case | Comparator | Exact commit |
|---|---|---|
| 01 | Opikat / Design Expert | `eb392da9803fd43a9a7fe68740f76f5397fe1549` |
| 02 | AjnasNB / Web App UX Auditor | `6252a1a92efe40da50836f1ad5294c293c6443d0` |
| 03 | sshahzaiib / Senior Product Designer | `7103331faf4771ec53f800d5be055ccc19e29f05` |
| 04 | 0furkancolak / Frontend UI Prototype | `385f1b09bcb8f449c17849b91faa18dbc76bbd9a` |
| 05 | Opikat / Design Expert | `eb392da9803fd43a9a7fe68740f76f5397fe1549` |
| 06 | Opikat / Design Expert | `eb392da9803fd43a9a7fe68740f76f5397fe1549` |

## Strongest evidence

### CASE-04 — One question before the architecture

PAR did not select client-first or work-first from the concept description.

It first asked whether recurring sessions start with a known client or with portfolio-wide attention discovery.

Only after the response supplied the decisive distribution did it recommend a work-first operating surface.

The baseline and public comparator both committed before obtaining that evidence.

### CASE-05 — Useful refusal

The founder requested authenticated navigation from marketing-only evidence.

PAR refused to translate public product-page taxonomy into authenticated product facts, while still giving a provisional product model and the minimum evidence required to decide.

### CASE-06 — Reframe first

The apparent question was whether `Teams` belongs in Settings or the sidebar.

PAR separated two jobs:

- active-Team context/switching;
- Team administration.

That upstream distinction governed the navigation question.

## Limitations

This benchmark should be read as a test of a **specific capability thesis**, not as proof that PAR is universally better at UX.

Important limitations:

1. Cases intentionally stress PAR's claimed mechanics.
2. Cases are controlled/synthetic rather than evidence of real-world adoption.
3. Runner and blind judge used the same broader model environment.
4. Lane B is a strong finite comparator set, not every possible UX method/configuration.
5. The first wave isolates decision reasoning and does not test open-web research quality.

## Reproducibility material

This repository includes:

- frozen case prompts and hidden authorities;
- scoring and acceptance contracts;
- comparator authority/mapping;
- anonymized outputs;
- blind case judgement JSON;
- final verdict;
- final post-run evidence review.

See [`benchmark/`](benchmark/).
