# Drenyra Guardian Angel — Codebase Guide

Maintainer-oriented map of this repository: where things live, what may depend on what, what is frozen, and how to validate a change. For the conceptual architecture, read [Architecture](architecture.md) and [Intended Usage](intended-usage.md) first.

> [!IMPORTANT]
> **This repository is the verification layer, never the author.** Every change must preserve the guardian invariants: independence, cited evidence, and strict read-only over frozen candidates.

---

## Repository map

```text
assets/branding/BRAND.md     Brand source + banner regeneration (brand-system v0.3)
docs/                        Intended usage, codebase guide, architecture
LICENSE                      Proprietary — never edited
README.md                    Positioning-first project overview (quality bar)
AGENTS.md                    Agent rules: doctrine, read-first, where changes belong
AI_POLICY.md                 AI-assisted contribution policy
CONTRIBUTING.md              Contribution workflow
CHANGELOG.md                 Keep a Changelog — all history under [Unreleased]
```

The verification lenses and tooling land under `src/` as they are built
(SDD-090); nothing in this repository executes yet. There is no package
manifest, no CI, and no test toolchain today.

---

## Layering (who may import whom)

The repository is currently documentation-only, so the layering rules are the
rules of the ecosystem position — they become import rules when `src/` lands:

```text
drenyra-ai contracts/         normative, versioned, FROZEN (candidate, receipt,
                              gate, ledger, recovery) — published versions only
        ▼
Guardian Angel verification   consumes the frozen surface; never depends on
                              private internals, a checkout, or other satellites
        ▼
reports                      verdicts and evidence to the ecosystem; never
                              approval, authority, or mutation
```

Rules that matter every day:

1. **Frozen surface.** Verification input is the published `drenyra-ai` contracts — published, versioned artifacts, never a checkout or private internals.
2. **One direction.** Satellites (including this repo) consume `drenyra-ai`; `drenyra-ai` never depends on them. This repo never depends on Command Center, Pi, Engram, or Skills.
3. **Read-only.** The verification target is frozen before any check; the Guardian Angel never mutates, executes, or persists changes to it.
4. **No authority.** Verdicts report (`APPROVED`/`ESCALATED`); they never grant approval, authority, or delivery.
5. **No reverse surface.** Changes to the contracts themselves belong upstream in `drenyra-ai` and are a major event there.

---

## Where a change goes

| Kind of change | Lands in | Also update |
| --- | --- | --- |
| Documentation (usage, architecture, guide) | `docs/` | the documentation index in README, CHANGELOG |
| Brand asset or prompt | `assets/branding/` | pass the brand-conformance checker (see [BRAND.md](../assets/branding/BRAND.md)) |
| Verification-model change (refutation, dual review, evidence, two-round rule) | `docs/architecture.md` + `docs/intended-usage.md` | treat as a breaking change; document the migration explicitly |
| Verification tooling (when `src/` lands) | `src/` + its tests | docs-as-code, CHANGELOG |
| License | never | — |

---

## Invariants

These are checked by maintainer review. A change is **not done** until all hold:

- **Independence.** The reviewer is never the author, approver, or executor of what it verifies.
- **Read-only doctrine.** Frozen candidates are never mutated, executed, or persisted by the reviewer.
- **Evidence, not narration.** Every finding cites persisted evidence or a receipt; transcripts prove nothing.
- **No invented findings.** Findings come from inspection of the frozen target against the frozen contracts — never from plausible-sounding claims.
- **Frozen contracts as published.** The verification surface is the published `drenyra-ai` contracts; drift is a defect.
- **Fiscal safety.** Money is BigInt cents, never floats; RUC/company/period scope is mandatory in every check; no data across RUCs without explicit context.
- **No AI attribution.** Conventional Commits only; no `Co-Authored-By` or "Generated with" markers.

---

## Testing and validation

- **No automated suite exists yet.** Documentation and model changes are validated by maintainer review against the quality bar and the guardian doctrine.
- **Brand changes:** run the `drenyra-ai` brand-conformance checker exactly as documented in [BRAND.md](../assets/branding/BRAND.md) (palette shape, dual-theme SVG scan, raster coverage ≥ 0.92). A brand asset that fails the checker is not committable.
- **Markdown:** render cleanly on GitHub; keep tables well-formed.

---

## Conventions

- **Conventional Commits**, no AI attribution. `feat|fix|docs|refactor|test|chore|ci|build|style|perf|revert(scope): message`.
- **Docs-as-code.** A behavioral or model change ships with its docs in the same change.
- **Neutral professional register, English.** All artifacts are public-facing ecosystem documentation.
- **Facts over aspiration.** Version, status, and dependency claims must match the verified ecosystem state (see the README ecosystem table); never present planned work as shipped.

---

## Read next

- [Architecture](architecture.md) — ecosystem position, core invariants, and the review lifecycle
- [Intended Usage](intended-usage.md) — the frontier and the responsibility split
- [CONTRIBUTING](../CONTRIBUTING.md) — the contribution workflow
- [README](../README.md) — the project overview at the ecosystem quality bar
