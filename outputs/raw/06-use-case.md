# Skill 05 Raw Output: Use-Case View

## 1. Review Status and Boundary

| Field | Value |
|---|---|
| Output type | First AI raw output for Skill 05 use-case view |
| Created for review by | Gerungan Dave Jordy |
| Creation date | 23 June 2026 |
| Baseline used | Reviewed Skill 01 through Skill 04 outputs |
| Boundary | This is a high-level use-case view for validation support only. It is not a final use-case specification, final diagram, implementation design, or reviewed output. |

This raw output derives use-case candidates only from reviewed `FR-*` requirements and reviewed `US-*` user stories. It does not add new requirement scope, new acceptance criteria, detailed policies, measurable NFR targets, final traceability, or final diagrams.

## 2. Inputs and Evidence Sources

| Source | Use in this output |
|---|---|
| `outputs/reviewed/01-inception.md` | Reviewed stakeholders, objectives, assumptions, and open questions. |
| `outputs/reviewed/02-elicitation.md` | Reviewed open-question status, answer classification, and decision gaps. |
| `outputs/reviewed/03-requirements.md` | Authoritative source for `FR-*`, `NFR-*`, `DR-*`, and `CON-SPEC-*` items. |
| `outputs/reviewed/04-user-stories.md` | Authoritative source for `US-*` items and story readiness. |
| `outputs/reviewed/05-prioritization.md` | Reviewed priority and readiness-risk baseline. |
| `evaluation/ai-output-review.md` | Review record and evidence-discipline corrections from earlier skills. |

## 3. Use-Case Derivation Rules

| Rule | Application |
|---|---|
| Derive only from reviewed baseline items. | Every use-case candidate maps to reviewed `FR-*` and `US-*` items. |
| Keep actors evidence-backed. | Actors are lecturer, student, administrator, or lecturer/administrator where reviewed evidence supports the capability. |
| Keep steps high level. | Main success scenarios avoid unapproved fields, status values, file policies, authentication workflows, report layouts, and NFR targets. |
| Preserve open boundaries. | `OQ-*`, `OQ-DRAFT-*`, `DR-*`, and `ASM-*` references are listed as blockers or open extensions. |
| Do not convert partial items into fully specified flows. | Partial use cases retain a partial validation note. |

## 4. Use-Case Candidates

| Use-case ID | Use-case name | Primary actor | Source items | Goal | Main success scenario | Validation note |
|---|---|---|---|---|---|---|
| `UC-01` | Create assignment | Lecturer | `FR-01`; `US-01`; `OBJ-01` | Define coursework tasks for students. | Lecturer starts assignment creation, provides assignment information at a high level, and the system records the assignment. | Ready at high level only; mandatory fields and validation remain open. |
| `UC-02` | Define assignment deadline | Lecturer | `FR-02`; `US-02`; `OBJ-01` | Set when coursework submissions are due. | Lecturer selects an assignment, defines a deadline at a high level, and the system associates the deadline with the assignment. | Ready at high level only; timezone, cutoff, deadline-change, and late-submission behavior remain open. |
| `UC-03` | View assignment information | Student | `FR-03`; `US-03`; `OBJ-02` | Understand coursework tasks before submitting work. | Student accesses available assignment information and reviews the assignment details provided by the system. | Ready at high level only; exact displayed fields remain open. |
| `UC-04` | Submit assignment file | Student | `FR-04`; `US-04`; `OBJ-02` | Provide coursework work through the system. | Student selects an assignment, provides a file for submission, and the system records the submission at a high level. | Ready at high level with high detail risk; file and submission policies remain open. |
| `UC-05` | Monitor assignment status and deadline | Student | `FR-05`; `US-05`; `OBJ-04` | Understand assignment progress and deadline position. | Student views assignment status and deadline information made available by the system. | Partial; status values, confirmation details, update rules, and deadline interpretation remain open. |
| `UC-06` | Record grade | Lecturer | `FR-06`; `US-06`; `OBJ-03` | Capture assessed coursework results. | Lecturer selects a student submission and records a grade at a high level. | Partial; publication, correction, visibility, and history rules remain open. |
| `UC-07` | Provide feedback | Lecturer | `FR-07`; `US-07`; `OBJ-03` | Provide assessment comments for a student submission. | Lecturer selects a student submission and records feedback at a high level. | Partial; feedback visibility, publication, correction, and history remain open. |
| `UC-08` | Manage users | Administrator | `FR-08`; `US-08`; `OBJ-05` | Support lecturer, student, and administrator participation. | Administrator manages user information at a high level. | Ready at high level with assumption-labelled role boundary; authentication and role assignment remain open. |
| `UC-09` | Manage courses | Administrator | `FR-09`; `US-09`; `OBJ-05` | Organise assignment activity around coursework context. | Administrator manages course information at a high level. | Ready at high level; course data, enrolment rules, and integration boundary remain open. |
| `UC-10` | Manage system configuration | Administrator | `FR-10`; `US-10`; `OBJ-05` | Control assignment-related system settings. | Administrator manages system configuration at a high level. | Ready at high level; configuration items and governance remain open. |
| `UC-11` | Access assignment-related reporting | Lecturer or administrator | `FR-11`; `US-11` | Review assignment activity at a high level. | Lecturer or administrator accesses assignment-related reporting support at a high level. | Partial; report types, fields, filters, recipients, and access rights remain open. |

## 5. Open Extensions and Blockers

| Use-case area | Open extensions or blockers |
|---|---|
| Assignment creation and deadline definition | `OQ-01`, `OQ-02`, `OQ-12`, `DR-01`, `DR-02`, and `DR-03` block detailed field validation, cutoff rules, and late-submission alternatives. |
| Submission | `OQ-02`, `OQ-03`, `OQ-04`, `OQ-DRAFT-03`, and `DR-03` through `DR-07` block detailed late submission, resubmission, file policy, failure handling, and receipt-proof flows. |
| Status monitoring | `OQ-12`, `OQ-DRAFT-01`, `OQ-DRAFT-03`, `DR-02`, `DR-07`, and `DR-08` block exact status labels and update rules. |
| Grading and feedback | `OQ-06` and `DR-10` block publication, correction, visibility, and history flows. |
| Administration | `OQ-08`, `OQ-10`, `OQ-11`, `OQ-DRAFT-02`, `ASM-03`, `DR-12` through `DR-15`, `DR-17`, and `DR-18` block authentication, role assignment, retention, integration, and managed-data detail. |
| Reporting | `OQ-07`, `ASM-01`, `ASM-06`, and `DR-11` block report contents and access rights. |
| Quality concerns | `OQ-09`, `ASM-02`, and `DR-16` block measurable validation for usability, security, performance, reliability, backup, recovery, capacity, and data integrity. |

## 6. Traceability to Requirements and User Stories

| Use case | Functional requirement | User story | Priority baseline |
|---|---|---|---|
| `UC-01` | `FR-01` | `US-01` | `Must`; high value; medium readiness risk |
| `UC-02` | `FR-02` | `US-02` | `Must`; high value; high readiness risk |
| `UC-03` | `FR-03` | `US-03` | `Must`; high value; medium readiness risk |
| `UC-04` | `FR-04` | `US-04` | `Must`; high value; high readiness risk |
| `UC-05` | `FR-05` | `US-05` | `Must`; high value; high readiness risk |
| `UC-06` | `FR-06` | `US-06` | `Must`; high value; high readiness risk |
| `UC-07` | `FR-07` | `US-07` | `Must`; high value; high readiness risk |
| `UC-08` | `FR-08` | `US-08` | `Must`; high value; high readiness risk |
| `UC-09` | `FR-09` | `US-09` | `Must`; high value; medium readiness risk |
| `UC-10` | `FR-10` | `US-10` | `Must`; high value; high readiness risk |
| `UC-11` | `FR-11` | `US-11` | `Should`; medium value; high readiness risk |

## 7. Student Decisions Needed

Before these use cases can become detailed reviewed use-case specifications, the student must decide whether to keep unresolved topics deferred or approve evidence for:

1. assignment fields, deadline timezone, cutoff, deadline-change, and late-submission rules;
2. resubmission, file limits, upload failure handling, submission receipt evidence, and status values;
3. grade and feedback publication, correction, visibility, and history;
4. reporting contents and access rights;
5. authentication, role assignment, audit, retention, system configuration governance, and integrations;
6. measurable NFR targets for usability, security, performance, reliability, backup, recovery, capacity, and data integrity.

## 8. Quality Checks

| Check | Result |
|---|---|
| Based on reviewed Skill 01 through Skill 04 baselines. | Passed |
| Use cases derive only from reviewed `FR-*` and `US-*` items. | Passed |
| No new requirement ID is created. | Passed |
| Deferred topics remain blockers, not approved use-case behavior. | Passed |
| Partial and assumption-labelled boundaries remain visible. | Passed |
| No final traceability matrix or final diagram is produced. | Passed |
| No policy was invented for late submission, resubmission, file limits, grade publication, notifications, authentication, reporting detail, retention, integrations, or measurable NFR targets. | Passed |
