# Skill 04 Raw Output: User Stories

## 1. Review Status and Boundary

| Field | Value |
|---|---|
| Raw output | `outputs/raw/04-user-stories.md` |
| Skill | Skill 04: User Story Derivation and Prioritisation |
| Generated date | 23 June 2026 |
| Review status | Raw AI output; not yet student-reviewed |
| Boundary | This file derives user-story candidates only from reviewed Skill 03 requirements. It is not a reviewed baseline, use case document, validation result, implementation plan, or change request. |

This raw output does not create new requirements. It converts reviewed Skill 03 `FR-*`, `NFR-*`, and `CON-SPEC-*` items into traceable story candidates where useful. Deferred `DR-*` topics remain blocked or decision-needed items.

## 2. Inputs and Evidence Sources

| Source | Role in this raw output |
|---|---|
| `README.md` | Assignment workflow, evidence policy, and raw/reviewed output separation. |
| `CASE.md` / `SRC-01` | Case-confirmed project facts and initial scope. |
| `outputs/reviewed/01-inception.md` | Reviewed stakeholders, objectives, risks, open questions, and constraints. |
| `outputs/reviewed/02-elicitation.md` | Reviewed elicitation classifications, open questions, and readiness risks. |
| `outputs/reviewed/03-requirements.md` | Authoritative requirements baseline for `FR-*`, `NFR-*`, `DR-*`, and `CON-SPEC-*` items. |
| `evaluation/ai-output-review.md` | Review corrections requiring evidence separation and visible partial status. |

Source labels are preserved from the reviewed baselines: `SRC-*`, `INT-*`, `ASM-*`, `OQ-*`, `OQ-DRAFT-*`, `FR-*`, `NFR-*`, `DR-*`, and `CON-SPEC-*`.

## 3. Story Derivation Rules

| Rule | Application in this raw output |
|---|---|
| Use reviewed Skill 03 as authority. | Story candidates map only to reviewed `FR-*`, `NFR-*`, or `CON-SPEC-*` items. |
| Do not create new requirements. | Story wording is narrower than or equal to its source requirement. |
| Preserve partial status. | Story candidates based on partial requirements keep open issues and risk notes visible. |
| Preserve assumption labels. | Stories linked to `ASM-*` evidence remain assumption-labelled where applicable. |
| Keep deferred topics deferred. | `DR-*` items are listed as blocked or decision-needed, not accepted story candidates. |
| Avoid acceptance criteria. | Acceptance criteria are not written because several policies and measurable targets remain open. |

## 4. User Story Candidates

| Story ID | User story | Source requirement | Evidence | Readiness | Boundary |
|---|---|---|---|---|---|
| US-01 | As a lecturer, I want to create assignments, so that coursework tasks can be defined for students. | `FR-01` | `SRC-01`; `INT-L-01` | Ready at high level | Mandatory fields, validation rules, templates, attachments, and publishing workflow remain open under `OQ-01` and `DR-01`. |
| US-02 | As a lecturer, I want to define assignment deadlines, so that students know when coursework submissions are due. | `FR-02` | `SRC-01`; `INT-L-01` | Ready at high level | Timezone, cutoff behavior, deadline changes, and late-submission handling remain open under `OQ-02`, `OQ-12`, `DR-02`, and `DR-03`. |
| US-03 | As a student, I want to view assignment information, so that I can understand coursework tasks before submitting work. | `FR-03` | `SRC-01`; `INT-S-01` | Ready at high level | Exact assignment fields and display expectations remain open under `OQ-01` and `DR-01`. |
| US-04 | As a student, I want to submit files for assignments, so that I can provide coursework work through the system. | `FR-04` | `SRC-01`; `INT-S-01` | Ready at high level with high unresolved-detail risk | File types, file size, upload failure handling, late submission, resubmission, and receipt evidence remain open under `OQ-02`, `OQ-03`, `OQ-04`, `OQ-DRAFT-03`, and `DR-03` through `DR-07`. |
| US-05 | As a student, I want to monitor assignment status and deadlines, so that I can understand my coursework progress. | `FR-05` | `SRC-01`; `INT-S-01`; `INT-S-02` | Partial | Exact status values, confirmation details, update rules, timezone, and receipt evidence remain open under `OQ-12`, `OQ-DRAFT-01`, `OQ-DRAFT-03`, `DR-02`, `DR-07`, and `DR-08`. |
| US-06 | As a lecturer, I want to record grades for student submissions, so that assessed coursework results can be captured. | `FR-06` | `SRC-01`; `INT-L-01`; `INT-L-05` | Partial | Publication timing, correction rules, visibility, and history remain open under `OQ-06` and `DR-10`. |
| US-07 | As a lecturer, I want to provide feedback for student submissions, so that students can receive assessment comments. | `FR-07` | `SRC-01`; `INT-L-01`; `INT-L-05` | Partial | Feedback publication, visibility, history, and correction rules remain open under `OQ-06` and `DR-10`. |
| US-08 | As an administrator, I want to manage users, so that the system can support lecturer, student, and administrator participation. | `FR-08` | `SRC-01`; `INT-A-01` | Ready at high level with assumption-labelled role boundary | Authentication, role-assignment workflow, managed user fields, and multi-role account behavior remain open under `OQ-08`, `ASM-03`, `DR-12`, and `DR-13`. |
| US-09 | As an administrator, I want to manage courses, so that assignment activity can be organised around coursework context. | `FR-09` | `SRC-01`; `INT-A-01` | Ready at high level | Required course data, enrolment rules, and campus-system integration remain open under `OQ-11`, `DR-17`, and `DR-18`. |
| US-10 | As an administrator, I want to manage system configuration, so that assignment-related system settings can be controlled. | `FR-10` | `SRC-01`; `INT-A-01` | Ready at high level | Configuration items, policy authority, and governance remain open under `OQ-DRAFT-02`, `DR-14`, and `DR-18`. |
| US-11 | As a lecturer or administrator, I want assignment-related reporting support, so that assignment activity can be reviewed at a high level. | `FR-11` | `SRC-01`; `INT-L-06` | Partial | Report types, contents, filters, recipients, and access rights remain open under `OQ-07` and `DR-11`. |
| US-12 | As a lecturer, student, or administrator, I want usable assignment-related workflows, so that I can complete my role's core activities. | `NFR-01` | `SRC-01`; `INT-A-06` | Partial NFR candidate | Usability criteria and task-completion expectations remain open under `OQ-09` and `DR-16`. |
| US-13 | As an administrator or assumed IT support stakeholder, I want academic data and role-based operations protected, so that unauthorised access or modification is reduced. | `NFR-02` | `SRC-01`; `INT-A-06`; `ASM-06` | Partial / assumption-labelled | Authentication, authorisation, role assignment, audit, and retention policies remain open under `OQ-08`, `OQ-10`, `DR-12`, `DR-13`, `DR-15`, and `DR-16`. |
| US-14 | As a lecturer, student, or administrator, I want acceptable performance for assignment-related workflows, so that routine task management is not unnecessarily delayed. | `NFR-03` | `SRC-01`; `INT-A-06` | Partial NFR candidate | Response-time, throughput, capacity, and load targets remain open under `OQ-09` and `DR-16`. |
| US-15 | As a student, lecturer, or assumed IT support stakeholder, I want reliable assignment submissions and record access, so that assignment work and records remain available when needed. | `NFR-04` | `SRC-01`; `INT-A-06`; `ASM-02` | Partial / assumption-labelled | Availability, backup, recovery, upload failure handling, and incident-response targets remain open under `OQ-04`, `OQ-09`, `DR-06`, and `DR-16`. |
| US-16 | As a lecturer, student, or administrator, I want assignment, submission, grade, feedback, deadline, user, course, and configuration data to retain integrity, so that academic records remain trustworthy. | `NFR-05` | `SRC-01`; `INT-A-06`; `ASM-04`; `ASM-05`; `ASM-06` | Partial / assumption-labelled | Identifier rules, timestamp rules, correction rules, receipt evidence, and retention rules remain open under `OQ-06`, `OQ-10`, `OQ-12`, `OQ-DRAFT-03`, `DR-02`, `DR-07`, `DR-10`, and `DR-15`. |
| US-17 | As the student preparing this assignment, I want requirements artefacts to preserve traceability, so that accepted requirements can be linked back to their sources. | `CON-SPEC-01` | `README.md`; reviewed Skill 01 `OBJ-07`; reviewed Skill 02 traceability notes | Ready as assignment artefact story | This is an assignment artefact story, not a Student Task Management System product feature. |

## 5. Deferred or Blocked Story Candidates

The following topics may affect future stories or acceptance criteria, but they are not approved story candidates in this raw Skill 04 output.

| Deferred ID | Deferred topic | Blocking source or question | Skill 04 handling |
|---|---|---|---|
| `DR-01` | Mandatory assignment fields and validation rules. | `INT-L-02`; `OQ-01` | Keep blocked; do not add assignment field acceptance criteria. |
| `DR-02` | Deadline timezone, cutoff, and deadline-change behavior. | `OQ-12`; `ASM-05` | Keep blocked; do not decide timezone or cutoff rules. |
| `DR-03` | Late-submission handling. | `INT-L-03`; `OQ-02` | Keep blocked; do not decide whether late submissions are blocked, accepted, or marked. |
| `DR-04` | Resubmission and version-history behavior. | `INT-L-04`; `OQ-03` | Keep blocked; do not decide replacement or version retention rules. |
| `DR-05` | File type, file-size, storage, and upload security constraints. | `INT-S-03`; `OQ-04` | Keep blocked; do not invent file limits or upload security rules. |
| `DR-06` | Upload failure handling and recovery behavior. | `INT-S-04`; `OQ-04` | Keep blocked; do not invent retry or recovery behavior. |
| `DR-07` | Submission confirmation, receipt evidence, and dispute-handling proof. | `INT-S-02`; `OQ-DRAFT-03` | Keep blocked; do not invent receipt evidence. |
| `DR-08` | Submission-status values and update rules. | `OQ-DRAFT-01` | Keep blocked; do not invent status labels. |
| `DR-09` | Notification events and channels. | `INT-S-05`; `OQ-05` | Keep blocked; no notification story is approved. |
| `DR-10` | Grade and feedback publication, correction, history, and visibility. | `INT-L-05`; `INT-S-06`; `OQ-06` | Keep blocked; do not define publication or correction policy. |
| `DR-11` | Reporting contents, filters, recipients, and access rights. | `INT-L-06`; `OQ-07`; `ASM-01`; `ASM-06` | Keep blocked; do not define report details. |
| `DR-12` | Authentication mechanism and account-management policy. | `INT-A-02`; `OQ-08` | Keep blocked; do not choose authentication method. |
| `DR-13` | Role assignment and multi-role account behavior. | `INT-A-03`; `OQ-08`; `ASM-03` | Keep blocked; do not define role assignment workflow. |
| `DR-14` | System-wide configuration governance. | `OQ-DRAFT-02` | Keep blocked; do not decide policy authority. |
| `DR-15` | Audit and data retention policy. | `INT-A-05`; `OQ-10` | Keep blocked; do not define audit fields or retention period. |
| `DR-16` | Measurable usability, security, performance, reliability, backup, recovery, and capacity targets. | `INT-A-06`; `OQ-09`; `ASM-02` | Keep blocked; do not invent measurable NFR targets. |
| `DR-17` | External integration or standalone system boundary. | `INT-A-04`; `OQ-11`; `ASM-08` | Keep blocked; do not decide integration scope. |
| `DR-18` | Detailed administrator-managed data for users, courses, and configuration. | `INT-A-01`; `OQ-DRAFT-02` | Keep blocked; do not define exact managed data. |

## 6. Traceability to Reviewed Requirements

| Story ID | Source item | Stakeholder or objective | Supporting evidence | Related open or deferred items |
|---|---|---|---|---|
| US-01 | `FR-01` | Lecturer; `OBJ-01` | `SRC-01`; `INT-L-01` | `OQ-01`; `DR-01` |
| US-02 | `FR-02` | Lecturer; `OBJ-01` | `SRC-01`; `INT-L-01` | `OQ-02`; `OQ-12`; `DR-02`; `DR-03` |
| US-03 | `FR-03` | Student; `OBJ-02` | `SRC-01`; `INT-S-01` | `OQ-01`; `DR-01` |
| US-04 | `FR-04` | Student; `OBJ-02` | `SRC-01`; `INT-S-01` | `OQ-02`; `OQ-03`; `OQ-04`; `OQ-DRAFT-03`; `DR-03`; `DR-04`; `DR-05`; `DR-06`; `DR-07` |
| US-05 | `FR-05` | Student; `OBJ-04` | `SRC-01`; `INT-S-01`; `INT-S-02` | `OQ-12`; `OQ-DRAFT-01`; `OQ-DRAFT-03`; `DR-02`; `DR-07`; `DR-08` |
| US-06 | `FR-06` | Lecturer; `OBJ-03` | `SRC-01`; `INT-L-01`; `INT-L-05` | `OQ-06`; `DR-10` |
| US-07 | `FR-07` | Lecturer; `OBJ-03` | `SRC-01`; `INT-L-01`; `INT-L-05` | `OQ-06`; `DR-10` |
| US-08 | `FR-08` | Administrator; `OBJ-05` | `SRC-01`; `INT-A-01` | `OQ-08`; `ASM-03`; `DR-12`; `DR-13` |
| US-09 | `FR-09` | Administrator; `OBJ-05` | `SRC-01`; `INT-A-01` | `OQ-11`; `DR-17`; `DR-18` |
| US-10 | `FR-10` | Administrator; `OBJ-05` | `SRC-01`; `INT-A-01` | `OQ-DRAFT-02`; `DR-14`; `DR-18` |
| US-11 | `FR-11` | Lecturer / administrator / assumed management | `SRC-01`; `INT-L-06` | `OQ-07`; `DR-11` |
| US-12 | `NFR-01` | Lecturer / student / administrator; `OBJ-06` | `SRC-01`; `INT-A-06` | `OQ-09`; `DR-16` |
| US-13 | `NFR-02` | Administrator / assumed IT support; `OBJ-06` | `SRC-01`; `INT-A-06`; `ASM-06` | `OQ-08`; `OQ-10`; `DR-12`; `DR-13`; `DR-15`; `DR-16` |
| US-14 | `NFR-03` | Lecturer / student / administrator; `OBJ-06` | `SRC-01`; `INT-A-06` | `OQ-09`; `DR-16` |
| US-15 | `NFR-04` | Student / lecturer / assumed IT support; `OBJ-06` | `SRC-01`; `INT-A-06`; `ASM-02` | `OQ-04`; `OQ-09`; `DR-06`; `DR-16` |
| US-16 | `NFR-05` | Lecturer / student / administrator; `OBJ-06` | `SRC-01`; `INT-A-06`; `ASM-04`; `ASM-05`; `ASM-06` | `OQ-06`; `OQ-10`; `OQ-12`; `OQ-DRAFT-03`; `DR-02`; `DR-07`; `DR-10`; `DR-15` |
| US-17 | `CON-SPEC-01` | Assignment traceability requirement | `README.md`; reviewed Skill 01 `OBJ-07`; reviewed Skill 02 traceability notes | None |

## 7. Student Decisions Needed

Before these raw story candidates can become reviewed output, the student should decide whether to:

1. Accept the story list as a high-level derivation from reviewed Skill 03.
2. Merge, split, or rename story candidates without changing their source requirements.
3. Keep NFR-derived stories as story candidates, or move them into prioritisation notes only.
4. Keep deferred topics out of stories until later evidence exists.
5. Approve no new policy details during Skill 04, or return to elicitation/specification if policy details must be added.

The following topics still require explicit approval before they can become story details or acceptance criteria: late submission, resubmission, file limits, grade publication, notifications, authentication, reporting details, retention, integrations, and measurable NFR targets.

## 8. Quality Checks

| Check | Result |
|---|---|
| Based on reviewed Skill 01, Skill 02, and Skill 03 baselines. | Passed |
| No new `FR-*` or `NFR-*` requirement was created. | Passed |
| Every story maps to an existing `FR-*`, `NFR-*`, or `CON-SPEC-*` item. | Passed |
| `DR-*` topics remain deferred or blocked. | Passed |
| Partial and assumption-labelled items keep their status visible. | Passed |
| Open questions keep their original `OQ-*` or `OQ-DRAFT-*` IDs. | Passed |
| No policy was invented for late submissions, resubmissions, file limits, grade publication, notifications, authentication, reporting details, retention, integrations, or measurable NFR targets. | Passed |
| No use cases, validation results, change requests, implementation design, or acceptance criteria are included. | Passed |
