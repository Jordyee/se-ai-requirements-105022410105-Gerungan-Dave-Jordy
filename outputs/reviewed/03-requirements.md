# 03 Requirements: Reviewed Baseline

## Review Status

| Field | Value |
|---|---|
| Raw source | `outputs/raw/03-requirements.md` |
| Reviewed by | Gerungan Dave Jordy |
| Review date | 23 June 2026 |
| Review outcome | Accepted with structural revisions for clarity and evidence discipline |
| Important boundary | This document is a reviewed requirements specification baseline, not a user story, use case, prioritisation, validation, or change request artefact. |

This reviewed baseline keeps Skill 03 intentionally high-level because Skill 02 did not approve new stakeholder policies, measurable non-functional targets, integrations, or scope expansions. Unresolved areas remain deferred until answered by real stakeholder evidence, approved simulation, or explicit student decision.

## 1. Inputs and Evidence Sources

| Source | Role in this reviewed baseline | Use rule |
|---|---|---|
| `SRC-01` | Assignment case brief and case baseline in `CASE.md`. | Supports case-confirmed high-level requirements. |
| `SRC-02` | Simulated interview record in `inputs/interview-answers.md`. | Use only with simulation labels and response status. |
| `SRC-03` | Assumption register in `inputs/assumptions.md`. | Use only as labelled assumptions with `ASM-*` IDs. |
| `outputs/reviewed/01-inception.md` | Reviewed inception baseline. | Provides reviewed scope, stakeholders, constraints, quality concerns, risks, and open questions. |
| `outputs/reviewed/02-elicitation.md` | Reviewed elicitation baseline. | Provides reviewed answer classification, open questions, readiness criteria, and Skill 03 risks. |
| `evaluation/ai-output-review.md` | Student review record. | Records corrections and review rationale. |

Evidence columns in this reviewed output use source, interview, or assumption IDs. Open questions and elicitation questions are listed separately as blockers or related unresolved issues.

## 2. Specification Readiness Summary

| Area | Readiness | Supporting evidence | Open detail |
|---|---|---|---|
| Assignment creation | Supported at high level | `SRC-01`; `INT-L-01` | Mandatory fields and validation remain open under `OQ-01`. |
| Deadline definition | Supported at high level | `SRC-01`; `INT-L-01` | Timezone, cutoff, deadline-change, and late-submission rules remain open under `OQ-02` and `OQ-12`. |
| Assignment viewing | Supported at high level | `SRC-01`; `INT-S-01` | Exact student-facing fields remain open. |
| File submission | Supported at high level | `SRC-01`; `INT-S-01` | File policy, failure handling, late submission, resubmission, and receipt evidence remain open under `OQ-02`, `OQ-03`, `OQ-04`, and `OQ-DRAFT-03`. |
| Status and deadline monitoring | Partial | `SRC-01`; `INT-S-01`; `INT-S-02` | Status values, confirmation details, and update rules remain open under `OQ-DRAFT-01`, `OQ-DRAFT-03`, and `OQ-12`. |
| Grading and feedback | Partial | `SRC-01`; `INT-L-01`; `INT-L-05`; `INT-S-06` | Publication, correction, visibility, and history remain open under `OQ-06`. |
| User, course, and configuration administration | Supported at high level | `SRC-01`; `INT-A-01` | Exact managed data, authentication, role assignment, and governance remain open under `OQ-08`, `OQ-11`, and `OQ-DRAFT-02`. |
| Reporting | Partial | `SRC-01`; `INT-L-06` | Report types, fields, recipients, filters, and access rights remain open under `OQ-07`. |
| Quality concerns | Partial | `SRC-01`; `INT-A-06` | Measurable usability, security, performance, reliability, backup, recovery, capacity, and data-integrity targets remain open under `OQ-09`. |

## 3. Functional Requirements

| ID | Requirement statement | Status | Supporting evidence | Open issues |
|---|---|---|---|---|
| FR-01 | The system shall allow lecturers to create assignments. | Supported at high level | `SRC-01`; `INT-L-01` | Mandatory fields, validation rules, templates, attachments, and publishing workflow are not specified. See `OQ-01`. |
| FR-02 | The system shall allow lecturers to define assignment deadlines. | Supported at high level | `SRC-01`; `INT-L-01` | Timezone, cutoff behavior, deadline changes, and late-submission handling are not specified. See `OQ-02` and `OQ-12`. |
| FR-03 | The system shall allow students to view assignment information. | Supported at high level | `SRC-01`; `INT-S-01` | Exact assignment fields and display expectations are not specified. See `OQ-01`. |
| FR-04 | The system shall allow students to submit files for assignments. | Supported at high level | `SRC-01`; `INT-S-01` | File types, file size, upload failure handling, late submission, resubmission, and receipt evidence are not specified. See `OQ-02`, `OQ-03`, `OQ-04`, and `OQ-DRAFT-03`. |
| FR-05 | The system shall allow students to monitor assignment status and deadlines. | Partial | `SRC-01`; `INT-S-01`; `INT-S-02` | Exact status values, confirmation details, and update rules are not specified. See `OQ-DRAFT-01`, `OQ-DRAFT-03`, and `OQ-12`. |
| FR-06 | The system shall allow lecturers to record grades for student submissions. | Partial | `SRC-01`; `INT-L-01`; `INT-L-05` | Publication timing, correction rules, visibility, and history are not specified. See `OQ-06`. |
| FR-07 | The system shall allow lecturers to provide feedback for student submissions. | Partial | `SRC-01`; `INT-L-01`; `INT-L-05` | Feedback publication, visibility, history, and correction rules are not specified. See `OQ-06`. |
| FR-08 | The system shall allow administrators to manage users. | Supported at high level | `SRC-01`; `INT-A-01` | Authentication, role-assignment workflow, managed user fields, and multi-role account behavior are not specified. See `OQ-08` and `ASM-03`. |
| FR-09 | The system shall allow administrators to manage courses. | Supported at high level | `SRC-01`; `INT-A-01` | Required course data, enrolment rules, and integration with campus systems are not specified. See `OQ-11`. |
| FR-10 | The system shall allow administrators to manage system configuration. | Supported at high level | `SRC-01`; `INT-A-01` | Configuration items, policy authority, and governance are not specified. See `OQ-DRAFT-02`. |
| FR-11 | The system shall support assignment-related reporting at a high level. | Partial | `SRC-01`; `INT-L-06` | Report types, contents, filters, recipients, and access rights are not specified. See `OQ-07`. |

## 4. Quality Concerns and Partial NFR Candidates

These items are retained as quality concerns and partial non-functional requirement candidates. They are not fully testable NFRs until measurable targets or policies are approved.

| ID | Quality concern / partial NFR candidate | Status | Supporting evidence | Open issues |
|---|---|---|---|---|
| NFR-01 | The system should support usable lecturer, student, and administrator workflows for assignment-related activities. | Partial | `SRC-01`; `INT-A-06` | Usability criteria and task-completion expectations are not specified. See `OQ-09`. |
| NFR-02 | The system should protect academic data and role-based operations from unauthorised access or modification. | Partial / assumption-labelled | `SRC-01`; `INT-A-06`; `ASM-06` | Authentication, authorisation, role assignment, audit, and retention policies are not specified. See `OQ-08` and `OQ-10`. |
| NFR-03 | The system should support acceptable performance for assignment creation, viewing, submission, grading, feedback, administration, and reporting workflows. | Partial | `SRC-01`; `INT-A-06` | Response-time, throughput, capacity, and load targets are not specified. See `OQ-09`. |
| NFR-04 | The system should support reliable assignment submissions and assignment-related record access. | Partial | `SRC-01`; `INT-A-06` | Availability, backup, recovery, upload failure handling, and incident-response targets are not specified. See `OQ-04` and `OQ-09`. |
| NFR-05 | The system should protect integrity of assignment, submission, grade, feedback, deadline, user, course, and configuration data. | Partial / assumption-labelled | `SRC-01`; `INT-A-06`; `ASM-04`; `ASM-05`; `ASM-06` | Identifier rules, timestamp rules, correction rules, receipt evidence, and retention rules are not specified. See `OQ-06`, `OQ-10`, `OQ-12`, and `OQ-DRAFT-03`. |

## 5. Specification Constraints and Artefact Requirements

| ID | Constraint or artefact requirement | Evidence | Status |
|---|---|---|---|
| CON-SPEC-01 | Requirements artefacts must preserve traceability between accepted requirements and their supporting sources. | `README.md`; reviewed Skill 01 `OBJ-07`; reviewed Skill 02 traceability notes | Supported |
| CON-SPEC-02 | Raw AI output must remain separate from reviewed output. | `README.md`; `evaluation/ai-output-review.md` | Supported |
| CON-SPEC-03 | Case facts, simulated evidence, assumptions, open questions, and deferred topics must remain distinguishable. | `README.md`; `SRC-01`; `SRC-02`; `SRC-03` | Supported |
| CON-SPEC-04 | The requirements specification must remain independent of implementation technology unless later approved. | `ASM-08`; reviewed Skill 01 constraints | Assumption-labelled working rule |

## 6. Deferred Requirement Topics

Deferred topics are not approved requirements. They identify areas that require stakeholder evidence, approved simulation, or explicit student decision before detailed specification.

| ID | Deferred topic | Blocking source or question | Reason |
|---|---|---|---|
| DR-01 | Mandatory assignment fields and validation rules. | `INT-L-02`; `OQ-01` | The case confirms assignment creation but not required assignment data. |
| DR-02 | Deadline timezone, cutoff, and deadline-change behavior. | `OQ-12`; `ASM-05` | Time-related interpretation remains undefined. |
| DR-03 | Late-submission handling. | `INT-L-03`; `OQ-02` | No approved policy exists. |
| DR-04 | Resubmission and version-history behavior. | `INT-L-04`; `OQ-03` | No approved policy exists. |
| DR-05 | File type, file-size, storage, and upload security constraints. | `INT-S-03`; `OQ-04` | No approved file policy exists. |
| DR-06 | Upload failure handling and recovery behavior. | `INT-S-04`; `OQ-04` | Failure handling is not specified. |
| DR-07 | Submission confirmation, receipt evidence, and dispute-handling proof. | `INT-S-02`; `OQ-DRAFT-03` | Status monitoring is confirmed, but proof details are undefined. |
| DR-08 | Submission-status values and update rules. | `OQ-DRAFT-01` | The status model is undefined. |
| DR-09 | Notification events and channels. | `INT-S-05`; `OQ-05` | No notification requirement is approved. |
| DR-10 | Grade and feedback publication, correction, history, and visibility. | `INT-L-05`; `INT-S-06`; `OQ-06` | Grading and feedback are confirmed only at topic level. |
| DR-11 | Reporting contents, filters, recipients, and access rights. | `INT-L-06`; `OQ-07`; `ASM-01`; `ASM-06` | Reporting is mentioned but not defined. |
| DR-12 | Authentication mechanism and account-management policy. | `INT-A-02`; `OQ-08` | Security mechanism is not provided. |
| DR-13 | Role assignment and multi-role account behavior. | `INT-A-03`; `OQ-08`; `ASM-03` | Role types are distinguishable, but assignment workflow is undefined. |
| DR-14 | System-wide configuration governance. | `OQ-DRAFT-02` | Authority to configure policy is undefined. |
| DR-15 | Audit and data retention policy. | `INT-A-05`; `OQ-10` | Retained records and retention period are undefined. |
| DR-16 | Measurable usability, security, performance, reliability, backup, recovery, and capacity targets. | `INT-A-06`; `OQ-09`; `ASM-02` | Quality areas are confirmed, but measurable targets are not approved. |
| DR-17 | External integration or standalone system boundary. | `INT-A-04`; `OQ-11`; `ASM-08` | No integration decision exists. |
| DR-18 | Detailed administrator-managed data for users, courses, and configuration. | `INT-A-01`; `OQ-DRAFT-02` | Administration is confirmed, but exact data and policy items remain undefined. |

## 7. Assumption-Labelled Items

| Assumption | Current reviewed status | Possible relevance | Boundary |
|---|---|---|---|
| `ASM-01` | Accepted working assumption | Academic management may be a secondary stakeholder for policy and reporting. | Does not define report contents, approval authority, or retention policy. |
| `ASM-02` | Accepted working assumption | IT support or system operator may own operational quality concerns. | Does not define availability, backup, recovery, monitoring, or security targets. |
| `ASM-03` | Revised working assumption | The system distinguishes at least lecturer, student, and administrator roles. | Does not define account model, role assignment, or multi-role behavior. |
| `ASM-04` | Accepted working assumption | Assignment and submission records may require stable identifiers. | Does not define identifier format or database design. |
| `ASM-05` | Accepted working assumption | Deadlines and submissions may need timestamps. | Does not define timezone, cutoff, late policy, or clock source. |
| `ASM-06` | Accepted working assumption | Grades and submissions should be protected by authorised access. | Does not define authentication, authorisation matrix, audit policy, or retention. |
| `ASM-07` | Accepted working scope boundary | Chat, plagiarism detection, payment, attendance, and video conferencing are excluded unless later approved. | Exclusion can change only through later elicitation or change management. |
| `ASM-08` | Accepted working rule | Requirements should remain independent of implementation technology. | Does not decide standalone or integration architecture. |

## 8. Traceability Matrix

| Item | Stakeholder or objective | Supporting evidence | Related open or deferred items |
|---|---|---|---|
| `FR-01` | Lecturer; `OBJ-01` | `SRC-01`; `INT-L-01` | `OQ-01`; `DR-01` |
| `FR-02` | Lecturer; `OBJ-01` | `SRC-01`; `INT-L-01` | `OQ-02`; `OQ-12`; `DR-02`; `DR-03` |
| `FR-03` | Student; `OBJ-02` | `SRC-01`; `INT-S-01` | `OQ-01`; `DR-01` |
| `FR-04` | Student; `OBJ-02` | `SRC-01`; `INT-S-01` | `OQ-02`; `OQ-03`; `OQ-04`; `OQ-DRAFT-03`; `DR-03`; `DR-04`; `DR-05`; `DR-06`; `DR-07` |
| `FR-05` | Student; `OBJ-04` | `SRC-01`; `INT-S-01`; `INT-S-02` | `OQ-12`; `OQ-DRAFT-01`; `OQ-DRAFT-03`; `DR-02`; `DR-07`; `DR-08` |
| `FR-06` | Lecturer; `OBJ-03` | `SRC-01`; `INT-L-01`; `INT-L-05` | `OQ-06`; `DR-10` |
| `FR-07` | Lecturer; `OBJ-03` | `SRC-01`; `INT-L-01`; `INT-L-05` | `OQ-06`; `DR-10` |
| `FR-08` | Administrator; `OBJ-05` | `SRC-01`; `INT-A-01` | `OQ-08`; `ASM-03`; `DR-12`; `DR-13` |
| `FR-09` | Administrator; `OBJ-05` | `SRC-01`; `INT-A-01` | `OQ-11`; `DR-17`; `DR-18` |
| `FR-10` | Administrator; `OBJ-05` | `SRC-01`; `INT-A-01` | `OQ-DRAFT-02`; `DR-14`; `DR-18` |
| `FR-11` | Lecturer / administrator / assumed management | `SRC-01`; `INT-L-06` | `OQ-07`; `DR-11` |
| `NFR-01` | Lecturer / student / administrator; `OBJ-06` | `SRC-01`; `INT-A-06` | `OQ-09`; `DR-16` |
| `NFR-02` | Administrator / assumed IT support; `OBJ-06` | `SRC-01`; `INT-A-06`; `ASM-06` | `OQ-08`; `OQ-10`; `DR-12`; `DR-13`; `DR-15`; `DR-16` |
| `NFR-03` | Lecturer / student / administrator; `OBJ-06` | `SRC-01`; `INT-A-06` | `OQ-09`; `DR-16` |
| `NFR-04` | Student / lecturer / assumed IT support; `OBJ-06` | `SRC-01`; `INT-A-06`; `ASM-02` | `OQ-04`; `OQ-09`; `DR-06`; `DR-16` |
| `NFR-05` | Lecturer / student / administrator; `OBJ-06` | `SRC-01`; `INT-A-06`; `ASM-04`; `ASM-05`; `ASM-06` | `OQ-06`; `OQ-10`; `OQ-12`; `OQ-DRAFT-03`; `DR-02`; `DR-07`; `DR-10`; `DR-15` |
| `CON-SPEC-01` | Assignment traceability requirement | `README.md`; reviewed Skill 01 and Skill 02 traceability notes | None |

## 9. Student Decisions Still Needed

Before later detailed requirements can be added, the student must decide whether to:

1. Keep all unresolved policy areas deferred.
2. Approve simulated stakeholder answers for late submission, resubmission, file limits, grade publication, notifications, authentication, reporting, retention, integrations, or measurable NFR targets.
3. Approve whether assumption-supported items such as stable identifiers, timestamps, and authorised access may remain as reviewed assumption-labelled requirements.
4. Define measurable usability, security, performance, reliability, backup, recovery, capacity, and data-integrity targets.
5. Keep reporting as a high-level case capability or add detailed report requirements through approved evidence.

## 10. Review Quality Checks

| Check | Result |
|---|---|
| Based on reviewed Skill 01 and Skill 02 baselines. | Passed |
| Raw output preserved separately from reviewed output. | Passed |
| Requirement evidence separated from open questions and elicitation questions. | Passed |
| Requirement IDs and deferred topic IDs are stable. | Passed |
| Assumptions keep `ASM-*` labels and are not converted into confirmed facts. | Passed |
| Open questions keep `OQ-*` or `OQ-DRAFT-*` IDs. | Passed |
| No policy is invented for late submissions, resubmissions, file limits, grade publication, notifications, authentication, reporting access, retention, integrations, or measurable NFR targets. | Passed |
| No user stories, use cases, priorities, validation results, or change requests are included. | Passed |
