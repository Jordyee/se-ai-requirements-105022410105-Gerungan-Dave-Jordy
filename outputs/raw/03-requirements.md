# Skill 03 Raw Output: Requirements Specification

## 1. Review Status and Boundary

| Field | Value |
|---|---|
| Output type | First AI-generated Skill 03 requirements specification draft |
| Raw output status | Awaiting student review |
| Date generated | 23 June 2026 |
| Boundary | Requirements specification only |
| Excluded from this output | User stories, use cases, prioritisation, validation results, change requests, implementation design, and reviewed requirements |

This raw output uses only the reviewed Skill 01 and Skill 02 baselines as authority for specification. It does not approve new stakeholder answers, policy choices, measurable non-functional targets, integrations, or scope expansions.

Unresolved areas from Skill 02 remain open or deferred. No requirement below decides late submission, resubmission, file limits, grade publication, notifications, authentication, reporting details, retention, integrations, or measurable non-functional targets.

## 2. Inputs and Evidence Sources

| Source | Role in this specification draft | Use rule |
|---|---|---|
| `SRC-01` | Assignment case brief and case baseline in `CASE.md`. | May support case-confirmed high-level requirements. |
| `SRC-02` | Simulated interview record in `inputs/interview-answers.md`. | Use only with simulation labels and response status. |
| `SRC-03` | Assumption register in `inputs/assumptions.md`. | Use only as labelled assumptions with `ASM-*` IDs. |
| `outputs/reviewed/01-inception.md` | Reviewed inception baseline. | Use for problem, scope, stakeholders, constraints, quality concerns, and open questions. |
| `outputs/reviewed/02-elicitation.md` | Reviewed elicitation baseline. | Use for answer classification, open questions, readiness criteria, and Skill 03 risks. |
| `evaluation/ai-output-review.md` | Student review record for earlier raw AI outputs. | Use to preserve correction and review boundaries. |

Relevant reviewed decisions:

- Skill 01 and Skill 02 raw outputs were reviewed and accepted with minor clarification.
- Skill 02 approved no new stakeholder policy, measurable non-functional target, integration decision, or scope expansion.
- All `OQ-*` and `OQ-DRAFT-*` questions remain open until answered by real stakeholder evidence, approved simulation, or explicit student decision.
- Assumptions keep their `ASM-*` labels and must not become confirmed facts.

## 3. Specification Readiness Map

### 3.1 Ready for High-Level Requirements

| Capability or concern | Evidence | Specification readiness |
|---|---|---|
| Lecturer creates assignments. | `SRC-01`; `INT-L-01`; `OBJ-01` | Ready only at high level. Mandatory fields remain open. |
| Lecturer defines deadlines. | `SRC-01`; `INT-L-01`; `OBJ-01` | Ready only at high level. Timezone and cutoff rules remain open. |
| Student views assignments. | `SRC-01`; `INT-S-01`; `OBJ-02` | Ready only at high level. Student-facing detail expectations remain open. |
| Student submits files. | `SRC-01`; `INT-S-01`; `OBJ-02` | Ready only at high level. File policy, failure handling, late submission, and resubmission remain open. |
| Student monitors assignment status and deadlines. | `SRC-01`; `INT-S-01`; `OBJ-04` | Ready only at high level. Exact status labels and confirmation details remain open. |
| Lecturer records grades. | `SRC-01`; `INT-L-01`; `OBJ-03` | Ready only at high level. Publication, correction, and history rules remain open. |
| Lecturer provides feedback. | `SRC-01`; `INT-L-01`; `OBJ-03` | Ready only at high level. Feedback visibility and history remain open. |
| Administrator manages users, courses, and system configuration. | `SRC-01`; `INT-A-01`; `OBJ-05` | Ready only at high level. Managed data, role assignment, and governance remain open. |
| Assignment-related reporting. | `SRC-01`; `INT-L-06` | Partially ready at high level. Report types, fields, recipients, and access remain open. |
| Usability, security, performance, reliability, and data integrity. | `SRC-01`; `INT-A-06`; `OBJ-06` | Ready only as quality concerns. Measurable targets and detailed policies remain open. |

### 3.2 Not Ready for Detailed Specification

| Area | Blocking evidence | Reason |
|---|---|---|
| Mandatory assignment fields | `INT-L-02`; `OQ-01`; `ELQ-L-01` | The case does not specify required assignment data. |
| Late-submission handling | `INT-L-03`; `OQ-02`; `ELQ-L-03`; `ELQ-M-01` | No approved policy states whether late submissions are blocked, accepted, marked, or controlled per assignment. |
| Resubmission and version history | `INT-L-04`; `OQ-03`; `ELQ-L-04` | No approved policy states whether submitted files may be replaced or versioned. |
| File restrictions and failed uploads | `INT-S-03`; `INT-S-04`; `OQ-04`; `ELQ-S-03`; `ELQ-S-04`; `ELQ-IT-01` | File formats, file size, security constraints, and failure recovery are undefined. |
| Notification behavior | `INT-S-05`; `OQ-05`; `ELQ-S-05` | Events and channels are undefined. |
| Grade and feedback publication | `INT-L-05`; `INT-S-06`; `OQ-06`; `ELQ-L-06`; `ELQ-S-07`; `ELQ-M-02` | Visibility, history, correction, and audit rules are undefined. |
| Reporting details | `INT-L-06`; `OQ-07`; `ELQ-L-07`; `ELQ-M-03` | Report contents, filters, recipients, and access rights are undefined. |
| Authentication and role assignment | `INT-A-02`; `INT-A-03`; `OQ-08`; `ELQ-A-02`; `ELQ-A-03`; `ASM-03` | Mechanism, assignment authority, and multi-role account behavior are undefined. |
| Measurable NFR targets | `INT-A-06`; `OQ-09`; `ELQ-A-07`; `ELQ-IT-03` | Response time, capacity, availability, backup, and recovery targets are undefined. |
| Retention and audit | `INT-A-05`; `OQ-10`; `ELQ-A-06`; `ELQ-M-04` | Stored audit details and retention periods are undefined. |
| Integration boundary | `INT-A-04`; `OQ-11`; `ELQ-A-05`; `ELQ-IT-04`; `ASM-08` | No approved standalone or integration decision exists. |
| Deadline timezone and cutoff | `OQ-12`; `ELQ-L-02` | Deadline interpretation is undefined. |
| Submission-status model | `OQ-DRAFT-01`; `ELQ-L-05`; `ELQ-S-06` | Exact status values are undefined. |
| System-wide policy governance | `OQ-DRAFT-02`; `ELQ-A-04` | Configuration authority is undefined. |
| Submission receipt evidence | `OQ-DRAFT-03`; `ELQ-L-08`; `ELQ-S-02` | Proof content and dispute-handling evidence are undefined. |

## 4. Functional Requirements

| ID | Requirement statement | Type | Evidence | Status | Notes or boundary |
|---|---|---|---|---|---|
| FR-01 | The system shall allow lecturers to create assignments. | Functional | `SRC-01`; `INT-L-01`; `OBJ-01` | Supported | This does not define mandatory assignment fields, validation rules, templates, attachments, or publishing workflow. See `OQ-01`. |
| FR-02 | The system shall allow lecturers to define assignment deadlines. | Functional | `SRC-01`; `INT-L-01`; `OBJ-01` | Supported | This does not define timezone, cutoff behavior, late handling, or deadline-change policy. See `OQ-02` and `OQ-12`. |
| FR-03 | The system shall allow students to view assignment information. | Functional | `SRC-01`; `INT-S-01`; `OBJ-02` | Supported | This does not define the exact assignment fields or student-facing layout. See `ELQ-S-01` and `OQ-01`. |
| FR-04 | The system shall allow students to submit files for assignments. | Functional | `SRC-01`; `INT-S-01`; `OBJ-02` | Supported | This does not define file types, file size, upload failure handling, late submission, resubmission, or receipt evidence. See `OQ-02`, `OQ-03`, `OQ-04`, and `OQ-DRAFT-03`. |
| FR-05 | The system shall allow students to monitor assignment status and deadlines. | Functional | `SRC-01`; `INT-S-01`; `OBJ-04`; `INT-S-02` | Partial | The case confirms status and deadline monitoring, but exact status values, confirmation details, and update rules remain open. See `OQ-DRAFT-01`, `OQ-DRAFT-03`, and `OQ-12`. |
| FR-06 | The system shall allow lecturers to record grades for student submissions. | Functional | `SRC-01`; `INT-L-01`; `OBJ-03`; `INT-L-05` | Partial | Grading is confirmed, but publication timing, correction rules, visibility, and history remain open. See `OQ-06`. |
| FR-07 | The system shall allow lecturers to provide feedback for student submissions. | Functional | `SRC-01`; `INT-L-01`; `OBJ-03`; `INT-L-05` | Partial | Feedback is confirmed, but visibility, history, correction, and publication rules remain open. See `OQ-06`. |
| FR-08 | The system shall allow administrators to manage users. | Functional | `SRC-01`; `INT-A-01`; `OBJ-05` | Supported | This does not define authentication, role-assignment workflow, managed user fields, or multi-role account behavior. See `OQ-08` and `ASM-03`. |
| FR-09 | The system shall allow administrators to manage courses. | Functional | `SRC-01`; `INT-A-01`; `OBJ-05` | Supported | This does not define required course data, enrolment rules, or integration with campus systems. See `OQ-11` and `ELQ-A-01`. |
| FR-10 | The system shall allow administrators to manage system configuration. | Functional | `SRC-01`; `INT-A-01`; `OBJ-05` | Supported | This does not define configuration items, policy authority, or governance. See `OQ-DRAFT-02`. |
| FR-11 | The system shall support assignment-related reporting at a high level. | Functional | `SRC-01`; `INT-L-06` | Partial | Reporting is mentioned, but report types, contents, filters, recipients, and access rights remain open. See `OQ-07`. |
| FR-12 | The system shall preserve traceability between accepted requirements and their evidence sources. | Functional | `README.md`; `SRC-01`; reviewed Skill 01 `OBJ-07`; reviewed Skill 02 traceability notes | Supported | This is an assignment artefact requirement, not an end-user product feature. |

## 5. Non-Functional Requirements

| ID | Requirement statement | Type | Evidence | Status | Notes or boundary |
|---|---|---|---|---|---|
| NFR-01 | The system shall consider usability for lecturer, student, and administrator assignment-related workflows. | Non-functional | `SRC-01`; `INT-A-06`; `OBJ-06` | Partial | No measurable usability criteria or task-completion targets are approved. See `OQ-09`. |
| NFR-02 | The system shall consider security for academic data and role-based operations. | Non-functional | `SRC-01`; `INT-A-06`; `OBJ-06`; `ASM-06` | Partial | Authentication, authorisation, role assignment, audit, and retention policies remain open. `ASM-06` remains a labelled assumption. See `OQ-08` and `OQ-10`. |
| NFR-03 | The system shall consider performance for assignment creation, viewing, submission, grading, feedback, administration, and reporting workflows. | Non-functional | `SRC-01`; `INT-A-06`; `OBJ-06` | Partial | No response-time, throughput, capacity, or load target is approved. See `OQ-09`. |
| NFR-04 | The system shall consider reliability for assignment submissions and assignment-related records. | Non-functional | `SRC-01`; `INT-A-06`; `OBJ-06` | Partial | Availability, backup, recovery, failure handling, and incident-response targets remain open. See `OQ-04` and `OQ-09`. |
| NFR-05 | The system shall consider data integrity for assignment, submission, grade, feedback, deadline, user, course, and configuration data. | Non-functional | `SRC-01`; `INT-A-06`; `OBJ-06`; `ASM-04`; `ASM-05`; `ASM-06` | Partial | Stable identifiers, timestamps, and authorised access are assumption-supported but still need detailed validation rules and policy approval. See `OQ-06`, `OQ-10`, `OQ-12`, and `OQ-DRAFT-03`. |

## 6. Deferred Requirement Topics

Deferred topics are not approved requirements. They identify areas that require stakeholder evidence, approved simulation, or explicit student decision before detailed specification.

| ID | Deferred topic | Evidence | Reason |
|---|---|---|---|
| DR-01 | Mandatory assignment fields and assignment validation rules. | `INT-L-02`; `OQ-01`; `ELQ-L-01` | The case confirms assignment creation but not required data or validation. |
| DR-02 | Deadline timezone, cutoff, and deadline-change behavior. | `OQ-12`; `ELQ-L-02`; `ASM-05` | Time-related interpretation remains undefined. |
| DR-03 | Late-submission handling. | `INT-L-03`; `OQ-02`; `ELQ-L-03`; `ELQ-M-01` | No approved policy exists. |
| DR-04 | Resubmission and version-history behavior. | `INT-L-04`; `OQ-03`; `ELQ-L-04` | No approved policy exists. |
| DR-05 | File type, file-size, storage, and security constraints for uploads. | `INT-S-03`; `OQ-04`; `ELQ-S-03`; `ELQ-IT-01` | No approved file policy exists. |
| DR-06 | Upload failure handling and recovery behavior. | `INT-S-04`; `OQ-04`; `ELQ-S-04` | Failure handling is not specified. |
| DR-07 | Submission confirmation, receipt evidence, and dispute-handling proof. | `INT-S-02`; `OQ-DRAFT-03`; `ELQ-S-02`; `ELQ-L-08` | Status monitoring is confirmed, but proof details are undefined. |
| DR-08 | Submission-status values and update rules. | `OQ-DRAFT-01`; `ELQ-L-05`; `ELQ-S-06` | The status model is undefined. |
| DR-09 | Notification events and channels. | `INT-S-05`; `OQ-05`; `ELQ-S-05` | No notification requirement is approved. |
| DR-10 | Grade and feedback publication, correction, history, and visibility. | `INT-L-05`; `INT-S-06`; `OQ-06`; `ELQ-L-06`; `ELQ-S-07`; `ELQ-M-02` | Grading and feedback are confirmed only at topic level. |
| DR-11 | Reporting contents, filters, recipients, and access rights. | `INT-L-06`; `OQ-07`; `ELQ-L-07`; `ELQ-M-03`; `ASM-01`; `ASM-06` | Reporting is mentioned but not defined. |
| DR-12 | Authentication mechanism and account-management policy. | `INT-A-02`; `OQ-08`; `ELQ-A-02`; `ELQ-IT-02` | Security mechanism is not provided. |
| DR-13 | Role assignment and multi-role account behavior. | `INT-A-03`; `OQ-08`; `ELQ-A-03`; `ASM-03` | Role types are distinguishable, but assignment workflow is undefined. |
| DR-14 | System-wide configuration governance. | `OQ-DRAFT-02`; `ELQ-A-04` | Authority to configure policy is undefined. |
| DR-15 | Audit and data retention policy. | `INT-A-05`; `OQ-10`; `ELQ-A-06`; `ELQ-M-04` | Retained records and retention period are undefined. |
| DR-16 | Measurable usability, security, performance, reliability, backup, recovery, and capacity targets. | `INT-A-06`; `OQ-09`; `ELQ-A-07`; `ELQ-IT-03` | Quality areas are confirmed, but measurable targets are not approved. |
| DR-17 | External integration or standalone system boundary. | `INT-A-04`; `OQ-11`; `ELQ-A-05`; `ELQ-IT-04`; `ASM-08` | No integration decision exists. |
| DR-18 | Detailed administrator-managed data for users, courses, and configuration. | `INT-A-01`; `ELQ-A-01`; `OQ-DRAFT-02` | Administration is confirmed, but exact data and policy items remain undefined. |

## 7. Open Questions Blocking Detail

| ID | Blocking question | Affected requirements |
|---|---|---|
| `OQ-01` | What assignment fields are mandatory when a lecturer creates an assignment? | `FR-01`; `FR-03`; `DR-01` |
| `OQ-02` | Are late submissions blocked, accepted with a marker, or controlled per assignment? | `FR-02`; `FR-04`; `DR-03` |
| `OQ-03` | May students replace a submitted file before the deadline, and must version history be retained? | `FR-04`; `DR-04`; `NFR-05` |
| `OQ-04` | Which file types and maximum file sizes are allowed? | `FR-04`; `NFR-04`; `DR-05`; `DR-06` |
| `OQ-05` | Which events require notifications, and through which channels? | `DR-09` |
| `OQ-06` | Can grades or feedback be changed after publication? | `FR-06`; `FR-07`; `NFR-05`; `DR-10` |
| `OQ-07` | What reports are required and who may access them? | `FR-11`; `DR-11` |
| `OQ-08` | How are users authenticated and roles assigned? | `FR-08`; `NFR-02`; `DR-12`; `DR-13` |
| `OQ-09` | What response-time, availability, backup, and recovery targets apply? | `NFR-01`; `NFR-03`; `NFR-04`; `DR-16` |
| `OQ-10` | What personal or academic data retention rules apply? | `NFR-02`; `NFR-05`; `DR-15` |
| `OQ-11` | Is the system standalone or integrated with an existing campus system? | `FR-09`; `DR-17` |
| `OQ-12` | Which timezone and deadline cut-off rules apply? | `FR-02`; `FR-05`; `DR-02` |
| `OQ-DRAFT-01` | What exact submission-status values should be displayed to students and lecturers? | `FR-05`; `DR-08` |
| `OQ-DRAFT-02` | Who is allowed to configure system-wide assignment policies? | `FR-10`; `DR-14`; `DR-18` |
| `OQ-DRAFT-03` | What evidence should be stored to prove that a submission was received? | `FR-04`; `FR-05`; `DR-07`; `NFR-05` |

## 8. Assumption-Labelled Items

These items may inform later specification, but they are not confirmed facts. Where they affect policy, security, or measurable NFR detail, they require explicit student approval before becoming reviewed requirements.

| Assumption | Current reviewed status | Possible specification relevance | Boundary |
|---|---|---|---|
| `ASM-01` | Accepted working assumption | Academic management may be a secondary stakeholder for policy and reporting. | Does not define report contents, approval authority, or retention policy. |
| `ASM-02` | Accepted working assumption | IT support or system operator may own operational quality concerns. | Does not define availability, backup, recovery, monitoring, or security targets. |
| `ASM-03` | Revised working assumption | The system distinguishes at least lecturer, student, and administrator roles. | Does not define account model, role assignment, or multi-role behavior. |
| `ASM-04` | Accepted working assumption | Assignment and submission records may require stable identifiers. | Does not define identifier format or database design. |
| `ASM-05` | Accepted working assumption | Deadlines and submissions may need timestamps. | Does not define timezone, cutoff, late policy, or clock source. |
| `ASM-06` | Accepted working assumption | Grades and submissions should be protected by authorised access. | Does not define authentication, authorisation matrix, audit policy, or retention. |
| `ASM-07` | Accepted working scope boundary | Chat, plagiarism detection, payment, attendance, and video conferencing are excluded unless later approved. | Exclusion can change only through later elicitation or change management. |
| `ASM-08` | Accepted working rule | Requirements should remain independent of implementation technology. | Does not decide standalone or integration architecture. |

## 9. Traceability Matrix

| Requirement | Stakeholder or objective | Evidence | Related open or deferred items |
|---|---|---|---|
| `FR-01` | Lecturer; `OBJ-01` | `SRC-01`; `INT-L-01` | `OQ-01`; `DR-01` |
| `FR-02` | Lecturer; `OBJ-01` | `SRC-01`; `INT-L-01` | `OQ-02`; `OQ-12`; `DR-02`; `DR-03` |
| `FR-03` | Student; `OBJ-02` | `SRC-01`; `INT-S-01` | `OQ-01`; `ELQ-S-01`; `DR-01` |
| `FR-04` | Student; `OBJ-02` | `SRC-01`; `INT-S-01` | `OQ-02`; `OQ-03`; `OQ-04`; `OQ-DRAFT-03`; `DR-03`; `DR-04`; `DR-05`; `DR-06`; `DR-07` |
| `FR-05` | Student; `OBJ-04` | `SRC-01`; `INT-S-01`; `INT-S-02` | `OQ-12`; `OQ-DRAFT-01`; `OQ-DRAFT-03`; `DR-02`; `DR-07`; `DR-08` |
| `FR-06` | Lecturer; `OBJ-03` | `SRC-01`; `INT-L-01`; `INT-L-05` | `OQ-06`; `DR-10` |
| `FR-07` | Lecturer; `OBJ-03` | `SRC-01`; `INT-L-01`; `INT-L-05` | `OQ-06`; `DR-10` |
| `FR-08` | Administrator; `OBJ-05` | `SRC-01`; `INT-A-01` | `OQ-08`; `ASM-03`; `DR-12`; `DR-13` |
| `FR-09` | Administrator; `OBJ-05` | `SRC-01`; `INT-A-01` | `OQ-11`; `DR-17`; `DR-18` |
| `FR-10` | Administrator; `OBJ-05` | `SRC-01`; `INT-A-01` | `OQ-DRAFT-02`; `DR-14`; `DR-18` |
| `FR-11` | Lecturer / administrator / assumed management | `SRC-01`; `INT-L-06`; `ASM-01`; `ASM-06` | `OQ-07`; `DR-11` |
| `FR-12` | Assignment process; `OBJ-07` | `README.md`; `SRC-01`; reviewed Skill 01 and Skill 02 traceability notes | None for this artefact-level requirement. |
| `NFR-01` | Lecturer / student / administrator; `OBJ-06` | `SRC-01`; `INT-A-06` | `OQ-09`; `DR-16` |
| `NFR-02` | Administrator / assumed IT support; `OBJ-06` | `SRC-01`; `INT-A-06`; `ASM-06` | `OQ-08`; `OQ-10`; `DR-12`; `DR-13`; `DR-15`; `DR-16` |
| `NFR-03` | Lecturer / student / administrator; `OBJ-06` | `SRC-01`; `INT-A-06` | `OQ-09`; `DR-16` |
| `NFR-04` | Student / lecturer / assumed IT support; `OBJ-06` | `SRC-01`; `INT-A-06`; `ASM-02` | `OQ-04`; `OQ-09`; `DR-06`; `DR-16` |
| `NFR-05` | Lecturer / student / administrator; `OBJ-06` | `SRC-01`; `INT-A-06`; `ASM-04`; `ASM-05`; `ASM-06` | `OQ-06`; `OQ-10`; `OQ-12`; `OQ-DRAFT-03`; `DR-02`; `DR-07`; `DR-10`; `DR-15` |

## 10. Student Decisions Needed

Before the reviewed Skill 03 requirements baseline can be completed, the student must decide whether to:

1. Keep this specification limited to high-level case-supported requirements and defer all unresolved policy areas.
2. Approve additional simulated stakeholder answers for late submission, resubmission, file limits, grade publication, notifications, authentication, reporting, retention, integrations, and measurable NFR targets.
3. Approve whether assumption-supported items such as stable identifiers, timestamps, and authorised access may appear as reviewed assumption-labelled requirements.
4. Define or defer measurable targets for usability, security, performance, reliability, backup, recovery, capacity, and data integrity.
5. Decide whether reporting remains a high-level case capability or receives detailed report requirements through approved evidence.
6. Decide whether Skill 03 reviewed output should preserve all deferred topics as exclusions or convert any of them after new evidence is recorded.

No reviewed requirement, user story, use case, priority, validation result, or change request is approved by this raw output.

## 11. Quality Checks

| Check | Result |
|---|---|
| Based on reviewed Skill 01 and reviewed Skill 02 baselines. | Passed |
| Every requirement has a stable `FR-*` or `NFR-*` ID. | Passed |
| Every deferred topic has a stable `DR-*` ID. | Passed |
| Confirmed case facts cite `SRC-01` or `CASE-CONFIRMED` `INT-*` entries. | Passed |
| Simulated evidence remains labelled through `INT-*` IDs and status notes. | Passed |
| Assumptions keep `ASM-*` labels and are not converted into confirmed facts. | Passed |
| Open questions keep `OQ-*` or `OQ-DRAFT-*` IDs. | Passed |
| Partial and unanswered items remain visibly incomplete. | Passed |
| No policy is invented for late submissions, resubmissions, file limits, grade publication, notifications, authentication, reporting access, retention, integrations, or measurable NFR targets. | Passed |
| No user stories, use cases, priorities, validation results, or change requests are included. | Passed |
| Student decisions needed before review are listed. | Passed |
