# Engineering decisions demonstrated by the project

## 1. Keep the original feature-freeze baseline intact

The scope was frozen at Analyst Workspace B2. Subsequent changes were treated as narrowly scoped remediations with separate commit identities. This prevents retrospective rewriting of the tested baseline.

## 2. Reproducible tests need versioned inputs

An initial clean checkout missed six static synthetic JSON fixtures, causing test failures and misleading HTTP responses in downstream lifecycle scenarios. A separate remediation commit added verified fixtures, a synthetic-provenance note and a SHA-256 manifest. The full suite then passed in a fresh checkout without manual fixture injection.

## 3. Auditability does not imply legal accuracy

Citation/reference validation and reviewer journals were necessary but insufficient. Two original AI propositions were unsupported by the cited legal paragraphs. The project retains these failure cases as evidence of a limitation, rather than representing them as verified legal findings.

## 4. Keep reviewer assessments distinct from current law

The reviewed-report projection was corrected so a `SUPPORTED` claim-review label does not automatically populate verified current-law findings for the historical-evidence workflow. Review decisions and rationales remain auditable; current-law and case-applicability flags remain unverified.

## 5. Prefer explicit abstention to unjustified legal determination

The prototype preserves uncertainty for missing or contradictory identity evidence, illustrative ownership computations and unresolved jurisdictional applicability. Human investigation, rather than autonomous release or block decisions, remains the outcome.

## What this shows—and what it does not

These decisions demonstrate traceability, test discipline and bounded AI-assistance design. They do not establish production operations, accurate current-law analysis or independent regulatory acceptance.
