# Drenyra Guardian Angel — Agent Guide

This file is for AI agents and their humans working in this repository. It answers: *what are the non-negotiable rules, what should I read first, and where do changes belong?*

> [!IMPORTANT]
> **This repository is the verification layer, never the author.** A change that turns the Guardian Angel into the author, approver, or executor of what it reviews is a product defect, not a design choice.

## Non-Negotiable Rules

Every change — code, docs, tests, or CI — must respect these. They are the guardian doctrine and are enforced by maintainer review.

1. **Never the author of what it reviews.** The Guardian Angel is an independent lens over frozen candidates and receipts. It never produces the work it verifies.
2. **Strictly read-only over frozen candidates.** The target of a verification is frozen before any check starts; the Guardian Angel never mutates, executes, or persists changes to it.
3. **Evidence is cited, never invented.** Every finding must cite the persisted evidence or receipt that proves it. A finding without evidence is not a finding.
4. **No invented findings.** Findings come from inspection of the frozen target against the applicable frozen contracts — never from plausible-sounding claims, transcripts, or narration.
5. **Reviewer sovereignty.** Review runs blind and independent: two judges inspect the identical target with identical criteria, each returns one neutral result, and neither sees the other's work. Scope is fixed before launch and never changes mid-review.
6. **Not part of the approval quorum.** The Guardian Angel reports `APPROVED`/`ESCALATED` verdicts; it never approves, rejects, or performs fiscal approval. Approval is an explicit human/R2/R3 event in the candidate lifecycle.
7. **Fiscal conventions.** Monetary values are BigInt cents (never floats); RUC/company/period scope is mandatory in every check; no data across RUCs without explicit context.
8. **Contracts are frozen public surface.** The verification surface is the published `drenyra-ai` contracts (`candidate`, `receipt`, `gate`, `ledger`, `recovery`) — published versions, never private internals. Drift from the frozen contracts is a defect.
9. **No AI attribution.** Conventional Commits only. No `Co-Authored-By`, `Reviewed-by`, or "Generated with" markers.

## Read Before Working

| Goal | Start here |
| --- | --- |
| Understand what the project is and is not | [Intended Usage](docs/intended-usage.md) |
| The verification model and review lifecycle | [Architecture](docs/architecture.md) |
| Codebase layout and conventions | [Codebase Guide](docs/CODEBASE-GUIDE.md) |
| The frozen contracts the verification consumes | [drenyra-ai Contracts](https://github.com/arkelythex/drenyra-ai/tree/main/contracts) |
| Contribution workflow | [CONTRIBUTING](CONTRIBUTING.md) |
| Contribution rules with AI assistance | [AI Policy](AI_POLICY.md) |

## Where Changes Belong

```text
assets/branding/    Brand source and banner regeneration (brand-system v0.3)
docs/               Intended usage, codebase guide, architecture
src/                Verification lenses and tooling (planned — SDD-090)
LICENSE             Proprietary — never edited
```

- A **documentation** change goes in `docs/` and updates the documentation index in [README](README.md) in the same change (docs-as-code).
- A **brand** change goes in `assets/branding/` and must keep the `brand-system` palette and the conformance checker green (see [BRAND.md](assets/branding/BRAND.md)).
- A **verification-model** change (refutation, blind dual review, evidence checks, the two-round rule) goes into the architecture and intended-usage docs first — the model is the contract this repository is built to execute.
- The **verification surface** is the frozen `drenyra-ai` contracts. Changing how this repository consumes them never changes the contracts themselves; a contract change belongs upstream in `drenyra-ai` and is a major event there.
- `LICENSE` is never edited.

## Skills

Verification work in this ecosystem follows the Drenyra adversarial-review discipline: blind dual review, refutation, evidence checks, and the bounded two-round rule. When working on the verification model or its tooling, load the relevant adversarial-review skill for the task **before** writing — the Drenyra ecosystem publishes its skills through [drenyra-skills](https://github.com/arkelythex/drenyra-skills); this repository does not yet ship a local skill registry. The reviewer's job is to find faults, not to be fair to the candidate.
