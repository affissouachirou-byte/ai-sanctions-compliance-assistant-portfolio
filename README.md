# AI Sanctions Compliance Assistant

**A synthetic, human-supervised sanctions investigation and regulatory-research prototype.**

The project explores how screening-alert context, identity evidence, illustrative ownership calculations, dated regulatory sources, AI-assisted research and analyst review can be presented in one traceable investigation workflow.

> **Project status — completed demonstration prototype (25 November 2026).** Not a production screening solution, a validated legal-advice system or a transaction-clearance tool. All scenarios described here are fictional.

## The problem

A name match is not proof of identity. An economic ownership percentage is not automatically a jurisdiction-specific legal ownership/control conclusion. A correctly quoted legal passage does not necessarily support the proposition attributed to it—or establish that it was operative for the case date.

This prototype makes those distinctions visible and preserves unresolved questions for human review.

## What the prototype demonstrates

- **Investigation context:** evidence-linked synthetic alerts, candidates and contradictory or missing identity attributes.
- **Ownership exploration:** dated illustrative equity and voting look-through, with no autonomous legal ownership/control ruling.
- **Regulatory research:** archived/source-versioned OFAC, Swiss SECO and EU evidence, with explicit currency and applicability limitations.
- **AI-assisted drafting:** an optional evidence-grounded research/advisory draft, not a legally authoritative conclusion.
- **Analyst review and reporting:** claim-level review, rationale and audit linkage; unverified legal claims withheld from verified current-law findings.
- **Human decision boundary:** no automated sanctions clearance, transaction release or final legal disposition.

See [architecture and trust boundaries](docs/ARCHITECTURE.md) and [synthetic case studies](docs/CASE_STUDIES.md).

## Demonstration cases

| Synthetic case | What it illustrates | Demonstrated control |
|---|---|---|
| `SYN-ADV-0332-001` | EUR 125,000 payment; 34% illustrative economic interest and 36.5% illustrative voting interest; dated legal evidence | Calculations are not treated as jurisdictional legal determinations; unsupported AI propositions are not promoted to verified findings |
| `SYN-EVAL-ID-001` | CHF 18,400 payment; two name-similar candidates with different date-of-birth evidence states | `CONTRADICTS` and `MISSING` remain distinct; identity remains unresolved |

[Read the case studies](docs/CASE_STUDIES.md) · [View the demonstration outline](docs/DEMO_OUTLINE.md)

## Validation evidence and important limits

**Reported by the project's Codex test run:** 984/984 automated pytest tests passed, with 0 failures, at commit `00dfb9e904ac08b4a07f77ab5b5430a0ecf3e659`. This is a technical regression result, **not** certification of legal accuracy or production readiness. The final documentation package did not independently rerun this suite.

Reconciled regulatory acceptance: **2 PASS, 6 PARTIAL, 1 NOT TESTED** across nine synthetic scenarios. The two passes concern advisory reporting safeguards; jurisdiction-specific legal outcomes remain unverified. Two propositions in an original live AI draft were materially unsupported by the passages cited, and the review/reporting controls kept them out of verified current-law findings.

See [validation and limitations](docs/VALIDATION_AND_LIMITATIONS.md).

## Technical design

**Documented implementation areas:** Python application services, FastAPI-based analyst-facing interface, pytest-based automated testing, structured JSON case/evidence contracts, evidence provenance and audit-linked claim review. Optional LLM-assisted drafting is restricted by review safeguards.

This public repository intentionally contains **documentation only**. Representative executable modules and tests should be added **only after** extraction from the verified development commit and a dedicated code, dependency, licensing and credential review. The original repository has not been copied here.

## Engineering decisions

The project uses a frozen baseline and traceable remediation commits. A missing-fixture packaging issue was resolved without changing application logic. A reporting correction ensured a reviewer's `SUPPORTED` label cannot, by itself, create a verified current-law finding in the historical research workflow.

[Read the engineering decisions](docs/ENGINEERING_DECISIONS.md).

## Boundaries

- No live bank/customer data in the published examples.
- No claim that the tool determines OFAC, EU or Swiss legal ownership/control status.
- No claim that current regulatory provisions, designations or jurisdictional applicability are verified in these case dossiers.
- No measured savings, production screening recall, risk-model calibration or autonomous disposition claims.
- Source/reuse rights for any future code, vendor materials or regulatory corpora must be reviewed before publication.

**Reference:** technical closeout commit `00dfb9e904ac08b4a07f77ab5b5430a0ecf3e659` (private development repository; no public source link asserted).

**Publication status:** public portfolio documentation. Executable code has not yet been security-reviewed or published.
