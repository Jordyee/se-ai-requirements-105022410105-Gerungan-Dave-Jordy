# 08 Change Request: Reviewed Baseline

## Review Status

| Field | Value |
|---|---|
| Raw source | `outputs/raw/08-change-request.md` |
| Reviewed by | Gerungan Dave Jordy |
| Review date | 23 June 2026 |
| Review outcome | Accepted with consolidation into fewer decision groups |
| Important boundary | These are proposed change requests only. They do not approve baseline changes, new requirements, policies, measurable NFR targets, final traceability, or final diagrams. |

This reviewed version consolidates the raw change requests so the comparison is clearer: raw output listed detailed candidates, while reviewed output groups them into decision areas for later student action.

## 1. Inputs and Evidence Sources

| Source | Use in this reviewed output |
|---|---|
| `outputs/raw/08-change-request.md` | First AI change request output reviewed for this stage. |
| `outputs/reviewed/03-requirements.md` | Baseline requirements, NFR candidates, deferred topics, and assumptions affected by changes. |
| `outputs/reviewed/04-user-stories.md` | Baseline user stories affected by changes. |
| `outputs/reviewed/05-prioritization.md` | Priority and readiness risk affected by changes. |
| `outputs/reviewed/07-validation.md` | Reviewed validation findings that motivate change requests. |

## 2. Review Revisions from Raw Output

| Raw output issue or improvement area | Reviewed revision |
|---|---|
| Raw output listed ten change request candidates, several of which overlap. | Consolidated them into six broader decision groups. |
| Raw output repeated "needs approval or stakeholder evidence" in every row. | Kept a shared approval rule and shorter evidence-status wording. |
| Raw output was accurate but heavy for a reviewed baseline. | Kept only the decision-ready impact summary. |

No change request is approved in this reviewed output.

## 3. Reviewed Change Request Candidates

| Change request | Decision area | Baseline affected | Evidence status | Impact if approved | Current status |
|---|---|---|---|---|---|
| `CR-01` | Assignment and deadline detail: mandatory fields, validation rules, timezone, cutoff, deadline-change, and late-submission behavior. | `FR-01` to `FR-03`; `US-01` to `US-03`; `UC-01` to `UC-03`; `DR-01` to `DR-03`; `OQ-01`; `OQ-02`; `OQ-12`; `ASM-05` | Needs student approval or stakeholder evidence. | Would make assignment creation, assignment viewing, and deadline validation more specific. | Proposed / Needs approval |
| `CR-02` | Submission and monitoring detail: resubmission, file limits, upload failure handling, receipt proof, status values, and update rules. | `FR-04`; `FR-05`; `US-04`; `US-05`; `UC-04`; `UC-05`; `DR-03` to `DR-08`; `OQ-02`; `OQ-03`; `OQ-04`; `OQ-DRAFT-01`; `OQ-DRAFT-03` | Needs student approval or stakeholder evidence. | Would reduce high risk around core student submission and monitoring workflows. | Proposed / Needs approval |
| `CR-03` | Grade and feedback policy: publication, correction, visibility, and history. | `FR-06`; `FR-07`; `US-06`; `US-07`; `UC-06`; `UC-07`; `DR-10`; `OQ-06`; `ASM-06` | Needs student approval or stakeholder evidence. | Would make grading and feedback use cases more testable. | Proposed / Needs approval |
| `CR-04` | Administration and security policy: authentication, role assignment, audit, retention, configuration governance, and managed data. | `FR-08` to `FR-10`; `NFR-02`; `NFR-05`; `US-08` to `US-10`; `UC-08` to `UC-10`; `DR-12` to `DR-15`; `DR-18`; `OQ-08`; `OQ-10`; `OQ-DRAFT-02`; `ASM-03`; `ASM-06` | Needs student approval or stakeholder evidence. | Would reduce security, accountability, and administration ambiguity. | Proposed / Needs approval |
| `CR-05` | Reporting and notification scope: report detail, report access rights, notification events, and notification channels. | `FR-11`; `US-11`; `UC-11`; `DR-09`; `DR-11`; `OQ-05`; `OQ-07`; `ASM-01`; `ASM-06` | Needs student approval or stakeholder evidence. | Would decide whether reporting remains high-level and whether notifications enter scope. | Proposed / Needs approval |
| `CR-06` | Measurable NFR and integration boundary: usability, security, performance, reliability, backup, recovery, capacity, data integrity targets, and standalone/integration decision. | `NFR-01` to `NFR-05`; `FR-09`; `FR-10`; `DR-16`; `DR-17`; `OQ-09`; `OQ-11`; `ASM-02`; `ASM-08` | Needs student approval or stakeholder evidence. | Would allow later NFR validation and architecture boundary decisions to become testable. | Proposed / Needs approval |

## 4. Approval Rule

| Rule | Reviewed decision |
|---|---|
| Change request approval | None of the `CR-*` items is approved by this reviewed output. |
| Evidence requirement | Each candidate requires real stakeholder evidence, approved simulation, or explicit student decision before it can change the reviewed baseline. |
| Baseline update path | Approved changes must update the relevant reviewed requirements, stories, priorities, validation, and later traceability artefacts. |
| Rejected or deferred changes | If the student rejects or defers a candidate, it should remain outside the approved requirements baseline. |

## 5. Suggested Review Priority

| Priority | Change request | Reason |
|---|---|---|
| 1 | `CR-02` Submission and monitoring detail | Affects high-value Must capabilities with high readiness risk. |
| 2 | `CR-03` Grade and feedback policy | Affects core lecturer assessment workflows. |
| 3 | `CR-04` Administration and security policy | Affects access control, accountability, and data integrity. |
| 4 | `CR-06` Measurable NFR and integration boundary | Needed before quality validation can become testable. |
| 5 | `CR-01` Assignment and deadline detail | Important for clearer assignment workflows. |
| 6 | `CR-05` Reporting and notification scope | Reporting is partial and notifications remain unapproved. |

## 6. Quality Checks

| Check | Result |
|---|---|
| Raw Skill 05 change request output was preserved separately. | Passed |
| Reviewed change requests are based on reviewed validation findings and reviewed baselines. | Passed |
| No change request is treated as approved. | Passed |
| No new requirement ID is created. | Passed |
| Open questions and deferred topics remain unresolved. | Passed |
| No policy was invented for late submission, resubmission, file limits, grade publication, notifications, authentication, reporting detail, retention, integrations, or measurable NFR targets. | Passed |
