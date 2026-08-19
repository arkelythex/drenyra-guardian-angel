# AI-Assisted Contribution Policy

AI-assisted contributions are permitted. The human contributor must understand, review, validate, and take full responsibility for everything they submit — especially when it touches the verification model or the frozen contracts this repository consumes.

> [!IMPORTANT]
> **Verification integrity is a product safety requirement.** This repository is the ecosystem's independent adversarial lens. A contribution that weakens independence, invents evidence or findings, or breaks the read-only doctrine over frozen candidates is a product defect regardless of who or what authored it. The contributor owns the submission; AI assistance does not transfer that ownership.

## Human Responsibility

The human contributor remains fully responsible for:

- The security, correctness, and ongoing maintenance of the complete submission.
- Reviewing and validating every change, claim, and test result.
- Ensuring appropriate licensing and confidence in the provenance of submitted material.
- Explaining and defending the design, implementation, and tradeoffs during review.
- Verifying that the guardian invariants hold: the reviewer is never the author, evidence is cited and never invented, findings are never fabricated, and the frozen contracts are consumed as published.

AI assistance does not transfer authorship, accountability, or legal responsibility away from the contributor.

## Disclosure

Disclose material AI assistance used to produce or substantively review any part of a contribution, including:

- Code, tests, or documentation.
- Designs, prompts, skills, schemas, or workflows.
- Substantive review, investigation, or analysis.

For material assistance, the pull request declaration must state:

1. The tool or model, if known.
2. The material scope of the assistance.
3. The verification the contributor performed.

Raw prompts and private conversation logs are not required by default.

Trivial formatting, spelling corrections, minor autocomplete, search or navigation, and trivial, non-substantive mechanical transformations do not require disclosure.

## Review and Attribution

Maintainers may request an explanation, prompt summary, provenance information, supporting evidence, or additional tests. They may reject work that the contributor cannot explain, verify, or defend.

AI tools must not receive human attribution, including `Co-Authored-By`, `Reviewed-by`, `Tested-by`, `Signed-off-by`, approval, or equivalent credit. An optional `Assisted-by` trailer may be accepted, but the pull request declaration is sufficient.

## Advisory Review and Verification

Assistance used to produce a contribution is distinct from adversarial verification of that contribution. Although materially substantive AI-assisted advisory review remains subject to the disclosure rules above, it remains distinct from contribution authorship. Automated review does not replace human authorship, provenance, consent, testing, or legal responsibility — and a verification verdict never replaces the human accountant as the final authority.

## Submission Quality

Review is based on observable submission quality, not on whether text or code appears to be AI-generated. Before proposing a fix, contributors should identify the underlying cause and the responsible invariant, then explain and defend why the change is proportionate. Prefer the smallest change that restores that invariant without adding duplicate authority, unnecessary abstractions, or unrelated complexity. This does not require broad or architectural work when a focused fix is sufficient.

Unacceptable behavior includes:

- Submitting output that the contributor has not reviewed.
- Making claims that cannot be verified or reporting results that did not occur.
- Inventing APIs, paths, behavior, evidence, findings, or test results.
- Masking a symptom, shifting the failure elsewhere, or leaving the responsible invariant broken.
- Weakening independence — for example, making the reviewer co-author, approver, or executor of what it verifies.
- Citing evidence that does not exist or relying on transcripts and narration instead of persisted evidence.
- Adding duplicate authority, unnecessary abstractions, or unrelated complexity that creates likely regressions.
- Including broad or unrelated changes outside the approved scope.
- Touching the frozen contract surface without going through the upstream `drenyra-ai` regime.
- Copying output without confidence in its provenance or license compatibility.
- Being unable to explain the change, its design, or its consequences.
- Delegating the work of understanding, validating, or repairing the submission back to maintainers.

## Enforcement

For now, maintainers enforce this policy through reviewer judgment and documented review decisions only. The project does not use automated AI detection or an automated disclosure gate.
