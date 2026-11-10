# DecisionLens

> **Evidence-bound product and UX decisions.**

**DecisionLens** is the public name of the frozen **Product Architecture Review V0** agent skill. It helps teams distinguish consequential product decisions from unsupported assumptions. The internal skill identifier remains `product-architecture-review` to preserve the tested V0 runtime and compatibility with the existing install ZIP.

[Download the published V0 release](https://github.com/PeterxVarga/decisionlens-skill/releases/tag/v0) · [Worked examples](examples/) · [Benchmark evidence](benchmark/)

DecisionLens is a free agent skill for reviewing a landing page, SaaS/product interface, screenshots, or an early product concept through **consequential product and UX decisions** rather than generic audit checklists.

It does not promise the objectively best information architecture.

It tries to find the **strongest architecture defensible from the available evidence**.

## What makes it different

Most AI product reviews are optimized to produce answers.

DecisionLens is also allowed to conclude:

- `SUPPORTED`
- `REVISIT`
- `UNRESOLVED`
- `REFRAME`
- `IMMATERIAL_UX_DIFFERENCE`
- `NEEDS_REAL_WORLD_EVIDENCE`

Two behavioral rules define the skill:

> **Ask only questions whose answers could materially change the architecture.**

> **Refuse to manufacture certainty when the evidence is insufficient.**

The unit of analysis is a **consequential decision**, not a screen, issue count, heuristic score, or visual preference.

## Example

An early multi-client product appears to need a choice between:

- client-first navigation; or
- a cross-client work queue.

A generic review can choose one immediately.

Product Architecture Review first asks:

> When a returning operator starts a normal session, do they usually know which client they need — or are they trying to discover what needs attention across their portfolio?

If the answer changes, the recommended operating axis can change.

That is a **decision-flip question**.

See [`examples/`](examples/) for worked outputs.

## What it reviews

The skill routes between four surfaces:

- **LANDING** — comprehension, offer hierarchy, CTA architecture, information sequence, public IA
- **PRODUCT** — object model, navigation, workflows, state, actions, density, responsive architecture
- **EARLY** — user/job model, core objects, operating axis, initial IA, evidence before commitment
- **HYBRID** — keeps public acquisition and authenticated-product claims separate

## What it deliberately does not do

It is not:

- a generic “senior product designer” persona;
- a visual-design generator;
- a pixel-polish tool;
- a UI builder;
- a heuristic scorecard;
- a full accessibility or CRO audit by default;
- a system that uses competitor convention as proof.

It may identify when those forms of work are needed, but it stops at product-architecture judgement unless asked to continue.

## Default output

The default artifact is a concise **Product Architecture Note**:

```text
PRODUCT ARCHITECTURE NOTE

Evidence boundary

SUPPORTED
D-01 — ...

REVISIT
D-02 — ...

REFRAME
D-03 — ...

NEEDS REAL-WORLD EVIDENCE
D-04 — ...

Recommended architecture under current evidence
Most consequential open question
```

See [`templates/architecture-note.md`](templates/architecture-note.md).

## Install

### Codex

Download the **install ZIP**, not the full source ZIP, from the [V0 GitHub Release](https://github.com/PeterxVarga/decisionlens-skill/releases/tag/v0). On Linux/macOS with `curl`, `unzip`, and `sha256sum`:

```bash
curl -fL https://github.com/PeterxVarga/decisionlens-skill/releases/download/v0/product-architecture-review-v0-install.zip -o decisionlens-v0-install.zip
curl -fL https://github.com/PeterxVarga/decisionlens-skill/releases/download/v0/SHA256SUMS -o SHA256SUMS
mv decisionlens-v0-install.zip product-architecture-review-v0-install.zip
sha256sum -c SHA256SUMS --ignore-missing
mkdir -p ~/.agents/skills
unzip -q product-architecture-review-v0-install.zip -d ~/.agents/skills
test -f ~/.agents/skills/product-architecture-review/SKILL.md
```

The installed folder and skill identifier intentionally remain **`product-architecture-review`**, even though the project is branded **DecisionLens**. Do not rename or edit the seven frozen runtime files for a cosmetic rebrand. Restart the agent if it does not discover the skill immediately.

For a repository-scoped installation, extract the same archive inside `<repo>/.agents/skills/`. The source ZIP contains complete benchmark and example materials, but is not required for runtime installation.

### ChatGPT

Where Skills upload is available for your plan/workspace, upload the minimal skill ZIP or folder through the Skills interface. Availability and installation vary by ChatGPT plan/workspace.

The release is intentionally an ordinary Agent Skill directory: `SKILL.md` plus supporting references and templates.

## Use

You can invoke it explicitly:

```text
Use the product-architecture-review skill (DecisionLens) on this SaaS.
I care about the navigation and operating model, not visual styling.
```

```text
Review this early product idea.
Ask only questions that could materially change the architecture.
```

```text
Review this landing page and separate what is actually supported
from what still needs evidence.
```

Or let an agent select it when its trigger description matches the task.

## Validation

The exact V0 runtime (originally named Product Architecture Review) in this repository was frozen and tested in a controlled **6-case × 3-lane blind hostile bake-off**.

Lanes:

- **A** — same frontier model, no dedicated UX skill
- **B** — preselected case-matched public UX/product-design skill
- **C** — Product Architecture Review V0 (now presented as DecisionLens)

Result:

| Gate | Result |
|---|---:|
| Valid executions | **18 / 18** |
| PAR evidence-integrity fatals | **0** |
| PAR material wins vs baseline | **4 / 6** |
| PAR material wins vs case-matched public comparator | **5 / 6** |
| Targeted PAR behavior passes | **6 / 6** |
| PAR outputs marked discussion-worthy | **6 / 6** |

The strongest differences occurred when the correct behavior was to:

1. ask one architecture-changing question before deciding;
2. refuse to infer authenticated IA from marketing evidence;
3. reframe a navigation-placement question into an upstream product/context question;
4. preserve a “boring” incumbent when the evidence supported it.

Full methodology, frozen comparator commits, anonymized outputs, case judgements, limitations, and final review are under [`benchmark/`](benchmark/).

### What this benchmark does *not* prove

It does **not** establish universal UX superiority, real-world adoption, or a 99% “accuracy” rate.

The cases intentionally target this skill's capability thesis. The useful public claim is therefore bounded:

> **In a frozen 6-case blind hostile bake-off, Product Architecture Review V0 materially outperformed the preselected case-matched public comparator on 5 of 6 cases, with zero evidence-integrity failures.**

## Release authority

The model-visible runtime is preserved **byte-for-byte** from the tested candidate.

Frozen runtime ZIP SHA-256:

```text
21e7ade5125899a5c818f87fe758d64c2fa6a531ac25366ffbbd524d0d0a52f7
```

The `Status: V0 EXPERIMENTAL` line and `name: product-architecture-review` inside `SKILL.md` are intentionally retained because changing the tested model-visible file would create a new candidate. The GitHub repository branding is not a new runtime version. The frozen benchmark-runtime ZIP digest above is **not** the SHA-256 of the downloadable install ZIP; verify release downloads using the `SHA256SUMS` asset.

See [`RELEASE-AUTHORITY.md`](RELEASE-AUTHORITY.md).

## Provenance

This skill was independently written after a mechanism-level pattern harvest of public design/product skills.

See [`PROVENANCE.md`](PROVENANCE.md) for the source register and license boundary.

## License

MIT. See [`LICENSE`](LICENSE).

## Status

**V0 PUBLISHED / FROZEN** — GitHub release `v0` (2026-11-10). The original runtime identity and historical benchmark claims remain unchanged.

The next evidence source is real-product use, not additional pre-release methodology expansion.
