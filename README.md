# Product Architecture Review

> **Give me a product. I’ll identify the architecture decisions you can defend — and the ones you can’t yet.**

Product Architecture Review is a free agent skill for reviewing a landing page, SaaS/product interface, screenshots, or an early product concept through **consequential product and UX decisions** rather than generic audit checklists.

It does not promise the objectively best information architecture.

It tries to find the **strongest architecture defensible from the available evidence**.

## What makes it different

Most AI product reviews are optimized to produce answers.

Product Architecture Review is also allowed to conclude:

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

Current Codex skill discovery supports user-installed skills under:

```bash
$HOME/.agents/skills/
```

Install this repository as:

```bash
mkdir -p ~/.agents/skills
cp -R product-architecture-review ~/.agents/skills/product-architecture-review
```

Then restart Codex if the skill does not appear immediately.

You can also place a repository-scoped copy under:

```text
<repo>/.agents/skills/product-architecture-review/
```

### ChatGPT

Where Skills upload is available for your plan/workspace, upload the minimal skill ZIP or folder through the Skills interface. Availability and installation vary by ChatGPT plan/workspace.

The release is intentionally an ordinary Agent Skill directory: `SKILL.md` plus supporting references and templates.

## Use

You can invoke it explicitly:

```text
Use Product Architecture Review on this SaaS.
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

The exact V0 runtime in this repository was frozen and tested in a controlled **6-case × 3-lane blind hostile bake-off**.

Lanes:

- **A** — same frontier model, no dedicated UX skill
- **B** — preselected case-matched public UX/product-design skill
- **C** — Product Architecture Review V0

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

The `Status: V0 EXPERIMENTAL` line inside `SKILL.md` is intentionally retained because changing the tested model-visible file would create a new candidate. The release wrapper is frozen for publication; the tested runtime itself is unchanged.

See [`RELEASE-AUTHORITY.md`](RELEASE-AUTHORITY.md).

## Provenance

This skill was independently written after a mechanism-level pattern harvest of public design/product skills.

See [`PROVENANCE.md`](PROVENANCE.md) for the source register and license boundary.

## License

MIT. See [`LICENSE`](LICENSE).

## Status

**V0 FROZEN / PUBLICATION GATE OPEN**

The next evidence source is real-product use, not additional pre-release methodology expansion.
