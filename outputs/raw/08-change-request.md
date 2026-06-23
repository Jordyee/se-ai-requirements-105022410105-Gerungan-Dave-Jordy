# Skill 05 Raw Output: Change Requests

## 1. Review Status and Boundary

| Field | Value |
|---|---|
| Output type | First AI raw output for Skill 05 change requests |
| Created for review by | Gerungan Dave Jordy |
| Creation date | 23 June 2026 |
| Baseline used | Reviewed Skill 01 through Skill 04 outputs and raw Skill 05 validation findings |
| Boundary | This document records proposed change request candidates and impact analysis only. It does not approve baseline changes, new requirements, policies, measurable NFR targets, final traceability, or final diagrams. |

Each change request below is a candidate created from validation gaps. Approval requires student decision and, where needed, updated evidence through elicitation/specification review before any reviewed baseline changes.

## 2. Inputs and Evidence Sources

| Source | Use in this output |
|---|---|
| `outputs/reviewed/01-inception.md` | Reviewed objectives, stakeholders, assumptions, risks, and open questions. |
| `outputs/reviewed/02-elicitation.md` | Reviewed decision log, answer classification, and elicitation risks. |
| `outputs/reviewed/03-requirements.md` | Baseline requirements, NFR candidates, deferred topics, and assumptions affected by changes. |
| `outputs/reviewed/04-user-stories.md` | Baseline user stories affected by changes. |
| `outputs/reviewed/05-prioritization.md` | Baseline priority and readiness risk affected by changes. |
| `outputs/raw/07-validation.md` | Raw validation findings that identify change candidates. |

## 3. Change Request Rules

| Rule | Application |
|---|---|
| A change request is not approval. | Every `CR-*` remains proposed, deferred, or needs approval unless the reviewed baseline is updated later. |
| Open questions stay open. | `OQ-*` and `OQ-DRAFT-*` references identify evidence gaps, not answers. |
| Deferred topics are not requirements. | `DR-*` items are impact areas until approved evidence supports a baseline change. |
| Partial requirements keep risk visible. | Change requests may reduce risk later but do not currently make partial items fully testable. |
| No silent policy choice. | Late submission, resubmission, file limits, grade publication, notifications, authentication, reporting, retention, integrations, and NFR targets require explicit approval. |

## 4. Change Request Candidates

| Change request ID | Request summary | Source of request | Current baseline affected | Proposed change type | Evidence status | Recommendation | Approval status |
|---|---|---|---|---|---|---|---|
| `CR-01` | Clarify mandatory assignment fields and assignment validation rules. | Validation findings `VAL-01`, `VAL-03` | `FR-01`; `FR-03`; `US-01`; `US-03`; `DR-01`; `OQ-01` | Clarification | Needs student approval or stakeholder evidence | Ask lecturer or approve simulated answer before updating requirements. | Proposed / Needs approval |
| `CR-02` | Clarify deadline timezone, cutoff, deadline-change, and late-submission behavior. | Validation finding `VAL-02` | `FR-02`; `US-02`; `DR-02`; `DR-03`; `OQ-02`; `OQ-12`; `ASM-05` | Policy decision | Needs student approval or stakeholder evidence | Defer unless lecturer or academic policy evidence is approved. | Proposed / Needs approval |
| `CR-03` | Clarify submission policy, including resubmission, file limits, upload failure handling, and receipt proof. | Validation finding `VAL-04` | `FR-04`; `US-04`; `DR-03` to `DR-07`; `OQ-02`; `OQ-03`; `OQ-04`; `OQ-DRAFT-03` | Policy decision / clarification | Needs student approval or stakeholder evidence | Gather lecturer, student, and IT support evidence before updating `FR-04` detail. | Proposed / Needs approval |
| `CR-04` | Clarify student-facing status values and update rules. | Validation finding `VAL-05` | `FR-05`; `US-05`; `DR-08`; `OQ-DRAFT-01`; `OQ-DRAFT-03`; `OQ-12` | Clarification | Needs student approval or stakeholder evidence | Ask lecturer and student stakeholders before specifying status model. | Proposed / Needs approval |
| `CR-05` | Clarify grade and feedback publication, correction, visibility, and history rules. | Validation findings `VAL-06`, `VAL-07` | `FR-06`; `FR-07`; `US-06`; `US-07`; `DR-10`; `OQ-06`; `ASM-06` | Policy decision | Needs student approval or stakeholder evidence | Ask lecturer and academic management before updating grading and feedback detail. | Proposed / Needs approval |
| `CR-06` | Clarify reporting types, contents, filters, recipients, and access rights. | Validation finding `VAL-11` | `FR-11`; `US-11`; `DR-11`; `OQ-07`; `ASM-01`; `ASM-06` | Clarification / addition | Needs student approval or stakeholder evidence | Keep high-level reporting until report detail is approved. | Proposed / Needs approval |
| `CR-07` | Clarify authentication, role assignment, audit, and retention policies. | Validation findings `VAL-08`, `VAL-13`, `VAL-16` | `FR-08`; `NFR-02`; `NFR-05`; `US-08`; `DR-12`; `DR-13`; `DR-15`; `OQ-08`; `OQ-10`; `ASM-03`; `ASM-06` | Policy decision | Needs student approval or stakeholder evidence | Ask administrator, IT support, or academic management before changing baseline. | Proposed / Needs approval |
| `CR-08` | Define measurable usability, security, performance, reliability, backup, recovery, capacity, and data-integrity targets. | Validation findings `VAL-12` to `VAL-16` | `NFR-01` to `NFR-05`; `DR-16`; `OQ-09`; `ASM-02` | Addition / policy decision | Needs student approval or stakeholder evidence | Defer fully testable NFR validation until measurable targets are approved. | Proposed / Needs approval |
| `CR-09` | Clarify course data, enrolment rules, administrator-managed data, and integration boundary. | Validation findings `VAL-09`, `VAL-18` | `FR-09`; `FR-10`; `US-09`; `US-10`; `DR-17`; `DR-18`; `OQ-11`; `OQ-DRAFT-02`; `ASM-08` | Clarification / policy decision | Needs student approval or stakeholder evidence | Keep technology and integration boundary open until administrator or IT evidence is approved. | Proposed / Needs approval |
| `CR-10` | Decide whether notification events and channels should enter scope. | Reviewed deferred topic from Skill 03 and Skill 04 | `DR-09`; `OQ-05`; possibly `FR-05`; `US-05`; `NFR-01` | Addition | Needs student approval or stakeholder evidence | Keep notifications deferred unless the student approves evidence for events and channels. | Proposed / Needs approval |

## 5. Impact Analysis

| Change request | Stakeholders affected | Requirement/story impact | Priority/validation impact | Risk if not resolved |
|---|---|---|---|---|
| `CR-01` | Lecturer; student | Could add detail to `FR-01`, `FR-03`, `US-01`, and `US-03`. | Would reduce ambiguity for assignment creation/viewing validation. | Assignment workflows remain high-level and cannot validate field completeness. |
| `CR-02` | Lecturer; student; academic management | Could add detail to `FR-02`, `US-02`, and submission-related boundaries. | Would reduce high readiness risk for deadline definition. | Deadline and late-submission behavior remains ambiguous. |
| `CR-03` | Student; lecturer; IT support | Could add detail to `FR-04`, `US-04`, and reliability/data-integrity concerns. | Would make submission validation more testable. | Core submission workflow remains high-risk despite Must priority. |
| `CR-04` | Student; lecturer | Could add detail to `FR-05` and `US-05`. | Would reduce monitoring ambiguity. | Users may not have a validated shared status model. |
| `CR-05` | Lecturer; student; academic management | Could add detail to `FR-06`, `FR-07`, `US-06`, and `US-07`. | Would make grading and feedback validation more complete. | Grade/feedback workflows remain policy-incomplete. |
| `CR-06` | Lecturer; administrator; assumed academic management | Could add detail to `FR-11` and `US-11`. | Would allow reporting to move beyond high-level partial validation. | Reporting expectations remain undefined. |
| `CR-07` | Administrator; lecturer; student; assumed IT support | Could add detail to `FR-08`, `NFR-02`, `NFR-05`, and `US-08`. | Would reduce security and data-integrity uncertainty. | Access control, accountability, and retention remain untestable. |
| `CR-08` | All stakeholders; assumed IT support | Could make `NFR-01` to `NFR-05` measurable. | Would allow NFRs to become testable instead of not testable yet. | Quality concerns remain non-measurable and weak for acceptance. |
| `CR-09` | Administrator; lecturer; student; assumed IT support | Could add detail to `FR-09`, `FR-10`, `US-09`, and `US-10`. | Would clarify system boundary and administrative data scope. | Course/admin workflows remain high-level; integration risk remains open. |
| `CR-10` | Student; lecturer | Could add notification scope if approved. | Would affect `FR-05`/`US-05` monitoring and usability validation. | Notification expectations remain outside approved requirements. |

## 6. Approval and Evidence Status

| Status | Change requests | Meaning |
|---|---|---|
| Proposed / needs approval | `CR-01` through `CR-10` | These are candidates for future baseline changes. None is approved by this raw output. |
| Approved | None | No reviewed baseline currently approves the proposed changes. |
| Rejected | None | No proposed change has been rejected in this raw output. |
| Deferred | None yet | The student may defer any candidate after review. |

No change request may update the reviewed requirements, user stories, prioritisation, use cases, validation, traceability, or diagram until the student approves the evidence path and reviewed baseline update.

## 7. Student Decisions Needed

The student should review each `CR-*` candidate and choose one of these actions:

1. `Approve evidence gathering`: collect or approve stakeholder evidence, then update earlier reviewed baselines before detailed validation.
2. `Defer`: keep the item as an open issue for later work.
3. `Reject`: decide the change should not enter scope.
4. `Clarify request`: rewrite the change request before evidence is gathered.

Decision priority for the next review should start with `CR-03`, `CR-05`, `CR-07`, and `CR-08` because they affect high-risk Must capabilities or NFR testability.

## 8. Quality Checks

| Check | Result |
|---|---|
| Change requests are based on reviewed Skill 01 through Skill 04 and raw Skill 05 validation findings. | Passed |
| No change request is treated as approved. | Passed |
| No new requirement ID is created. | Passed |
| Deferred `DR-*` topics remain decision areas, not requirements. | Passed |
| Open `OQ-*` and `OQ-DRAFT-*` items are not answered. | Passed |
| Partial and assumption-labelled items keep their status and risk visible. | Passed |
| No policy was invented for late submission, resubmission, file limits, grade publication, notifications, authentication, reporting detail, retention, integrations, or measurable NFR targets. | Passed |
| No final traceability matrix, final diagram, implementation task, or code design is produced. | Passed |
