# Drenyra Guardian Angel

**Independent adversarial verification for fiscal work.** Pre-alpha.

> [!IMPORTANT]
> **Private commercial product** — this repository is **private**; distribution
> of artifacts is contractual, never public. Use, copy, and distribution remain
> governed by the [LICENSE](LICENSE) (proprietary, © Arkelythex).

## Role in the ecosystem

The Guardian Angel is the ecosystem's independent, adversarial, continuous
verification layer for accounting and fiscal work. It is the fiscal-domain
counterpart of
[`gentleman-guardian-angel` (gga)](https://github.com/Gentleman-Programming/gentleman-guardian-angel) —
same posture (independent reviewer, never the author), stricter controls
(fiscal risk is not a merge conflict).

It **verifies adversarially** (refutation, dual distinct review, evidence
checks) and **never performs fiscal approval** — approval is an explicit
human/R2/R3 event recorded in the candidate lifecycle.

| Ecosystem project | Role | Status |
| --- | --- | --- |
| [Drenyra Command Center](https://github.com/arkelythex/drenyra-command-center) | Command Center (consumes) | In development (public) |
| [Drenyra AI](https://github.com/arkelythex/drenyra-ai) | Verifiable core — contracts source | Alpha (v0.5.0) |
| [Drenyra Pi](https://github.com/arkelythex/drenyra-pi) | Pi-native harness (consumes, pinned) | Pre-alpha |
| [Drenyra Engram](https://github.com/arkelythex/drenyra-engram) | Institutional memory (used) | Alpha (v0.2.1) |
| [Drenyra Skills](https://github.com/arkelythex/drenyra-skills) | Versioned accounting/tax knowledge | In development |
| **Drenyra Guardian Angel** | Independent adversarial verification | **This repo** |

**Direction rule:** the Guardian Angel consumes the **frozen contracts** of
[`drenyra-ai`](https://github.com/arkelythex/drenyra-ai) (`candidate`, `receipt`,
`gate`, `ledger`, `recovery`, `brand-system`) as its public surface — published
versions, never private internals. It never claims SUNAT, bank, or ERP
execution, and never performs fiscal approval.

## Posture

- **Independent**: never the author of what it reviews; a separate lens.
- **Adversarial**: seeks refutation, not confirmation — candidate-caused severe
  findings block; pre-existing/base findings become follow-ups.
- **Evidence-first**: decides from persisted evidence and receipts, never from
  transcripts.
- **Fiscal-safe**: RUC/company/period scope enforced in every check; no data
  across RUCs without explicit context.

### Drenyra Dominion Program

The Guardian Angel is one vertical inside the
[Drenyra Dominion Program](https://github.com/arkelythex/drenyra-ai/tree/main/openspec/programs/drenyra-dominion),
the federated program master that fixes vision, authority, contracts,
dependencies, gates, and sequencing across every Drenyra repository. A single
master SDD governs the ecosystem; implementable vertical SDDs deliver complete
capabilities that may traverse the repositories they need while each
repository preserves its own ownership and boundaries.

| Program vertical | This repo's role |
| --- | --- |
| [SDD-090 — Guardian Angel](https://github.com/arkelythex/drenyra-ai/tree/main/openspec/programs/drenyra-dominion/sdds/sdd-090-guardian) | Independent, adversarial, strictly read-only verification over frozen candidates |
| [SDD-040 — Receipt-Driven Accounting v2](https://github.com/arkelythex/drenyra-ai/tree/main/openspec/programs/drenyra-dominion/sdds/sdd-040-rda-v2) | Provides frozen candidates with exact identity and evidence for review |

**Guardian doctrine:** strictly read-only over frozen candidates; never part
of the approval quorum; never approves, executes, or mutates candidates.

## Structure

```text
assets/branding/BRAND.md     brand + banner regeneration (brand-system v0.2)
docs/                        posture, lenses, runbooks (planned)
src/                         verification lenses (planned)
LICENSE                      proprietary, © Arkelythex
```

## Brand

All assets follow the [brand-system](https://github.com/arkelythex/drenyra-ai/blob/main/contracts/brand-system.md)
contract (v0.2 — dark + light themes, cyan/violet accents). The Guardian Angel
banner prompt (twin-lens shield motif) is in
[`assets/branding/BRAND.md`](assets/branding/BRAND.md) and the ecosystem set in
[`gpt-image-prompts.md`](https://github.com/arkelythex/drenyra-ai/blob/main/docs/assets/brand/gpt-image-prompts.md).

Proprietary. © 2026 Arkelythex. All rights reserved.
