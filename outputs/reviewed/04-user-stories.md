# 04 User Stories: Reviewed Baseline

## Review Status

| Field | Value |
|---|---|
| Raw source | `outputs/raw/04-user-stories.md` |
| Reviewed by | Gerungan Dave Jordy |
| Review date | 23 June 2026 |
| Review outcome | Accepted with simplification and structure revisions |
| Important boundary | This reviewed output derives user stories only from reviewed Skill 03 requirements. It is not a use case, validation, implementation, or change request artefact. |

This reviewed version keeps the raw output's evidence discipline but simplifies the presentation. Product-facing user stories are limited to functional requirements. NFR and assignment-artefact items are preserved as supporting considerations instead of being treated as product user stories.

## 1. Inputs and Evidence Sources

| Source | Use in this reviewed output |
|---|---|
| `outputs/raw/04-user-stories.md` | First AI output reviewed for this stage. |
| `outputs/reviewed/01-inception.md` | Reviewed stakeholders, objectives, open questions, risks, and constraints. |
| `outputs/reviewed/02-elicitation.md` | Reviewed elicitation status and unresolved decision log. |
| `outputs/reviewed/03-requirements.md` | Authoritative source for `FR-*`, `NFR-*`, `DR-*`, and `CON-SPEC-*` items. |
| `evaluation/ai-output-review.md` | Review record and corrections. |

## 2. Review Revisions from Raw Output

| Raw output issue or improvement area | Reviewed revision |
|---|---|
| Raw output included NFR-derived items as user stories. | Kept NFRs as quality considerations because they are partial and not yet measurable. |
| Raw output repeated long deferred-topic details in several sections. | Condensed deferred references while preserving `OQ-*`, `OQ-DRAFT-*`, and `DR-*` traceability. |
| Raw story table was comprehensive but heavy. | Kept the core story list focused on functional requirements `FR-01` through `FR-11`. |
| Raw output had an assignment artefact story for traceability. | Moved traceability into artefact considerations, not the product story list. |

No new requirement, policy, acceptance criterion, use case, validation result, or change request is added in this reviewed version.

## 3. Story Derivation Rules

| Rule | Reviewed application |
|---|---|
| Derive only from reviewed Skill 03. | Every story maps to an existing `FR-*` item. |
| Preserve evidence labels. | Each story keeps `SRC-*`, `INT-*`, `ASM-*`, `OQ-*`, `OQ-DRAFT-*`, and `DR-*` references where relevant. |
| Keep partial status visible. | Stories based on partial requirements retain open issue notes. |
| Do not invent acceptance criteria. | No acceptance criteria are written because policy and measurable targets remain open. |
| Keep deferred topics deferred. | `DR-*` topics are referenced as blockers, not converted into story content. |

## 4. Reviewed Product User Stories

| Story ID | User story | Source requirement | Evidence | Readiness | Open boundary |
|---|---|---|---|---|---|
| US-01 | As a lecturer, I want to create assignments, so that coursework tasks can be defined for students. | `FR-01` | `SRC-01`; `INT-L-01` | Ready at high level | Mandatory fields and validation remain open under `OQ-01` and `DR-01`. |
| US-02 | As a lecturer, I want to define assignment deadlines, so that students know when coursework submissions are due. | `FR-02` | `SRC-01`; `INT-L-01` | Ready at high level | Timezone, cutoff, deadline-change, and late-submission rules remain open under `OQ-02`, `OQ-12`, `DR-02`, and `DR-03`. |
| US-03 | As a student, I want to view assignment information, so that I can understand coursework tasks before submitting work. | `FR-03` | `SRC-01`; `INT-S-01` | Ready at high level | Exact assignment fields and display expectations remain open under `OQ-01` and `DR-01`. |
| US-04 | As a student, I want to submit files for assignments, so that I can provide coursework work through the system. | `FR-04` | `SRC-01`; `INT-S-01` | Ready at high level with high detail risk | File policy, late submission, resubmission, upload failure handling, and receipt proof remain open under `OQ-02`, `OQ-03`, `OQ-04`, `OQ-DRAFT-03`, and `DR-03` through `DR-07`. |
| US-05 | As a student, I want to monitor assignment status and deadlines, so that I can understand my coursework progress. | `FR-05` | `SRC-01`; `INT-S-01`; `INT-S-02` | Partial | Status values, confirmation details, update rules, timezone, and receipt evidence remain open under `OQ-12`, `OQ-DRAFT-01`, `OQ-DRAFT-03`, `DR-02`, `DR-07`, and `DR-08`. |
| US-06 | As a lecturer, I want to record grades for student submissions, so that assessed coursework results can be captured. | `FR-06` | `SRC-01`; `INT-L-01`; `INT-L-05` | Partial | Publication timing, correction rules, visibility, and history remain open under `OQ-06` and `DR-10`. |
| US-07 | As a lecturer, I want to provide feedback for student submissions, so that students can receive assessment comments. | `FR-07` | `SRC-01`; `INT-L-01`; `INT-L-05` | Partial | Feedback publication, visibility, history, and correction rules remain open under `OQ-06` and `DR-10`. |
| US-08 | As an administrator, I want to manage users, so that lecturer, student, and administrator participation can be supported. | `FR-08` | `SRC-01`; `INT-A-01` | Ready at high level with assumption-labelled role boundary | Authentication, role assignment, managed user fields, and multi-role behavior remain open under `OQ-08`, `ASM-03`, `DR-12`, and `DR-13`. |
| US-09 | As an administrator, I want to manage courses, so that assignment activity can be organised around coursework context. | `FR-09` | `SRC-01`; `INT-A-01` | Ready at high level | Required course data, enrolment rules, and integration boundary remain open under `OQ-11`, `DR-17`, and `DR-18`. |
| US-10 | As an administrator, I want to manage system configuration, so that assignment-related system settings can be controlled. | `FR-10` | `SRC-01`; `INT-A-01` | Ready at high level | Configuration items, policy authority, and governance remain open under `OQ-DRAFT-02`, `DR-14`, and `DR-18`. |
| US-11 | As a lecturer or administrator, I want assignment-related reporting support, so that assignment activity can be reviewed at a high level. | `FR-11` | `SRC-01`; `INT-L-06` | Partial | Report types, contents, filters, recipients, and access rights remain open under `OQ-07` and `DR-11`. |

## 5. Quality and Artefact Considerations

These items are important for prioritisation and later validation, but they are not reviewed as product user stories because they are partial quality concerns or assignment artefact constraints.

| Item | Reviewed handling | Reason |
|---|---|---|
| `NFR-01` Usability | Keep as quality consideration. | Criteria and task-completion expectations remain open under `OQ-09` and `DR-16`. |
| `NFR-02` Security | Keep as quality consideration with assumption label. | Authentication, authorisation, audit, role, and retention policies remain open under `OQ-08`, `OQ-10`, and related `DR-*` items. |
| `NFR-03` Performance | Keep as quality consideration. | Response-time, throughput, capacity, and load targets remain open under `OQ-09` and `DR-16`. |
| `NFR-04` Reliability | Keep as quality consideration with assumption-linked operational risk. | Availability, backup, recovery, upload failure handling, and incident response remain open. |
| `NFR-05` Data integrity | Keep as quality consideration with assumption labels. | Identifier, timestamp, correction, receipt, and retention rules remain open. |
| `CON-SPEC-01` to `CON-SPEC-04` | Keep as assignment artefact constraints. | These guide evidence handling and requirements discipline, not product user behavior. |

## 6. Deferred Topics Kept Out of Stories

The following deferred topics remain blocked and must not be converted into story details or acceptance criteria without approved evidence:

| Deferred area | Related IDs |
|---|---|
| Assignment fields, validation, deadline time rules, late submission, and resubmission. | `DR-01` to `DR-04`; `OQ-01`; `OQ-02`; `OQ-03`; `OQ-12` |
| File policy, upload failure handling, submission receipt proof, and status values. | `DR-05` to `DR-08`; `OQ-04`; `OQ-DRAFT-01`; `OQ-DRAFT-03` |
| Notifications. | `DR-09`; `OQ-05` |
| Grade and feedback publication, correction, visibility, and history. | `DR-10`; `OQ-06` |
| Reporting detail and access rights. | `DR-11`; `OQ-07` |
| Authentication, role assignment, audit, retention, and configuration governance. | `DR-12` to `DR-15`; `OQ-08`; `OQ-10`; `OQ-DRAFT-02`; `ASM-03`; `ASM-06` |
| Measurable NFR targets, integration boundary, and administrator-managed data detail. | `DR-16` to `DR-18`; `OQ-09`; `OQ-11`; `ASM-02`; `ASM-08` |

## 7. Traceability Summary

| Story | Source requirement | Objective or stakeholder |
|---|---|---|
| US-01 | `FR-01` | Lecturer; `OBJ-01` |
| US-02 | `FR-02` | Lecturer; `OBJ-01` |
| US-03 | `FR-03` | Student; `OBJ-02` |
| US-04 | `FR-04` | Student; `OBJ-02` |
| US-05 | `FR-05` | Student; `OBJ-04` |
| US-06 | `FR-06` | Lecturer; `OBJ-03` |
| US-07 | `FR-07` | Lecturer; `OBJ-03` |
| US-08 | `FR-08` | Administrator; `OBJ-05` |
| US-09 | `FR-09` | Administrator; `OBJ-05` |
| US-10 | `FR-10` | Administrator; `OBJ-05` |
| US-11 | `FR-11` | Lecturer / administrator / assumed management |

## 8. Quality Checks

| Check | Result |
|---|---|
| Raw Skill 04 user-story output was preserved separately. | Passed |
| Reviewed stories derive only from reviewed Skill 03 `FR-*` items. | Passed |
| NFR and constraint items were not misrepresented as product user stories. | Passed |
| Partial and assumption-labelled boundaries remain visible. | Passed |
| Deferred topics remain deferred and traceable. | Passed |
| No acceptance criteria, use cases, validation results, change requests, implementation tasks, or new requirements are included. | Passed |
| No policy was invented for late submission, resubmission, file limits, grade publication, notifications, authentication, reporting detail, retention, integrations, or measurable NFR targets. | Passed |
