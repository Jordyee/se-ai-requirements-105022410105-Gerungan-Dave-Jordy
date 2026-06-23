# 07 Validation: Reviewed Baseline

## Review Status

| Field | Value |
|---|---|
| Raw source | `outputs/raw/07-validation.md` |
| Reviewed by | Gerungan Dave Jordy |
| Review date | 23 June 2026 |
| Review outcome | Accepted with simplification and grouped findings |
| Important boundary | This validates the reviewed requirements baseline at its current detail level. It does not approve new requirements, policies, measurable NFR targets, final traceability, or final diagrams. |

This reviewed version keeps the raw validation conclusions but reduces table size. The main validation result is that the baseline is internally traceable and consistent, but many product details remain partial or not testable yet.

## 1. Inputs and Evidence Sources

| Source | Use in this reviewed output |
|---|---|
| `outputs/raw/07-validation.md` | First AI validation output reviewed for this stage. |
| `outputs/reviewed/03-requirements.md` | Authoritative reviewed requirements and deferred topics. |
| `outputs/reviewed/04-user-stories.md` | Reviewed story traceability and readiness. |
| `outputs/reviewed/05-prioritization.md` | Reviewed MoSCoW, value, and readiness risk. |
| `outputs/reviewed/06-use-case.md` | Reviewed high-level use-case view. |
| `evaluation/ai-output-review.md` | Review record and correction rationale. |

## 2. Review Revisions from Raw Output

| Raw output issue or improvement area | Reviewed revision |
|---|---|
| Raw validation matrix listed one row for almost every item. | Grouped similar findings while preserving important `FR-*`, `US-*`, `NFR-*`, and `DR-*` references. |
| Raw output repeated the same "needs approval" decision across many rows. | Consolidated unresolved decisions into grouped readiness risks. |
| Raw output was accurate but longer than needed for the reviewed baseline. | Kept the validation result and shortened wording. |

No unsupported policy decision was found in the raw output. No open question is answered in this reviewed version.

## 3. Reviewed Validation Summary

| Area | Reviewed items | Result | Finding |
|---|---|---|---|
| Traceability from requirements to stories | `FR-01` to `FR-11`; `US-01` to `US-11` | Pass | Every reviewed product user story maps to an existing reviewed functional requirement. |
| Traceability from stories to use cases | `US-01` to `US-11`; `UC-01` to `UC-11` | Pass | Reviewed use cases are high-level views derived from reviewed stories and requirements. |
| Priority-risk alignment | Skill 04 priorities; `FR-*`; `NFR-*`; `CON-SPEC-*` | Pass | Must/Should labels do not hide readiness risk; partial items remain marked risky or incomplete. |
| Deferred topics | `DR-01` to `DR-18` | Pass | Deferred topics are kept as blockers or decision areas, not approved requirements. |
| Assignment and deadline capabilities | `FR-01` to `FR-03`; `US-01` to `US-03`; `UC-01` to `UC-03` | Partial | Valid at high level, but assignment fields, deadline interpretation, and late-submission rules remain open. |
| Submission and monitoring capabilities | `FR-04`; `FR-05`; `US-04`; `US-05`; `UC-04`; `UC-05` | Partial / risk | Core capabilities are supported, but submission policy, file policy, receipt proof, status values, and update rules remain unresolved. |
| Grading and feedback capabilities | `FR-06`; `FR-07`; `US-06`; `US-07`; `UC-06`; `UC-07` | Partial | Grading and feedback are in scope, but publication, correction, visibility, and history rules remain open. |
| Administration capabilities | `FR-08` to `FR-10`; `US-08` to `US-10`; `UC-08` to `UC-10` | Partial / risk | User, course, and configuration management are valid at high level, but authentication, role assignment, governance, integration, and managed-data detail remain open. |
| Reporting | `FR-11`; `US-11`; `UC-11` | Partial / risk | Reporting is case-supported only at a high level; report detail and access rights remain undefined. |
| NFR candidates | `NFR-01` to `NFR-05` | Not testable yet | Quality areas are confirmed, but measurable usability, security, performance, reliability, backup, recovery, capacity, and data-integrity targets are not approved. |
| Artefact constraints | `CON-SPEC-01` to `CON-SPEC-04` | Pass / risk | Evidence separation and traceability constraints are followed; technology independence remains assumption-labelled through `ASM-08`. |

## 4. Open Validation Risks

| Risk group | Related IDs | Current handling |
|---|---|---|
| Detailed product behavior | `DR-01` to `DR-11` | Keep partial; do not create detailed validation criteria yet. |
| Security, role, audit, and retention policy | `DR-12`; `DR-13`; `DR-15`; `OQ-08`; `OQ-10`; `ASM-03`; `ASM-06` | Keep risk-labelled until approved policy exists. |
| Measurable NFR validation | `NFR-01` to `NFR-05`; `DR-16`; `OQ-09`; `ASM-02` | Mark not testable yet. |
| Integration and administrative data boundary | `DR-17`; `DR-18`; `OQ-11`; `ASM-08` | Keep open; do not choose standalone or integration behavior. |

## 5. Student Decisions Needed

Before validation can become more testable, the student must decide whether to approve evidence for:

1. assignment fields, deadline rules, late submission, resubmission, file policy, receipt evidence, and status values;
2. grade and feedback publication, correction, visibility, and history;
3. reporting contents and access rights;
4. authentication, role assignment, audit, retention, configuration governance, integration, and managed data;
5. measurable NFR targets.

## 6. Quality Checks

| Check | Result |
|---|---|
| Raw Skill 05 validation output was preserved separately. | Passed |
| Reviewed validation uses only reviewed Skill 03, Skill 04, and reviewed use-case items. | Passed |
| No new requirement ID is created. | Passed |
| Open questions and deferred topics remain unresolved. | Passed |
| Partial and assumption-labelled items keep their risk visible. | Passed |
| NFR candidates without measurable targets are not marked fully testable. | Passed |
| No final traceability matrix or final diagram is produced. | Passed |
