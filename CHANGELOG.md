# Changelog

<!-- markdownlint-disable MD024 -->

All notable changes to Drenyra Guardian Angel will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).
This repository has no releases yet: everything is under `[Unreleased]` and
versioning begins when the first release ships.

## [Unreleased]

### Added

- **Repository scaffold** — README, LICENSE, `.gitignore`, and the branding assets directory. (2026-08-10, `37b6d77`)
- **Ecosystem table points at Drenyra Command Center** as the web-application consumer. (2026-08-10, `63483ad`)
- **Brand-conformance acceptance threshold tightened** to coverage ≥ 0.92 in `assets/branding/BRAND.md`. (2026-08-10, `c282ed7`)
- **BRAND.md uses a sibling-relative brand-conformance path** (`../drenyra-ai/scripts/brand-conformance.mjs`) — no host-specific absolute paths. (2026-08-11, `1441bdd`)
- **BRAND.md points at the upgraded art-direction Shared DNA** in the ecosystem creative brief. (2026-08-11, `ef9f485`)
- **README references the Drenyra Dominion Program** — SDD-090 (Guardian Angel) and SDD-040 (Receipt-Driven Accounting v2). (2026-08-11, `9269893`)
- **README visual flow** — flow banner and visual-flow section. (2026-08-14, `eb7c3a8`, `138dfe8`; later removed with the README rewrite)
- **Documentation set at the ecosystem quality bar** — README rewrite (positioning-first, In development/public status), AGENTS.md, AI_POLICY.md, CONTRIBUTING.md, CHANGELOG.md, and `docs/` (intended-usage, CODEBASE-GUIDE, architecture) describing the verification model: refutation, blind dual review, evidence checks, and the bounded two-round rule over frozen `drenyra-ai` contracts. (2026-08-19)

### Changed

- **README ecosystem repo visibility and statuses corrected** to the verified ecosystem state: Command Center In development (public), Drenyra AI Alpha (v0.5.0), Engram Alpha (v0.2.1). (2026-08-19, `8791400`)
- **README restated at the quality bar** — the repository is public and **In development**, replacing the previous "private" and "Pre-alpha" claims; the verification tooling is explicitly documented as planned under SDD-090. (2026-08-19)
