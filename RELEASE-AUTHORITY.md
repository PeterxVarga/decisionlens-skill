# Release Authority — Product Architecture Review V0

## State

**PUBLIC RELEASE CANDIDATE:** V0  
**METHODOLOGY:** FROZEN  
**HOSTILE BAKE-OFF WAVE 01:** PASS  
**PRE-RELEASE METHODOLOGY PATCH:** NOT AUTHORIZED  
**NEXT EVIDENCE SOURCE:** REAL-PRODUCT / PUBLIC USE

## Exact tested runtime

Runtime ZIP:

`product-architecture-review-v0-runtime.zip`

SHA-256:

`21e7ade5125899a5c818f87fe758d64c2fa6a531ac25366ffbbd524d0d0a52f7`

The following model-visible files in the public repository are byte-identical to the tested candidate:

- `SKILL.md` — `727324b2783884dc3f2d9a3aec8e73226216dec6f36021b45d10c85096427bc9`
- `references/intake-and-routing.md` — `3a3ec5e04a25939100b9820775b82d8a502d89822678582c19b3bc1709b2b174`
- `references/product-and-ia-analysis.md` — `2aefc3420a9c10adc82062d52636539231be9ed8d47883688eaa9d9b24e81b14`
- `references/evidence-and-research.md` — `571769c5fa783812a041235a5199f0d76f77699c93ca4ba17494405e99b79573`
- `references/decision-adversary.md` — `b2a489403324c720692b822a921efd911a04b153416329b3ec71e9e161b6561c`
- `templates/architecture-note.md` — `aee067a8b1d170877662935232826244fb8ece70219bcf51f5a55519a21dde19`
- `templates/deep-review.md` — `63a1913f5c9d9a39b7bf9dc5e9fc7d36f0f6fd11f74e511022ce1fec7ea7dc6f`

## Packaging boundary

The following files are public-release packaging and were **not** part of the model-visible candidate during Wave 01:

- `README.md`
- `LICENSE`
- `RELEASE-AUTHORITY.md`
- `BENCHMARK.md`
- `LAUNCH-X.md`
- `PUBLIC-CLAIMS.md`
- `examples/**`
- `benchmark/**`
- repository manifest files

Changing those files does not change the tested runtime.

Changing `SKILL.md`, `references/**`, or `templates/**` creates a new model-visible candidate and must not be represented as the exact Wave 01 V0 authority.

## Note on `Status: V0 EXPERIMENTAL`

The tested `SKILL.md` contains the line:

`Status: V0 EXPERIMENTAL`

It is preserved intentionally. Rewriting it to `V0 FROZEN` would alter the tested model-visible bytes. The release status is therefore recorded in this wrapper file rather than silently mutating the candidate.
