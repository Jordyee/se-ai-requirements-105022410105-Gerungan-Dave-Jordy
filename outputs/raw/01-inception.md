# Skill 01 Raw Output: Project Inception and Stakeholder Discovery

## 1. Evidence Summary

This raw output is the first AI-generated inception draft. It is not yet a reviewed requirements baseline.

| Source | Evidence type | Use in this draft |
|---|---|---|
| `SRC-01` | Assignment case brief and case baseline | Primary source for confirmed project facts, actors, capabilities, quality concerns, and assignment constraints. |
| `SRC-02` | Simulated interview record | Used only with simulation labels. `CASE-CONFIRMED` answers can support case facts; `PARTIALLY ANSWERED` and `UNANSWERED` entries remain incomplete. |
| `SRC-03` | Assumption register | Used only as labelled assumptions. Accepted assumptions are working assumptions, not confirmed stakeholder facts. |

Confirmed by the case (`SRC-01`):

- The project is a Student Task Management System for coursework assignment management.
- Lecturers create assignments, set deadlines, grade submissions, and provide feedback.
- Students view assignments, submit files, and monitor assignment status and deadlines.
- Administrators manage users, courses, and system configuration.
- The system must consider usability, security, performance, reliability, and data integrity.
- Requirements artefacts must remain traceable, and unsupported information must remain labelled.

Simulated interview evidence (`SRC-02`):

- `INT-L-01`, `INT-S-01`, and `INT-A-01` restate case-confirmed stakeholder activities.
- `INT-A-06` confirms that usability, security, performance, reliability, and data integrity must be considered.
- `INT-L-05`, `INT-L-06`, `INT-S-02`, and `INT-S-06` are only partially answered.
- Remaining interview questions about policy, authentication, integrations, files, audit, notifications, and failure handling are unanswered.

Assumptions (`SRC-03`):

- `ASM-01` and `ASM-02` add secondary stakeholders as working assumptions.
- `ASM-03` states that the system distinguishes at least lecturer, student, and administrator roles, but account-role behaviour remains unconfirmed.
- `ASM-04`, `ASM-05`, and `ASM-06` support traceability, timestamps, and authorised access as accepted working assumptions.
- `ASM-07` sets an accepted working scope boundary for features not stated in the case.
- `ASM-08` keeps requirements engineering independent from a specific implementation technology.

## 2. Problem Statement

The university needs a consistent way for lecturers, students, and administrators to manage coursework assignment information and activities. The case confirms the need to support assignment creation, deadline management, file submission, grading, feedback, status monitoring, user and course administration, system configuration, and reporting (`SRC-01`; `INT-L-01`; `INT-S-01`; `INT-A-01`).

Without a defined system and traceable requirements, assignment information, submission status, deadlines, grading, feedback, and reporting may be handled inconsistently across stakeholder groups (`SRC-01`). This draft does not prescribe implementation technology, hosting, integrations, or platform choices because those are not provided by the case (`SRC-01`; `ASM-08`).

## 3. Initial Business Objectives

| ID | Objective | Evidence | Status |
|---|---|---|---|
| OBJ-01 | Enable lecturers to create assignments and define deadlines. | `SRC-01`; `INT-L-01` | Confirmed by case |
| OBJ-02 | Enable students to view assignments and submit files. | `SRC-01`; `INT-S-01` | Confirmed by case |
| OBJ-03 | Enable lecturers to record grades and feedback. | `SRC-01`; `INT-L-01` | Confirmed by case |
| OBJ-04 | Enable students to monitor assignment status and deadlines. | `SRC-01`; `INT-S-01` | Confirmed by case |
| OBJ-05 | Enable administrators to manage users, courses, and system configuration. | `SRC-01`; `INT-A-01` | Confirmed by case |
| OBJ-06 | Consider usability, security, performance, reliability, and data integrity. | `SRC-01`; `INT-A-06` | Confirmed at quality-area level; measurable targets remain open |
| OBJ-07 | Maintain traceability from stakeholder evidence to requirements artefacts. | `SRC-01`; README evidence policy | Assignment constraint |

## 4. Stakeholder Discovery

| ID | Stakeholder | Status | Evidence | Initial interest | Uncertainty |
|---|---|---|---|---|---|
| STK-01 | Lecturer | Confirmed case stakeholder | `SRC-01`; `INT-L-01` | Efficiently create assignments, set deadlines, identify submissions, grade work, provide feedback, and access reporting. | Mandatory assignment fields, late-submission rules, resubmission rules, grade publication rules, and report details are not defined. |
| STK-02 | Student | Confirmed case stakeholder | `SRC-01`; `INT-S-01` | View applicable assignments, understand deadlines, submit files reliably, and monitor status. | Confirmation details, file type and size limits, upload failure handling, notifications, and grade/feedback history are not defined. |
| STK-03 | Administrator | Confirmed case stakeholder | `SRC-01`; `INT-A-01` | Manage users, courses, and system configuration in a controlled way. | Authentication, role assignment, audit, retention, and integrations are not defined. |
| STK-04 | University or academic management | Inferred secondary stakeholder; assumption | `ASM-01`; `SRC-03` | Possible oversight, academic-policy compliance, and reporting interest. | No direct stakeholder statement is available; must remain an assumption until validated. |
| STK-05 | IT support or system operator | Inferred secondary stakeholder; assumption | `ASM-02`; `SRC-03` | Possible interest in availability, security, backup, recovery, monitoring, and supportability. | No direct stakeholder statement is available; must remain an assumption until validated. |

## 5. Preliminary Scope

### In scope by case evidence

The following topics are supported by the case and may be analysed further in later skills:

- Lecturer assignment creation (`SRC-01`; `INT-L-01`).
- Assignment deadline definition (`SRC-01`; `INT-L-01`).
- Student access to assignment information (`SRC-01`; `INT-S-01`).
- Student file submission (`SRC-01`; `INT-S-01`).
- Submission status and deadline monitoring (`SRC-01`; `INT-S-01`).
- Lecturer grading and feedback (`SRC-01`; `INT-L-01`).
- Administrator management of users, courses, and system configuration (`SRC-01`; `INT-A-01`).
- Assignment-related reporting at a high level (`SRC-01`; `INT-L-06` partially answered).
- Consideration of usability, security, performance, reliability, and data integrity (`SRC-01`; `INT-A-06`).

### Out of scope until approved

The following items are not stated in the case and should not become requirements without later evidence or an approved assumption:

- Real-time chat or video conferencing (`ASM-07`).
- Plagiarism detection (`ASM-07`).
- Tuition payment or other financial processing (`ASM-07`).
- Student attendance management (`ASM-07`).
- Course-content streaming or learning-material authoring (`SRC-01`; no supporting evidence).
- External learning management, identity, email, or cloud-storage integrations (`INT-A-04` unanswered).
- Native mobile applications (`SRC-01`; no supporting evidence).

These items are not permanently rejected. They are outside the initial working scope unless later elicitation or change management adds evidence.

## 6. Constraints

| ID | Constraint | Evidence | Status |
|---|---|---|---|
| CON-01 | The project must use the Student Task Management System case. | `SRC-01`; README | Confirmed assignment constraint |
| CON-02 | Raw AI output must be preserved separately from reviewed output. | README evidence policy | Confirmed assignment constraint |
| CON-03 | Reviewed requirements remain the student's responsibility. | README; `SRC-01` | Confirmed assignment constraint |
| CON-04 | Case facts, simulated answers, assumptions, and open questions must remain distinguishable. | README; `SRC-01`; `SRC-02`; `SRC-03` | Confirmed assignment constraint |
| CON-05 | No unsupported feature may enter the reviewed baseline without evidence or an approved assumption. | README; `SRC-03` | Confirmed assignment constraint |
| CON-06 | Implementation technology, budget, schedule, hosting environment, and integrations are not provided. | `SRC-01`; `ASM-08` | Known information gap / working rule |
| CON-07 | The system distinguishes at least lecturer, student, and administrator roles, but multi-role account behaviour is not confirmed. | `ASM-03` | Working assumption, not confirmed fact |

## 7. Quality Concerns

The case confirms that the system must consider the following quality areas (`SRC-01`; `INT-A-06`). This inception draft does not assign numeric targets because no approved values are available.

| Quality area | Confirmed concern | Open measurement question |
|---|---|---|
| Usability | Users must be able to carry out assignment-related workflows. | What usability criteria or task-completion expectations should be used? |
| Security | Academic data and role-based operations need protection. | What authentication, authorisation, and audit policies apply? |
| Performance | System responsiveness must be considered. | What response-time and capacity targets apply? |
| Reliability | Assignment submission and records should be dependable. | What availability, backup, and recovery targets apply? |
| Data integrity | Assignment, submission, grade, feedback, and deadline data must remain consistent. | What validation, timestamp, identifier, versioning, and correction rules apply? |

Working assumptions related to quality:

- `ASM-04` assumes assignment and submission records require stable identifiers.
- `ASM-05` assumes the system records timestamps for deadlines and submissions.
- `ASM-06` assumes only authorised users may view or modify grades and submissions.

These assumptions remain labelled and require appropriate validation before becoming final requirements.

## 8. Risks and Stakeholder Tensions

The following are investigation topics, not confirmed conflicts:

| ID | Risk or tension | Evidence | Why it matters |
|---|---|---|---|
| RISK-01 | Late-submission policy is unknown. | `INT-L-03` unanswered; `OQ-02` | Affects submission rules, status labels, grading workflow, and fairness. |
| RISK-02 | Resubmission and version-history policy is unknown. | `INT-L-04` unanswered; `OQ-03` | Affects data integrity, auditability, and student workflow. |
| RISK-03 | File type, size, and upload failure rules are unknown. | `INT-S-03` unanswered; `INT-S-04` unanswered; `OQ-04` | Affects usability, storage, security, and reliability. |
| RISK-04 | Grade and feedback publication rules are incomplete. | `INT-L-05` partially answered; `INT-S-06` partially answered; `OQ-06` | Affects student visibility, lecturer corrections, and academic record control. |
| RISK-05 | Reporting is mentioned but not defined. | `SRC-01`; `INT-L-06` partially answered; `OQ-07` | Affects stakeholder expectations and access rights. |
| RISK-06 | Authentication, role assignment, audit, and retention are unknown. | `INT-A-02`, `INT-A-03`, `INT-A-05` unanswered; `OQ-08`, `OQ-10` | Affects security, privacy, accountability, and administration. |
| RISK-07 | Integration decisions are unknown. | `INT-A-04` unanswered; `OQ-11` | Affects scope, data flow, technical constraints, and project complexity. |
| RISK-08 | Measurable NFR targets are unknown. | `OQ-09`; `SRC-01` quality areas only | Affects later validation and acceptance criteria. |

Potential stakeholder tensions to investigate later:

- Students may prefer flexible resubmission, while lecturers may require controlled final submissions.
- Lecturers may prefer flexible grade correction, while academic management may require an audit trail.
- Users may prefer convenience, while administrators and IT support may require stronger security controls.
- Reporting needs may conflict with privacy and least-privilege access.

## 9. Open Questions for Elicitation

Existing open questions from the case baseline:

| ID | Question | Intended stakeholder | Why it matters |
|---|---|---|---|
| OQ-01 | What assignment fields are mandatory when a lecturer creates an assignment? | Lecturer | Defines creation rules and validation. |
| OQ-02 | Are late submissions blocked, accepted with a marker, or controlled per assignment? | Lecturer / academic management | Affects submission business rules. |
| OQ-03 | May students replace a submitted file before the deadline, and must version history be retained? | Lecturer / student | Affects data integrity and auditability. |
| OQ-04 | Which file types and maximum file sizes are allowed? | Lecturer / IT support | Affects validation, storage, and security. |
| OQ-05 | Which events require notifications, and through which channels? | Lecturer / student | Prevents unsupported notification features. |
| OQ-06 | Can grades or feedback be changed after publication? | Lecturer / academic management | Defines authorization and audit rules. |
| OQ-07 | What reports are required and who may access them? | Lecturer / administrator / management | The assignment mentions reporting but not its contents. |
| OQ-08 | How are users authenticated and roles assigned? | Administrator / IT support | Required for access-control requirements. |
| OQ-09 | What response-time, availability, backup, and recovery targets apply? | IT support / management | Required for measurable NFRs. |
| OQ-10 | What personal or academic data retention rules apply? | Administrator / management | Affects privacy and data lifecycle. |
| OQ-11 | Is the system standalone or integrated with an existing campus system? | Administrator / IT support | Affects scope and interfaces. |
| OQ-12 | Which timezone and deadline cut-off rules apply? | Lecturer / administrator | Prevents deadline ambiguity. |

Additional draft open questions identified during inception:

| ID | Question | Intended stakeholder | Why it matters |
|---|---|---|---|
| OQ-DRAFT-01 | What exact submission-status values should be displayed to students and lecturers? | Lecturer / student | The case confirms status monitoring but not the status model. |
| OQ-DRAFT-02 | Who is allowed to configure system-wide assignment policies? | Administrator / academic management | The case mentions system configuration but not governance. |
| OQ-DRAFT-03 | What evidence should be stored to prove that a submission was received? | Lecturer / student / IT support | Supports dispute handling and data integrity. |

## 10. Student Decisions Needed

The student should review and decide the following before later specification:

1. Whether the later baseline will use only case-confirmed facts or also approve simulated stakeholder policies.
2. Which unresolved policy areas may become approved assumptions: late submission, resubmission, file limits, grade publication, notifications, authentication, reporting, retention, integrations, and NFR targets.
3. Whether `OQ-DRAFT-01`, `OQ-DRAFT-02`, and `OQ-DRAFT-03` should be retained, revised, or removed.
4. Whether `ASM-01` and `ASM-02` are sufficient as secondary stakeholders for the assignment, or whether additional stakeholders must be added.
5. When this raw output is reviewed, which corrections should be recorded in `evaluation/ai-output-review.md` before creating `outputs/reviewed/01-inception.md`.

No policy decisions are made in this raw output.

## 11. Traceability Notes

- Case-confirmed facts are traced to `SRC-01` and, where available, `CASE-CONFIRMED` simulated answers such as `INT-L-01`, `INT-S-01`, `INT-A-01`, and `INT-A-06`.
- Simulated interview entries from `SRC-02` are used only according to their status labels.
- Assumptions from `SRC-03` remain labelled with `ASM-*` IDs and are not converted into confirmed facts.
- Open questions from `CASE.md` retain their `OQ-*` identifiers.
- New questions added by this draft use `OQ-DRAFT-*` identifiers until the student reviews them.
- This output does not define final functional requirements, user stories, use cases, priorities, validation results, or change requests.
