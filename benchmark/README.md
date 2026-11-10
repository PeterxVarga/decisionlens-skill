# Benchmark transparency

This directory contains the public evidence needed to inspect the Product Architecture Review qualification work.

## Wave 01 — V0 hostile bake-off

Wave 01 contains the evidence used to qualify the frozen V0 release after lane reveal.

It intentionally includes the formerly hidden case authorities because the wave is complete.

Structure:

```text
benchmark/
├── cases/                 # Wave 01 model-facing case + hidden authority
├── outputs/               # Wave 01 anonymized X/Y/Z transcripts
├── judgements/            # Wave 01 locked blind case adjudications
├── SCORING-CONTRACT.md
├── ACCEPTANCE-CONTRACT.md
├── COMPARATOR-AUTHORITY.md
├── CASE-MAPPING.md
├── BLINDING-MAP.json
├── FINAL-VERDICT.json
├── FINAL-EVIDENCE-REVIEW.md
└── USAGE-REPORT.md
```

## Wave 02 — V1 falsification

A later V1 Decision Qualification Engine candidate was deliberately tested against a stronger frozen comparator stack, including a minimal prompt baseline and composed public-skill adversary.

Wave 02 completed 52 executions and returned:

**FAIL — KEEP V0**

The candidate was not merged into the model-visible runtime.

See [`WAVE02-V1-FALSIFICATION.md`](WAVE02-V1-FALSIFICATION.md) for the hypothesis, frozen comparator commits, acceptance failures, and surviving micro-hypothesis.

The full raw Wave 02 harness output was produced locally and is not represented here as a complete public artifact set unless separately archived later.

The controlled cases in both waves are methodology stress tests, not claims of real-world product validation.
