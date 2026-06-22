# 02 Elicitation: Reviewed Baseline

## Review Status

- **Raw source:** `outputs/raw/02-elicitation.md`
- **Reviewed by:** Gerungan Dave Jordy
- **Review date:** 23 June 2026
- **Review outcome:** Accepted with minor clarification and status updates.
- **Important boundary:** This document is an elicitation baseline, not a final requirements specification.

No new stakeholder policy, measurable non-functional target, integration decision, or scope expansion is approved in this reviewed output. Open questions remain open until answered by real stakeholder evidence, approved simulation, or explicit student decision.

## 1. Inputs and Evidence Sources

| Source | Role in this elicitation baseline | Review decision |
|---|---|---|
| `SRC-01` | Assignment case brief and case baseline in `CASE.md`. | Use as confirmed case evidence only where the case states the fact. |
| `SRC-02` | Simulated interview record in `inputs/interview-answers.md`. | Use only with simulation labels and response status. |
| `SRC-03` | Assumption register in `inputs/assumptions.md`. | Use only as labelled assumptions with `ASM-*` IDs. |
| `outputs/reviewed/01-inception.md` | Reviewed inception baseline. | Use as the starting point for stakeholders, open questions, risks, and student decisions. |
| `evaluation/ai-output-review.md` | Review record for raw AI outputs. | Use to track corrections and review rationale. |

Skill 01 retained `OQ-DRAFT-01`, `OQ-DRAFT-02`, and `OQ-DRAFT-03` for elicitation. This reviewed Skill 02 baseline keeps them open.

## 2. Elicitation Objectives

| ID | Objective | Evidence basis | Status |
|---|---|---|---|
| ELO-01 | Clarify lecturer workflow details for creating assignments, setting deadlines, receiving submissions, grading, feedback, and reporting. | `SRC-01`; `INT-L-01`; `OQ-01`; `OQ-02`; `OQ-03`; `OQ-06`; `OQ-07` | Needs stakeholder answers |
| ELO-02 | Clarify student workflow expectations for viewing assignments, submitting files, receiving confirmation, monitoring status, and seeing feedback. | `SRC-01`; `INT-S-01`; `OQ-03`; `OQ-04`; `OQ-05`; `OQ-DRAFT-01`; `OQ-DRAFT-03` | Needs stakeholder answers |
| ELO-03 | Clarify administrator responsibilities for users, roles, courses, configuration, authentication, audit, retention, and integrations. | `SRC-01`; `INT-A-01`; `OQ-08`; `OQ-10`; `OQ-11`; `OQ-DRAFT-02` | Needs stakeholder answers |
| ELO-04 | Clarify assumed secondary stakeholder concerns without treating them as confirmed direct stakeholder facts. | `ASM-01`; `ASM-02`; `OQ-07`; `OQ-09`; `OQ-10`; `OQ-11` | Requires validation or student approval |
| ELO-05 | Identify which unanswered or partially answered items block later requirements specification. | `SRC-02`; reviewed Skill 01 baseline | Ongoing |

## 3. Stakeholder Coverage Map

| Stakeholder | Status | Elicitation focus | Evidence link |
|---|---|---|---|
| Lecturer | Confirmed case stakeholder | Assignment fields, deadline rules, late submissions, resubmissions, grade and feedback publication, grade correction, reporting, and submission dispute evidence. | `SRC-01`; `INT-L-01`; `INT-L-02`; `INT-L-03`; `INT-L-04`; `INT-L-05`; `INT-L-06`; `OQ-01`; `OQ-02`; `OQ-03`; `OQ-06`; `OQ-07`; `OQ-12`; `OQ-DRAFT-03` |
| Student | Confirmed case stakeholder | Assignment visibility, submission confirmation, file restrictions, upload failure handling, notification expectations, status labels, and grade or feedback visibility. | `SRC-01`; `INT-S-01`; `INT-S-02`; `INT-S-03`; `INT-S-04`; `INT-S-05`; `INT-S-06`; `OQ-03`; `OQ-04`; `OQ-05`; `OQ-DRAFT-01`; `OQ-DRAFT-03` |
| Administrator | Confirmed case stakeholder | User management, course management, system configuration, authentication, role assignment, audit, retention, integration, and configuration governance. | `SRC-01`; `INT-A-01`; `INT-A-02`; `INT-A-03`; `INT-A-04`; `INT-A-05`; `INT-A-06`; `OQ-08`; `OQ-10`; `OQ-11`; `OQ-DRAFT-02` |
| University or academic management | Assumed secondary stakeholder | Academic policy approval, reporting needs, grade correction governance, retention policy, and oversight needs. | `ASM-01`; `OQ-02`; `OQ-06`; `OQ-07`; `OQ-10`; `OQ-DRAFT-02` |
| IT support or system operator | Assumed secondary stakeholder | Security, performance, availability, backup, recovery, file handling constraints, monitoring, and integration constraints. | `ASM-02`; `OQ-04`; `OQ-08`; `OQ-09`; `OQ-10`; `OQ-11` |

## 4. Question Guide by Stakeholder

### Lecturer Questions

| Question ID | Related item | Question | Evidence goal |
|---|---|---|---|
| ELQ-L-01 | `OQ-01`; `INT-L-02` | What information must a lecturer provide when creating a new assignment? | Identify mandatory assignment data without inventing fields. |
| ELQ-L-02 | `OQ-12` | Which timezone and deadline cut-off rule should apply when an assignment reaches its deadline? | Clarify deadline interpretation and avoid ambiguous submission status. |
| ELQ-L-03 | `OQ-02`; `INT-L-03` | How should the system treat submissions received after the deadline? | Clarify late-submission policy. |
| ELQ-L-04 | `OQ-03`; `INT-L-04` | May students replace a submitted file before the deadline, and should earlier versions be retained? | Clarify resubmission and version-history policy. |
| ELQ-L-05 | `OQ-DRAFT-01` | What submission-status values should lecturers see when reviewing student work? | Clarify the status model from the lecturer perspective. |
| ELQ-L-06 | `OQ-06`; `INT-L-05` | When should grades and feedback become visible to students, and can they be changed after publication? | Clarify publication and correction rules. |
| ELQ-L-07 | `OQ-07`; `INT-L-06` | What reports are useful to lecturers, and what information should each report contain? | Clarify reporting contents. |
| ELQ-L-08 | `OQ-DRAFT-03` | What evidence should be stored to prove that a student submission was received? | Clarify dispute-handling and submission proof needs. |

### Student Questions

| Question ID | Related item | Question | Evidence goal |
|---|---|---|---|
| ELQ-S-01 | `SRC-01`; `INT-S-01` | What information do students need to understand an assignment before submitting work? | Clarify student-facing assignment details. |
| ELQ-S-02 | `OQ-DRAFT-03`; `INT-S-02` | What confirmation should students receive after submitting a file? | Clarify submission receipt evidence. |
| ELQ-S-03 | `OQ-04`; `INT-S-03` | Which file formats and maximum file sizes do students expect or need to submit? | Gather file-handling needs without setting policy yet. |
| ELQ-S-04 | `OQ-04`; `INT-S-04` | What should happen from the student perspective if an upload fails or is interrupted? | Clarify failure handling expectations. |
| ELQ-S-05 | `OQ-05`; `INT-S-05` | Which events should notify students, and which channels are acceptable? | Clarify notification needs without assuming channels. |
| ELQ-S-06 | `OQ-DRAFT-01` | What status labels would help students understand whether their assignment is pending, submitted, late, graded, or otherwise unresolved? | Clarify student-facing status model. |
| ELQ-S-07 | `OQ-06`; `INT-S-06` | What grade and feedback history should students be able to view? | Clarify visibility and history expectations. |

### Administrator Questions

| Question ID | Related item | Question | Evidence goal |
|---|---|---|---|
| ELQ-A-01 | `SRC-01`; `INT-A-01` | What user, course, and configuration data must administrators manage? | Clarify administrative data scope. |
| ELQ-A-02 | `OQ-08`; `INT-A-02` | How should users be authenticated for the system? | Clarify authentication policy or integration needs. |
| ELQ-A-03 | `OQ-08`; `INT-A-03`; `ASM-03` | Who assigns lecturer, student, and administrator roles, and can one account hold more than one role? | Clarify role assignment and multi-role account behavior. |
| ELQ-A-04 | `OQ-DRAFT-02` | Who is allowed to configure system-wide assignment policies? | Clarify governance for system configuration. |
| ELQ-A-05 | `OQ-11`; `INT-A-04` | Is the system expected to stand alone or integrate with existing campus systems? | Clarify integration boundary. |
| ELQ-A-06 | `OQ-10`; `INT-A-05` | What audit and retention information must be stored for users, submissions, grades, feedback, and configuration changes? | Clarify accountability and data lifecycle. |
| ELQ-A-07 | `OQ-09`; `INT-A-06` | What response-time, availability, backup, and recovery expectations should be used for later measurable NFRs? | Gather measurable quality targets. |

### Academic Management Questions

| Question ID | Related item | Question | Evidence goal |
|---|---|---|---|
| ELQ-M-01 | `ASM-01`; `OQ-02` | Does academic policy define whether late submissions are blocked, accepted, marked, or decided per assignment? | Validate whether management owns late-submission policy. |
| ELQ-M-02 | `ASM-01`; `OQ-06` | What approval or audit rules apply when grades or feedback are changed after publication? | Clarify grade governance. |
| ELQ-M-03 | `ASM-01`; `OQ-07` | What summary reports, if any, does academic management need? | Validate reporting needs for the assumed stakeholder. |
| ELQ-M-04 | `ASM-01`; `OQ-10` | What academic data retention policy applies to assignment, submission, grade, and feedback records? | Clarify retention expectations. |

### IT Support or System Operator Questions

| Question ID | Related item | Question | Evidence goal |
|---|---|---|---|
| ELQ-IT-01 | `ASM-02`; `OQ-04` | Are there operational constraints on allowed file types, maximum file size, storage, or malware scanning? | Clarify technical and security constraints without adding unsupported features. |
| ELQ-IT-02 | `ASM-02`; `OQ-08` | What access-control, account-management, and monitoring policies must the system support? | Clarify operational security expectations. |
| ELQ-IT-03 | `ASM-02`; `OQ-09` | What availability, backup, recovery, and incident-response targets are expected? | Gather measurable reliability targets. |
| ELQ-IT-04 | `ASM-02`; `OQ-11` | What existing campus systems, if any, must this system exchange data with? | Clarify integration scope. |

## 5. Existing Interview Answer Classification

| Response ID | Existing status | Reviewed classification | Remaining gap |
|---|---|---|---|
| INT-L-01 | CASE-CONFIRMED | Supports lecturer activity coverage because it restates `SRC-01`. | Detailed fields, policies, and report contents remain open. |
| INT-L-02 | UNANSWERED | Not ready for specification. | Mandatory assignment fields. |
| INT-L-03 | UNANSWERED | Not ready for specification. | Late-submission policy. |
| INT-L-04 | UNANSWERED | Not ready for specification. | Resubmission and version-history policy. |
| INT-L-05 | PARTIALLY ANSWERED | Confirms grading and feedback are in scope, but does not define visibility or publication timing. | Grade publication, visibility, history, and correction rules. |
| INT-L-06 | PARTIALLY ANSWERED | Confirms reporting is mentioned, but not report types or contents. | Required reports, fields, filters, recipients, and access rights. |
| INT-S-01 | CASE-CONFIRMED | Supports student activity coverage because it restates `SRC-01`. | Confirmation, status labels, file policy, and feedback visibility remain open. |
| INT-S-02 | PARTIALLY ANSWERED | Confirms status monitoring exists, but not confirmation details. | Submission receipt content, timestamps, proof, and status update rules. |
| INT-S-03 | UNANSWERED | Not ready for specification. | File formats and maximum file size. |
| INT-S-04 | UNANSWERED | Not ready for specification. | Upload failure handling and recovery behavior. |
| INT-S-05 | UNANSWERED | Not ready for specification. | Notification events and channels. |
| INT-S-06 | PARTIALLY ANSWERED | Confirms grades and feedback exist, but not visibility or history. | Grade and feedback history rules. |
| INT-A-01 | CASE-CONFIRMED | Supports administrator activity coverage because it restates `SRC-01`. | Exact managed data, policies, and configuration authority remain open. |
| INT-A-02 | UNANSWERED | Not ready for specification. | Authentication mechanism and policy. |
| INT-A-03 | UNANSWERED | Not ready for specification. | Role assignment and multi-role account behavior. |
| INT-A-04 | UNANSWERED | Not ready for specification. | Integration requirement or standalone boundary. |
| INT-A-05 | UNANSWERED | Not ready for specification. | Audit and retention policy. |
| INT-A-06 | CASE-CONFIRMED | Confirms quality areas at a topic level because it restates `SRC-01`. | Measurable usability, security, performance, reliability, and data-integrity targets. |

## 6. Evidence Capture Template

Use this template for any new real stakeholder answer or student-approved simulated answer. Do not add unapproved answers silently.

| Field | Required content |
|---|---|
| Answer ID | Stable ID such as `INT-L-07`, `INT-S-08`, `INT-A-09`, `INT-M-01`, or `INT-IT-01`. |
| Stakeholder | Lecturer, student, administrator, academic management, IT support, or other approved stakeholder. |
| Question ID | Related `ELQ-*` ID. |
| Source type | Real stakeholder interview, student-approved simulation, case-confirmed restatement, or assumption update. |
| Answer text | The recorded answer, kept separate from AI interpretation. |
| Status | `CASE-CONFIRMED`, `ANSWERED`, `PARTIALLY ANSWERED`, `UNANSWERED`, or `ASSUMPTION-BASED`. |
| Date | Date the answer was recorded. |
| Reviewer or approver | Student or stakeholder who approved the entry. |
| Related open questions | `OQ-*` or `OQ-DRAFT-*` IDs affected by the answer. |
| Specification readiness | Whether the answer can support Skill 03, still needs clarification, or requires student approval. |

## 7. Open Questions and Decision Log

| ID | Current status | Elicitation owner | Decision needed before specification |
|---|---|---|---|
| OQ-01 | Open | Lecturer | Mandatory assignment fields. |
| OQ-02 | Open | Lecturer / academic management | Late-submission handling. |
| OQ-03 | Open | Lecturer / student | Resubmission and version-history rules. |
| OQ-04 | Open | Lecturer / IT support | Allowed file types, file-size limits, and related security constraints. |
| OQ-05 | Open | Lecturer / student | Notification events and channels. |
| OQ-06 | Open | Lecturer / academic management | Grade publication, correction, and history rules. |
| OQ-07 | Open | Lecturer / administrator / academic management | Report contents, access rights, and recipients. |
| OQ-08 | Open | Administrator / IT support | Authentication and role assignment. |
| OQ-09 | Open | IT support / academic management | Measurable response-time, availability, backup, and recovery targets. |
| OQ-10 | Open | Administrator / academic management | Data retention rules. |
| OQ-11 | Open | Administrator / IT support | Standalone or integrated system boundary. |
| OQ-12 | Open | Lecturer / administrator | Timezone and deadline cut-off rules. |
| OQ-DRAFT-01 | Open and retained by Skill 01 review | Lecturer / student | Submission-status values for users. |
| OQ-DRAFT-02 | Open and retained by Skill 01 review | Administrator / academic management | Governance for system-wide assignment policies. |
| OQ-DRAFT-03 | Open and retained by Skill 01 review | Lecturer / student / IT support | Evidence stored to prove submission receipt. |

Review decision: keep all listed open questions unresolved until later answers or explicit student-approved assumptions exist.

## 8. Risks for Later Specification

| Risk ID | Risk | Evidence | Effect on Skill 03 |
|---|---|---|---|
| ELR-01 | Detailed assignment creation cannot be specified safely until mandatory fields are known. | `INT-L-02`; `OQ-01` | Blocks detailed validation rules for assignment creation. |
| ELR-02 | Submission behavior cannot be specified safely until late-submission, resubmission, file, failure, and timestamp rules are clarified. | `INT-L-03`; `INT-L-04`; `INT-S-03`; `INT-S-04`; `OQ-02`; `OQ-03`; `OQ-04`; `OQ-12`; `ASM-05` | Blocks detailed submission rules and edge cases. |
| ELR-03 | Grade and feedback behavior cannot be specified safely until visibility, publication, correction, and history rules are clarified. | `INT-L-05`; `INT-S-06`; `OQ-06`; `ASM-06` | Blocks detailed grading and feedback access rules. |
| ELR-04 | Reporting cannot be specified safely until report types, fields, audience, and access rules are clarified. | `INT-L-06`; `OQ-07`; `ASM-01`; `ASM-06` | Blocks report requirements and authorization details. |
| ELR-05 | Security requirements cannot be made measurable until authentication, role assignment, audit, retention, and access policies are clarified. | `INT-A-02`; `INT-A-03`; `INT-A-05`; `OQ-08`; `OQ-10`; `ASM-03`; `ASM-06` | Blocks detailed security and privacy requirements. |
| ELR-06 | Non-functional requirements cannot be made measurable until response-time, availability, backup, recovery, and capacity targets are approved. | `INT-A-06`; `OQ-09`; `ASM-02` | Blocks testable NFRs. |
| ELR-07 | Integration scope cannot be specified safely until standalone or campus-system integration expectations are clarified. | `INT-A-04`; `OQ-11`; `ASM-08` | Blocks interface and data-flow requirements. |

## 9. Readiness Criteria for Skill 03

Skill 03 should not write detailed final requirements until the student decides how to handle unresolved answers.

| Criterion ID | Criterion | Current state |
|---|---|---|
| RC-01 | The student reviews the raw Skill 02 output. | Completed for this reviewed baseline. |
| RC-02 | Every new simulated answer is approved and recorded with answer ID, source label, date, and reviewer. | Not done; no new simulated answers are approved here. |
| RC-03 | Each `OQ-*` and `OQ-DRAFT-*` item is either answered, partially answered with a stated gap, or explicitly deferred. | Deferred; all remain open for later elicitation or student decision. |
| RC-04 | Student-approved policies exist for late submission, resubmission, file limits, grade publication, notifications, authentication, reporting, retention, integrations, and measurable NFRs, or those areas are excluded from detailed specification. | Not done; these areas remain open. |
| RC-05 | Assumption-based stakeholder topics keep `ASM-*` labels unless validated. | Preserved. |
| RC-06 | No final requirement is written from an unanswered item. | Preserved. |

## 10. Student Decisions Needed Before Skill 03

Before creating detailed requirements, the student must decide whether to:

1. Keep all unresolved policy areas open and write only high-level requirements supported by `SRC-01`.
2. Approve additional simulated stakeholder answers for late submission, resubmission, file limits, grade publication, notifications, authentication, reporting, retention, integrations, and measurable NFR targets.
3. Explicitly defer unresolved areas from Skill 03 so they do not appear as unsupported detailed requirements.

No final requirements are approved in this Step 02 baseline.

## 11. Traceability Notes

- Confirmed case facts trace to `SRC-01` and case-confirmed simulated answers such as `INT-L-01`, `INT-S-01`, `INT-A-01`, and `INT-A-06`.
- Existing simulated answers from `SRC-02` remain labelled according to their original status.
- Assumptions from `SRC-03` keep their `ASM-*` identifiers and are not converted into facts.
- Open questions from `CASE.md` keep their `OQ-*` identifiers.
- Draft open questions retained by reviewed Skill 01 keep their `OQ-DRAFT-*` identifiers.
- Elicitation questions use `ELQ-*` identifiers.
- This reviewed output intentionally avoids final requirements, user stories, use cases, priorities, validation results, and change requests.
