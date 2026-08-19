# Intended Usage — Drenyra Guardian Angel

> [!IMPORTANT]
> **The frontier:** the Guardian Angel verifies fiscal work — it never produces it. It is the ecosystem's independent, adversarial, continuous review lens, and it is never part of the approval quorum.

## Definition

**Drenyra Guardian Angel is the independent verification layer of the Drenyra ecosystem: it reviews frozen accounting candidates and receipts against the published `drenyra-ai` contracts, seeking refutation rather than confirmation.**

It is the fiscal-domain counterpart of `gentleman-guardian-angel` — same posture (independent reviewer, never the author), stricter controls (fiscal risk is not a merge conflict). Its verification model has three pillars:

- **Refutation** — the reviewer looks for what breaks the candidate, not for what supports it. Candidate-caused severe findings block; pre-existing/base findings become follow-ups.
- **Blind dual review** — two independent judges inspect the identical frozen target with identical criteria, each returning one neutral findings result. Agreement is corroboration; contradiction escalates to a human decision.
- **Evidence checks** — every finding must cite the persisted evidence or receipt that proves it. A finding without evidence is not a finding; transcripts and narration prove nothing.

## The verification frontier

The Guardian Angel occupies the verification position that Judgment Day holds in software engineering — **equivalent discipline, stricter controls**. Judgment Day turns ordinary review into explicit blind dual review with a bounded two-round rule; the Guardian Angel applies the same discipline to accounting and fiscal candidates, where the stakes are not a merge conflict but a filing.

The institution is the same across the ecosystem: **the AI proposes, the system validates, the professional decides, the evidence remains.** The Guardian Angel is the "validates" step made adversarial and independent — a separate lens that never wrote what it reads.

## What the Guardian Angel is NOT

| Not this | Because |
| --- | --- |
| The author of what it reviews | It verifies candidates and receipts produced by the ecosystem; it never produces them |
| An approver | Approval is an explicit human/R2/R3 event in the candidate lifecycle; a verification verdict grants no authority |
| Part of the approval quorum | It reports `APPROVED`/`ESCALATED` verdicts but is never consulted as a decision-maker in the approval flow |
| An executor | Strictly read-only over frozen candidates; it never mutates, executes, or persists changes |
| A legal or tax advisor | It verifies evidence and contract conformance; it does not give legal or tax advice, and its verdicts do not replace professional judgment |
| The fiscal authority | The human accountant is the final authority; the Guardian Angel is a verification input to that authority |
| A source of truth | The accounting database is transactional truth; receipts and the ledger are execution proof; verification is an independent check over them |

## The responsibility split

| Component | Role |
| --- | --- |
| **Drenyra AI** | Verifiable core — frozen contracts, candidates, receipts, gates, ledger (Alpha v0.5.0) |
| **Drenyra Guardian Angel** | Independent, adversarial, continuous verification over the frozen contracts (this repo) |
| **Drenyra Engram** | Institutional memory — informs, never authorizes |
| **Drenyra Skills** | Versioned accounting, tax, and operational knowledge (PE jurisdiction) |
| **Drenyra Pi** | Pi-native harness (consumes, pinned) |
| **Drenyra Command Center** | Web application for professionals (consumes) |
| **Human accountant** | Final authority — decides, approves, and owns the fiscal outcome |

## The target experience

A professional accountant works in the Command Center. Behind the scenes, every material candidate is verified by an independent adversarial lens: two blind judges, refutation, evidence checks, a bounded correction budget, and a clear verdict. The professional never operates the verification machinery — they receive the verdict, the evidence, and the decision rights, and they remain the final authority.

> "The system that did the work is not the system that checked the work."

## Frontier rules

1. **Never the author.** The Guardian Angel verifies; it never produces what it verifies.
2. **Strictly read-only.** The verification target is frozen before any check; nothing is mutated, executed, or persisted by the reviewer.
3. **Refutation, not confirmation.** Severe candidate-caused findings block; pre-existing/base findings become follow-ups.
4. **Evidence is cited.** Every finding cites persisted evidence or a receipt. Findings without evidence do not exist.
5. **Blind dual review.** Two independent judges, identical target and criteria, one neutral result each; agreement corroborates, contradiction escalates.
6. **Bounded correction.** At most two scoped fix/re-judgment rounds; round-two survivors escalate.
7. **Never approval.** Verdicts report; approval is a separate, explicit human event.
8. **Fiscal discipline.** Money is whole-number cents (BigInt); RUC/company/period scope is mandatory; contracts are consumed as published, never from private internals.

## Quick path

1. Read the [Architecture](architecture.md) — ecosystem position, invariants, and the review lifecycle.
2. Read the [Codebase Guide](CODEBASE-GUIDE.md) — where things live and what must never change.
3. Read the frozen contracts this repository consumes: [drenyra-ai Contracts](https://github.com/arkelythex/drenyra-ai/tree/main/contracts).

## Next steps

- The verification model and review lifecycle → [Architecture](architecture.md)
- The repository map and invariants → [Codebase Guide](CODEBASE-GUIDE.md)
- What has changed → [CHANGELOG.md](../CHANGELOG.md)
- The project overview → [README.md](../README.md)
