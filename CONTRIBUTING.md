# Contributing to Drenyra Guardian Angel

Thank you for your interest in contributing to **Drenyra Guardian Angel** — the ecosystem's independent, adversarial, continuous verification layer for fiscal work.

> [!IMPORTANT]
> **Verification integrity is a product safety requirement.** This repository is the independent review lens of the Drenyra ecosystem. Never weaken the read-only doctrine over frozen candidates, never invent evidence or findings, and never turn the reviewer into the author, approver, or executor of what it reviews. Monetary values are whole-number cents (BigInt); RUC/company/period scope is mandatory in every check.

Before you dive in, read this guide fully. The repository is in development — today it contains the brand source and this documentation set; the verification tooling is being built under [SDD-090](https://github.com/arkelythex/drenyra-ai/tree/main/openspec/programs/drenyra-dominion/sdds/sdd-090-guardian).

---

## Table of Contents

- [Issue-First Workflow](#issue-first-workflow)
- [Ground Rules](#ground-rules)
- [Development Setup](#development-setup)
- [Testing and Validation](#testing-and-validation)
- [Commit Convention](#commit-convention)
- [Branch Naming](#branch-naming)
- [Pull Request Rules](#pull-request-rules)
- [Code of Conduct](#code-of-conduct)
- [Questions?](#questions)

---

## Issue-First Workflow

**No PR without an issue. No exceptions.**

This project follows a strict issue-first workflow:

1. **Open an issue** describing the problem or change (bug, documentation gap, verification-model change).
2. **Wait for approval** — a maintainer adds the `status:approved` label when the issue is ready to be worked on.
3. **Comment on the issue** to let others know you are working on it.
4. **Open a PR** referencing the approved issue with `Closes #<N>`.

PRs that are not linked to an issue will be rejected by maintainers during review. An issue without `status:approved` is usually still in discussion — implementing before the decision lands means the work gets thrown away.

---

## Ground Rules

These are the non-negotiable rules for every contribution. They are the guardian doctrine.

- **Never the author of what it reviews.** The Guardian Angel is an independent lens; it never produces the work it verifies.
- **Strictly read-only over frozen candidates.** The verification target is frozen before any check; the Guardian Angel never mutates, executes, or persists changes to it.
- **Evidence is cited, never invented.** Every finding must cite the persisted evidence or receipt that proves it.
- **No invented findings.** Findings come from inspecting the frozen target against the applicable frozen contracts — never from narration or plausible-sounding claims.
- **Not part of the approval quorum.** Verdicts are `APPROVED`/`ESCALATED` reports; approval is an explicit human/R2/R3 event in the candidate lifecycle.
- **Frozen contracts as published.** The verification surface is the published `drenyra-ai` contracts — published versions, never private internals. Contract changes belong upstream in `drenyra-ai`.
- **Fiscal conventions.** Money is whole-number cents (BigInt), never floats; RUC/company/period scope is mandatory; no data across RUCs without explicit context.
- **Docs-as-code.** Update docs in the same PR as code. Stale docs are a bug.
- **No AI attribution.** Conventional Commits only; no `Co-Authored-By` or "Generated with" markers.

---

## Development Setup

The repository currently has no build or test toolchain: no package manifest, no CI, no runnable binary. Contributions today are documentation, verification-model design, and brand assets.

- **Clone** the repository and open a branch per [Branch Naming](#branch-naming).
- **Read first** — [Intended Usage](docs/intended-usage.md), the [Architecture](docs/architecture.md), and the [Codebase Guide](docs/CODEBASE-GUIDE.md).
- **Brand work** uses the sibling-checkout layout described in [BRAND.md](assets/branding/BRAND.md): clone `drenyra-ai` next to this repository so `../drenyra-ai/scripts/brand-conformance.mjs` resolves.

When the verification tooling lands under `src/`, this section will grow the real setup and test commands.

---

## Testing and Validation

- **No automated test suite exists yet.** Documentation and model changes are validated by maintainer review against the quality bar and the guardian doctrine.
- **Brand changes** are validated with the `drenyra-ai` brand-conformance checker (palette shape, dual-theme SVG scan, raster coverage ≥ 0.92) as documented in [BRAND.md](assets/branding/BRAND.md). Never commit a brand asset that fails the checker.
- **Markdown** should render cleanly on GitHub; keep tables well-formed and lines reasonably short.

---

## Commit Convention

This project uses [Conventional Commits](https://www.conventionalcommits.org/).

### Format

```text
<type>(<optional-scope>)!: <description>

[optional body]

[optional footer]
```

### Allowed Types

| Type | Purpose |
| --- | --- |
| `feat` | New feature |
| `fix` | Bug fix |
| `docs` | Documentation only |
| `refactor` | Code change (no behavior change) |
| `chore` | Maintenance, dependencies, tooling |
| `style` | Formatting, linting (no logic change) |
| `perf` | Performance improvement |
| `test` | Adding or updating tests |
| `build` | Build system or external deps |
| `ci` | CI configuration |
| `revert` | Reverts a previous commit |

### Examples

```text
docs: bring documentation set to the ecosystem quality bar
docs(architecture): document the blind dual review lifecycle
chore(branding): tighten conformance acceptance threshold
feat(verification): add evidence citation check to findings
```

### Breaking Changes

Add `!` after the type/scope and include a `BREAKING CHANGE:` footer. In this repository a breaking change is almost always a verification-model change — treat it as a major event and document the migration explicitly.

**Never** add `Co-Authored-By`, `Reviewed-by`, or "Generated with" AI markers to commits or PR bodies.

---

## Branch Naming

Branch names **must** match this pattern:

```text
^(feat|fix|chore|docs|style|refactor|perf|test|build|ci|revert)\/[a-z0-9._-]+$
```

**Rules:**

- All lowercase
- Use hyphens, dots, or underscores as separators (no spaces, no uppercase)
- Keep the description short and descriptive

**Examples:** `docs/verification-model`, `docs/readme-quality-bar`, `chore/branding-conformance`

---

## Pull Request Rules

### PR Size Budget

Keep PRs at or below **400 changed lines** (`additions + deletions`). This is a deliberate cognitive-load limit: a PR should be reviewable in roughly **60 minutes**. If your change cannot fit that budget, split it into chained or stacked PRs so each review remains focused.

### Before Opening a PR

- [ ] There is a linked issue (`Closes #<N>`) approved with `status:approved`
- [ ] The PR is at or below 400 changed lines, or it was split into chained PRs
- [ ] Commits follow Conventional Commits format and are organized by deliverable unit
- [ ] Brand assets pass the brand-conformance checker, if branding changed
- [ ] Docs updated in this same PR (docs-as-code) and `CHANGELOG.md` updated
- [ ] The change preserves the guardian invariants: independence, evidence, read-only doctrine
- [ ] Code is self-reviewed
- [ ] I understand and take responsibility for the complete submission, and have disclosed any material AI assistance in the PR

### PR Title

Use the same Conventional Commits format as commit messages:

```text
docs(architecture): document the review lifecycle
docs: rewrite README to the ecosystem quality bar
```

### Linking Your Issue

In the PR body, include one of:

```text
Closes #42
Fixes #42
Resolves #42
```

---

## Code of Conduct

Be respectful. We are building the verification layer of a fiscal system together.

- Critique code, not people
- Be constructive in reviews
- Welcome newcomers

This project follows the [Contributor Covenant](https://www.contributor-covenant.org/). Violations may result in removal from the project.

---

## Questions?

- Open a [discussion](https://github.com/arkelythex/drenyra-ai/discussions) in the ecosystem repository for questions and ideas — not issues.
- See what is planned and what shipped → [CHANGELOG.md](CHANGELOG.md)
- Understand the intended usage and frontier → [Intended Usage](docs/intended-usage.md)
