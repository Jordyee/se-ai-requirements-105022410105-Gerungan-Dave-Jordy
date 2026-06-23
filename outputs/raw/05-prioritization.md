# Skill 04 Raw Output: Requirements Prioritisation

## 1. Review Status and Boundary

| Field | Value |
|---|---|
| Raw output | `outputs/raw/05-prioritization.md` |
| Skill | Skill 04: User Story Derivation and Prioritisation |
| Generated date | 23 June 2026 |
| Review status | Raw AI output; not yet student-reviewed |
| Boundary | This file prioritises only reviewed Skill 03 requirements, quality concerns, and artefact constraints. It is not a reviewed prioritisation baseline, use case document, validation result, implementation plan, or change request. |

Priority labels in this raw output are recommendations for review. They do not approve unresolved policies, deferred topics, measurable NFR targets, or new requirements.

## 2. Inputs and Evidence Sources

| Source | Role in this raw output |
|---|---|
| `README.md` | Assignment workflow and evidence-handling policy. |
| `CASE.md` / `SRC-01` | Case-confirmed project scope and quality areas. |
| `outputs/reviewed/01-inception.md` | Reviewed objectives, stakeholders, constraints, open questions, and risks. |
| `outputs/reviewed/02-elicitation.md` | Reviewed answer classification and unresolved decision log. |
| `outputs/reviewed/03-requirements.md` | Authoritative source for `FR-*`, `NFR-*`, `DR-*`, and `CON-SPEC-*` items. |
| `evaluation/ai-output-review.md` | Review guidance requiring partial and assumption-labelled items to remain visibly incomplete. |

## 3. Prioritisation Method

This raw prioritisation uses MoSCoW labels with value-risk notes:

| Dimension | Values | Meaning |
|---|---|---|
| MoSCoW | `Must`, `Should`, `Could`, `Won't for now` | Relative priority for reviewed requirements or deferred topics. |
| Value | `High`, `Medium`, `Low` | Stakeholder or assignment value based on reviewed objectives and case scope. |
| Risk/readiness | `Low`, `Medium`, `High` | Risk created by open questions, partial evidence, assumptions, or missing measurable targets. |

MoSCoW labels do not change requirement readiness. A `Must` item can still have high risk if its detailed rules are unresolved.

## 4. Requirements Readiness Map

| Item | Reviewed status | Evidence | Open or deferred items | Readiness for prioritisation |
|---|---|---|---|---|
| `FR-01` Assignment creation | Supported at high level | `SRC-01`; `INT-L-01` | `OQ-01`; `DR-01` | Prioritisable; details incomplete. |
| `FR-02` Deadline definition | Supported at high level | `SRC-01`; `INT-L-01` | `OQ-02`; `OQ-12`; `DR-02`; `DR-03` | Prioritisable; policy and time rules incomplete. |
| `FR-03` Assignment viewing | Supported at high level | `SRC-01`; `INT-S-01` | `OQ-01`; `DR-01` | Prioritisable; display details incomplete. |
| `FR-04` File submission | Supported at high level | `SRC-01`; `INT-S-01` | `OQ-02`; `OQ-03`; `OQ-04`; `OQ-DRAFT-03`; `DR-03` to `DR-07` | Prioritisable; high unresolved-detail risk. |
| `FR-05` Status and deadline monitoring | Partial | `SRC-01`; `INT-S-01`; `INT-S-02` | `OQ-12`; `OQ-DRAFT-01`; `OQ-DRAFT-03`; `DR-02`; `DR-07`; `DR-08` | Prioritisable only with partial status visible. |
| `FR-06` Grade recording | Partial | `SRC-01`; `INT-L-01`; `INT-L-05` | `OQ-06`; `DR-10` | Prioritisable only with publication/correction gaps visible. |
| `FR-07` Feedback provision | Partial | `SRC-01`; `INT-L-01`; `INT-L-05` | `OQ-06`; `DR-10` | Prioritisable only with publication/correction gaps visible. |
| `FR-08` User management | Supported at high level | `SRC-01`; `INT-A-01` | `OQ-08`; `ASM-03`; `DR-12`; `DR-13` | Prioritisable; account and role policy incomplete. |
| `FR-09` Course management | Supported at high level | `SRC-01`; `INT-A-01` | `OQ-11`; `DR-17`; `DR-18` | Prioritisable; course data and integration boundary incomplete. |
| `FR-10` System configuration | Supported at high level | `SRC-01`; `INT-A-01` | `OQ-DRAFT-02`; `DR-14`; `DR-18` | Prioritisable; governance details incomplete. |
| `FR-11` Reporting | Partial | `SRC-01`; `INT-L-06` | `OQ-07`; `DR-11` | Prioritisable only at high level; report details blocked. |
| `NFR-01` Usability quality concern | Partial | `SRC-01`; `INT-A-06` | `OQ-09`; `DR-16` | Prioritisable as a quality concern, not a testable target. |
| `NFR-02` Security quality concern | Partial / assumption-labelled | `SRC-01`; `INT-A-06`; `ASM-06` | `OQ-08`; `OQ-10`; `DR-12`; `DR-13`; `DR-15`; `DR-16` | Prioritisable as a quality concern; policy details blocked. |
| `NFR-03` Performance quality concern | Partial | `SRC-01`; `INT-A-06` | `OQ-09`; `DR-16` | Prioritisable as a quality concern; no measurable target. |
| `NFR-04` Reliability quality concern | Partial / assumption-linked | `SRC-01`; `INT-A-06`; `ASM-02` | `OQ-04`; `OQ-09`; `DR-06`; `DR-16` | Prioritisable as a quality concern; no measurable target. |
| `NFR-05` Data integrity quality concern | Partial / assumption-labelled | `SRC-01`; `INT-A-06`; `ASM-04`; `ASM-05`; `ASM-06` | `OQ-06`; `OQ-10`; `OQ-12`; `OQ-DRAFT-03`; `DR-02`; `DR-07`; `DR-10`; `DR-15` | Prioritisable as a quality concern; integrity rules incomplete. |
| `CON-SPEC-01` Traceability | Supported | `README.md`; reviewed Skill 01 `OBJ-07`; reviewed Skill 02 traceability notes | None | Prioritisable as assignment artefact constraint. |
| `CON-SPEC-02` Raw/reviewed separation | Supported | `README.md`; `evaluation/ai-output-review.md` | None | Prioritisable as assignment artefact constraint. |
| `CON-SPEC-03` Evidence separation | Supported | `README.md`; `SRC-01`; `SRC-02`; `SRC-03` | None | Prioritisable as assignment artefact constraint. |
| `CON-SPEC-04` Technology independence | Assumption-labelled working rule | `ASM-08`; reviewed Skill 01 constraints | `DR-17` | Prioritisable as a working rule; integration architecture remains open. |

## 5. MoSCoW Prioritisation Table

| Item | MoSCoW | Value | Risk/readiness | Rationale |
|---|---|---|---|---|
| `FR-01` Assignment creation | Must | High | Medium | Assignment creation is core to lecturer workflow and `OBJ-01`; details remain open under `OQ-01` and `DR-01`. |
| `FR-02` Deadline definition | Must | High | High | Deadlines are core to `OBJ-01`, but timezone, cutoff, deadline changes, and late-submission handling remain open under `OQ-02`, `OQ-12`, `DR-02`, and `DR-03`. |
| `FR-03` Assignment viewing | Must | High | Medium | Students need assignment visibility for `OBJ-02`; exact fields remain tied to `OQ-01` and `DR-01`. |
| `FR-04` File submission | Must | High | High | Student submission is core to `OBJ-02`; file policy, late submission, resubmission, failure handling, and proof remain blocked by `DR-03` through `DR-07`. |
| `FR-05` Status and deadline monitoring | Must | High | High | Status and deadline monitoring is confirmed by `OBJ-04`, but status values, receipt details, and update rules remain unresolved. |
| `FR-06` Grade recording | Must | High | High | Grade recording is core to `OBJ-03`, but publication, correction, visibility, and history rules remain open under `OQ-06` and `DR-10`. |
| `FR-07` Feedback provision | Must | High | High | Feedback is core to `OBJ-03`, but feedback visibility, correction, and history rules remain open under `OQ-06` and `DR-10`. |
| `FR-08` User management | Must | High | High | User management is core to `OBJ-05`, but authentication, role assignment, and multi-role behavior remain unresolved under `OQ-08`, `DR-12`, and `DR-13`. |
| `FR-09` Course management | Must | High | Medium | Course management is core to `OBJ-05`; course data and integration boundaries remain open under `OQ-11`, `DR-17`, and `DR-18`. |
| `FR-10` System configuration | Must | High | High | Configuration is core to administrator scope, but policy authority and configurable items remain open under `OQ-DRAFT-02`, `DR-14`, and `DR-18`. |
| `FR-11` Reporting | Should | Medium | High | Reporting is mentioned by the case and `INT-L-06`, but report types, contents, recipients, filters, and access rights remain undefined under `OQ-07` and `DR-11`. |
| `NFR-01` Usability | Should | High | High | Usability is confirmed as a quality area, but criteria and task-completion expectations remain unmeasured under `OQ-09` and `DR-16`. |
| `NFR-02` Security | Must | High | High | Protecting academic data and role-based operations is important, but authentication, authorisation, audit, retention, and role policies remain open. |
| `NFR-03` Performance | Should | Medium | High | Performance is confirmed as a quality area, but response-time, capacity, throughput, and load targets are not approved under `OQ-09` and `DR-16`. |
| `NFR-04` Reliability | Should | High | High | Reliable submissions and record access are important to student and lecturer workflows, but availability, backup, recovery, and failure-handling targets remain open. |
| `NFR-05` Data integrity | Must | High | High | Data integrity protects academic records, but identifier, timestamp, correction, receipt, and retention rules remain incomplete. |
| `CON-SPEC-01` Traceability | Must | High | Low | Traceability is an assignment objective and reviewed artefact requirement. |
| `CON-SPEC-02` Raw/reviewed separation | Must | High | Low | Raw/reviewed separation is required by the assignment evidence policy. |
| `CON-SPEC-03` Evidence separation | Must | High | Low | Facts, simulated evidence, assumptions, open questions, and deferred topics must remain distinguishable. |
| `CON-SPEC-04` Technology independence | Should | Medium | Medium | Technology independence protects the current requirements boundary, but integration and standalone decisions remain open under `DR-17`. |

## 6. Value-Risk Notes

| Theme | Value note | Risk note | Priority implication |
|---|---|---|---|
| Core lecturer workflow | Assignment creation, deadlines, grading, and feedback directly support `OBJ-01` and `OBJ-03`. | Detailed policies for fields, deadlines, late submission, grade publication, and correction remain open. | Keep core lecturer capabilities as `Must`, but mark several as high risk. |
| Core student workflow | Assignment viewing, file submission, and status/deadline monitoring directly support `OBJ-02` and `OBJ-04`. | File limits, upload failures, receipt proof, status labels, late submission, and resubmission remain open. | Keep core student capabilities as `Must`, with high risk on submission and monitoring details. |
| Core administration workflow | User, course, and configuration management directly support `OBJ-05`. | Authentication, role assignment, governance, managed data, and integration boundaries remain open. | Keep administration capabilities as `Must`, but flag policy and governance risk. |
| Reporting | Reporting is in scope at a high level. | Report contents, filters, recipients, and access rights are not defined. | Keep as `Should` until detailed reporting evidence exists. |
| Quality concerns | Usability, security, performance, reliability, and data integrity are confirmed quality areas under `OBJ-06`. | Measurable targets and several policies are missing. | Prioritise security and data integrity as `Must` quality concerns; keep usability, performance, and reliability as `Should` until measurable targets are approved. |
| Assignment evidence constraints | Traceability and raw/reviewed separation are required by the assignment workflow. | Low risk because the policy is already defined. | Keep as `Must` artefact constraints. |

## 7. Deferred Topics and Blockers

Deferred topics are not approved requirements. Their priority here reflects decision urgency only, not scope approval.

| Deferred ID | Topic | Decision urgency | Reason |
|---|---|---|---|
| `DR-01` | Mandatory assignment fields and validation rules. | High | Affects `FR-01` and `FR-03`. |
| `DR-02` | Deadline timezone, cutoff, and deadline-change behavior. | High | Affects `FR-02`, `FR-05`, and data integrity. |
| `DR-03` | Late-submission handling. | High | Affects `FR-02`, `FR-04`, status, grading, and fairness. |
| `DR-04` | Resubmission and version-history behavior. | High | Affects `FR-04` and data integrity. |
| `DR-05` | File type, file-size, storage, and upload security constraints. | High | Affects `FR-04`, security, reliability, and usability. |
| `DR-06` | Upload failure handling and recovery behavior. | High | Affects `FR-04` and `NFR-04`. |
| `DR-07` | Submission confirmation, receipt evidence, and dispute-handling proof. | High | Affects `FR-04`, `FR-05`, and `NFR-05`. |
| `DR-08` | Submission-status values and update rules. | High | Affects `FR-05`. |
| `DR-09` | Notification events and channels. | Medium | Useful to user experience, but no notification requirement is approved. |
| `DR-10` | Grade and feedback publication, correction, history, and visibility. | High | Affects `FR-06`, `FR-07`, and `NFR-05`. |
| `DR-11` | Reporting contents, filters, recipients, and access rights. | Medium | Affects `FR-11`; reporting is high-level only. |
| `DR-12` | Authentication mechanism and account-management policy. | High | Affects `FR-08` and `NFR-02`. |
| `DR-13` | Role assignment and multi-role account behavior. | High | Affects `FR-08` and access control. |
| `DR-14` | System-wide configuration governance. | Medium | Affects `FR-10`; authority is undefined. |
| `DR-15` | Audit and data retention policy. | High | Affects `NFR-02` and `NFR-05`. |
| `DR-16` | Measurable quality targets. | High | Affects all `NFR-*` candidates and later validation. |
| `DR-17` | External integration or standalone system boundary. | Medium | Affects `FR-09`, `CON-SPEC-04`, and architecture scope. |
| `DR-18` | Detailed administrator-managed data. | Medium | Affects `FR-09` and `FR-10`. |

## 8. Priority Conflicts and Student Decisions Needed

| Decision area | Affected items | Why student approval is needed |
|---|---|---|
| Late submission policy | `FR-02`; `FR-04`; `FR-05`; `DR-03` | Priority cannot decide whether late submissions are blocked, accepted, marked, or controlled per assignment. |
| Resubmission and version history | `FR-04`; `NFR-05`; `DR-04` | Priority cannot decide whether replacements are allowed or whether versions are retained. |
| File limits and upload failure handling | `FR-04`; `NFR-04`; `DR-05`; `DR-06` | Priority cannot invent file types, file sizes, retry rules, storage rules, or upload security. |
| Grade and feedback publication | `FR-06`; `FR-07`; `NFR-05`; `DR-10` | Priority cannot decide publication timing, visibility, correction, or history rules. |
| Authentication and role assignment | `FR-08`; `NFR-02`; `DR-12`; `DR-13` | Priority cannot choose authentication mechanisms or role workflows. |
| Reporting detail | `FR-11`; `DR-11` | Priority cannot define report contents, recipients, filters, or access rights. |
| Retention and audit | `NFR-02`; `NFR-05`; `DR-15` | Priority cannot set retained data, audit evidence, or retention periods. |
| Integrations | `FR-09`; `CON-SPEC-04`; `DR-17` | Priority cannot decide standalone or integrated architecture. |
| Measurable NFR targets | `NFR-01` through `NFR-05`; `DR-16` | Priority cannot invent response time, availability, backup, recovery, capacity, or usability targets. |

## 9. Traceability Matrix

| Prioritised item | MoSCoW | Related story | Supporting evidence | Related open or deferred items |
|---|---|---|---|---|
| `FR-01` | Must | US-01 | `SRC-01`; `INT-L-01` | `OQ-01`; `DR-01` |
| `FR-02` | Must | US-02 | `SRC-01`; `INT-L-01` | `OQ-02`; `OQ-12`; `DR-02`; `DR-03` |
| `FR-03` | Must | US-03 | `SRC-01`; `INT-S-01` | `OQ-01`; `DR-01` |
| `FR-04` | Must | US-04 | `SRC-01`; `INT-S-01` | `OQ-02`; `OQ-03`; `OQ-04`; `OQ-DRAFT-03`; `DR-03`; `DR-04`; `DR-05`; `DR-06`; `DR-07` |
| `FR-05` | Must | US-05 | `SRC-01`; `INT-S-01`; `INT-S-02` | `OQ-12`; `OQ-DRAFT-01`; `OQ-DRAFT-03`; `DR-02`; `DR-07`; `DR-08` |
| `FR-06` | Must | US-06 | `SRC-01`; `INT-L-01`; `INT-L-05` | `OQ-06`; `DR-10` |
| `FR-07` | Must | US-07 | `SRC-01`; `INT-L-01`; `INT-L-05` | `OQ-06`; `DR-10` |
| `FR-08` | Must | US-08 | `SRC-01`; `INT-A-01` | `OQ-08`; `ASM-03`; `DR-12`; `DR-13` |
| `FR-09` | Must | US-09 | `SRC-01`; `INT-A-01` | `OQ-11`; `DR-17`; `DR-18` |
| `FR-10` | Must | US-10 | `SRC-01`; `INT-A-01` | `OQ-DRAFT-02`; `DR-14`; `DR-18` |
| `FR-11` | Should | US-11 | `SRC-01`; `INT-L-06` | `OQ-07`; `DR-11` |
| `NFR-01` | Should | US-12 | `SRC-01`; `INT-A-06` | `OQ-09`; `DR-16` |
| `NFR-02` | Must | US-13 | `SRC-01`; `INT-A-06`; `ASM-06` | `OQ-08`; `OQ-10`; `DR-12`; `DR-13`; `DR-15`; `DR-16` |
| `NFR-03` | Should | US-14 | `SRC-01`; `INT-A-06` | `OQ-09`; `DR-16` |
| `NFR-04` | Should | US-15 | `SRC-01`; `INT-A-06`; `ASM-02` | `OQ-04`; `OQ-09`; `DR-06`; `DR-16` |
| `NFR-05` | Must | US-16 | `SRC-01`; `INT-A-06`; `ASM-04`; `ASM-05`; `ASM-06` | `OQ-06`; `OQ-10`; `OQ-12`; `OQ-DRAFT-03`; `DR-02`; `DR-07`; `DR-10`; `DR-15` |
| `CON-SPEC-01` | Must | US-17 | `README.md`; reviewed Skill 01 `OBJ-07`; reviewed Skill 02 traceability notes | None |
| `CON-SPEC-02` | Must | None | `README.md`; `evaluation/ai-output-review.md` | None |
| `CON-SPEC-03` | Must | None | `README.md`; `SRC-01`; `SRC-02`; `SRC-03` | None |
| `CON-SPEC-04` | Should | None | `ASM-08`; reviewed Skill 01 constraints | `DR-17` |

## 10. Quality Checks

| Check | Result |
|---|---|
| Based on reviewed Skill 01, Skill 02, and Skill 03 baselines. | Passed |
| Every prioritised product item maps to an existing `FR-*`, `NFR-*`, or `CON-SPEC-*` item. | Passed |
| No new requirement ID was created. | Passed |
| `DR-*` items remain deferred or decision-needed, not approved requirements. | Passed |
| Partial and assumption-labelled items keep their status and risk visible. | Passed |
| Open questions keep their original `OQ-*` or `OQ-DRAFT-*` IDs. | Passed |
| No policy was invented for late submissions, resubmissions, file limits, grade publication, notifications, authentication, reporting details, retention, integrations, or measurable NFR targets. | Passed |
| No use cases, validation results, change requests, implementation design, or acceptance tests are included. | Passed |
