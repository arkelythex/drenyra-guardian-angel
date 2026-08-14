<div align="center">

<img width="1200" alt="Drenyra Guardian Angel flow — frozen candidate → independent review lenses → evidence → verification report" src="assets/branding/drenyra-guardian-angel-flow-banner.svg" />

<p><code>frozen candidate → independent review lenses → evidence → verification report</code></p>

</div>

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
| [Drenyra Command Center](https://github.com/arkelythex/drenyra-command-center) | Command Center (consumes) | In development (private) |
| [Drenyra AI](https://github.com/arkelythex/drenyra-ai) | Verifiable core — contracts source | Pre-alpha |
| [Drenyra Pi](https://github.com/arkelythex/drenyra-pi) | Pi-native harness (consumes, pinned) | Pre-alpha |
| [Drenyra Engram](https://github.com/arkelythex/drenyra-engram) | Institutional memory (used) | Pre-alpha |
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
