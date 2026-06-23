# Skill 05 Raw Output: Requirements Validation

## 1. Review Status and Boundary

| Field | Value |
|---|---|
| Output type | First AI raw output for Skill 05 requirements validation |
| Created for review by | Gerungan Dave Jordy |
| Creation date | 23 June 2026 |
| Baseline used | Reviewed Skill 01 through Skill 04 outputs |
| Boundary | This validates the current reviewed baseline at its current level of detail. It does not approve new requirements, deferred topics, policies, measurable NFR targets, final traceability, or final diagrams. |

Validation result meanings:

- `Pass`: valid at the reviewed level of detail.
- `Partial`: valid at high level but missing detail remains open.
- `Risk`: baseline item may remain but carries assumption, readiness, or consistency risk.
- `Blocked`: validation depends on unresolved evidence or policy.
- `Not testable yet`: quality or behavior cannot be measured without approved criteria or targets.

## 2. Inputs and Evidence Sources

| Source | Use in this output |
|---|---|
| `outputs/reviewed/01-inception.md` | Reviewed stakeholders, objectives, quality concerns, risks, and open questions. |
| `outputs/reviewed/02-elicitation.md` | Reviewed answer classification, open decision log, and elicitation risks. |
| `outputs/reviewed/03-requirements.md` | Authoritative requirements, NFR candidates, deferred topics, assumptions, and traceability. |
| `outputs/reviewed/04-user-stories.md` | Reviewed user stories and story readiness. |
| `outputs/reviewed/05-prioritization.md` | Reviewed MoSCoW, value, readiness risk, and deferred decision areas. |
| `evaluation/ai-output-review.md` | Prior correction record and evidence discipline rules. |

## 3. Validation Method

| Check type | Meaning |
|---|---|
| Traceability | Checks whether reviewed stories and priorities map back to reviewed requirements and evidence. |
| Consistency | Checks whether reviewed artefacts agree with each other. |
| Ambiguity | Checks whether wording could be interpreted beyond approved evidence. |
| Readiness | Checks whether the item is ready only at high level, partial, blocked, or assumption-labelled. |
| Testability | Checks whether the item can be validated with observable criteria under the current reviewed baseline. |
| Priority-risk alignment | Checks whether priority labels preserve readiness risk. |
| Evidence boundary | Checks whether open questions, assumptions, and deferred topics remain separated from approved scope. |

## 4. Validation Inventory

| Item group | Items checked | Baseline status |
|---|---|---|
| Functional requirements | `FR-01` through `FR-11` | Case-supported high-level capabilities, with several partial or high-risk details. |
| Quality concerns / NFR candidates | `NFR-01` through `NFR-05` | Partial; not fully measurable or testable yet. |
| Artefact constraints | `CON-SPEC-01` through `CON-SPEC-04` | Supported assignment workflow constraints, with `CON-SPEC-04` assumption-labelled through `ASM-08`. |
| User stories | `US-01` through `US-11` | All mapped to existing `FR-*` items. |
| Priorities | Skill 04 MoSCoW and value-risk table | Priorities assigned only to reviewed requirements, NFR candidates, and constraints. |
| Deferred topics | `DR-01` through `DR-18` | Not approved requirements; validation blockers or change candidates only. |

## 5. Validation Matrix

| Validation ID | Reviewed item | Check type | Result | Evidence basis | Finding | Required action |
|---|---|---|---|---|---|---|
| `VAL-01` | `FR-01`; `US-01`; `UC-01` | Traceability / readiness | Partial | `SRC-01`; `INT-L-01`; `OQ-01`; `DR-01` | Assignment creation is valid at high level, but mandatory fields and validation rules remain open. | Defer detail / student approval needed |
| `VAL-02` | `FR-02`; `US-02`; `UC-02` | Traceability / testability | Partial | `SRC-01`; `INT-L-01`; `OQ-02`; `OQ-12`; `DR-02`; `DR-03` | Deadline definition is valid at high level, but timezone, cutoff, deadline-change, and late-submission behavior are not testable yet. | Defer detail / student approval needed |
| `VAL-03` | `FR-03`; `US-03`; `UC-03` | Traceability / ambiguity | Partial | `SRC-01`; `INT-S-01`; `OQ-01`; `DR-01` | Assignment viewing is valid at high level, but exact visible fields are not specified. | Clarify later |
| `VAL-04` | `FR-04`; `US-04`; `UC-04` | Readiness / testability | Partial | `SRC-01`; `INT-S-01`; `OQ-02`; `OQ-03`; `OQ-04`; `OQ-DRAFT-03`; `DR-03` to `DR-07` | File submission is valid at high level, but detailed validation is blocked by unresolved submission policy, file policy, failure handling, and receipt evidence. | Defer detail / student approval needed |
| `VAL-05` | `FR-05`; `US-05`; `UC-05` | Readiness / ambiguity | Risk | `SRC-01`; `INT-S-01`; `INT-S-02`; `OQ-12`; `OQ-DRAFT-01`; `OQ-DRAFT-03`; `DR-02`; `DR-07`; `DR-08` | Status and deadline monitoring is partially supported, but exact status values, confirmation details, and update rules are unresolved. | Clarify / change request candidate |
| `VAL-06` | `FR-06`; `US-06`; `UC-06` | Readiness / testability | Partial | `SRC-01`; `INT-L-01`; `INT-L-05`; `OQ-06`; `DR-10` | Grade recording is valid at high level, but publication, correction, visibility, and history rules are unresolved. | Defer detail / student approval needed |
| `VAL-07` | `FR-07`; `US-07`; `UC-07` | Readiness / testability | Partial | `SRC-01`; `INT-L-01`; `INT-L-05`; `OQ-06`; `DR-10` | Feedback provision is valid at high level, but feedback publication, visibility, correction, and history rules are unresolved. | Defer detail / student approval needed |
| `VAL-08` | `FR-08`; `US-08`; `UC-08` | Evidence boundary / readiness | Risk | `SRC-01`; `INT-A-01`; `OQ-08`; `ASM-03`; `DR-12`; `DR-13` | User management is valid at high level, but authentication, role assignment, managed user fields, and multi-role behavior remain open. | Clarify / student approval needed |
| `VAL-09` | `FR-09`; `US-09`; `UC-09` | Readiness / evidence boundary | Partial | `SRC-01`; `INT-A-01`; `OQ-11`; `DR-17`; `DR-18` | Course management is valid at high level, but required course data, enrolment rules, and integration boundary remain open. | Clarify later |
| `VAL-10` | `FR-10`; `US-10`; `UC-10` | Readiness / evidence boundary | Partial | `SRC-01`; `INT-A-01`; `OQ-DRAFT-02`; `DR-14`; `DR-18` | System configuration is valid at high level, but configuration items and governance authority are unresolved. | Clarify / student approval needed |
| `VAL-11` | `FR-11`; `US-11`; `UC-11` | Readiness / testability | Risk | `SRC-01`; `INT-L-06`; `OQ-07`; `DR-11`; `ASM-01`; `ASM-06` | Reporting is supported only at a high level; report types, contents, filters, recipients, and access rights remain undefined. | Change request candidate |
| `VAL-12` | `NFR-01` | Testability | Not testable yet | `SRC-01`; `INT-A-06`; `OQ-09`; `DR-16` | Usability is a reviewed quality concern, but usability criteria and task-completion expectations are not approved. | Define measurable target later |
| `VAL-13` | `NFR-02` | Testability / evidence boundary | Not testable yet | `SRC-01`; `INT-A-06`; `ASM-06`; `OQ-08`; `OQ-10`; `DR-12`; `DR-13`; `DR-15`; `DR-16` | Security is important and assumption-linked, but authentication, authorisation, audit, role, and retention policies are not approved. | Define policy and target later |
| `VAL-14` | `NFR-03` | Testability | Not testable yet | `SRC-01`; `INT-A-06`; `OQ-09`; `DR-16` | Performance is a reviewed quality concern, but response-time, throughput, capacity, and load targets remain open. | Define measurable target later |
| `VAL-15` | `NFR-04` | Testability | Not testable yet | `SRC-01`; `INT-A-06`; `ASM-02`; `OQ-04`; `OQ-09`; `DR-06`; `DR-16` | Reliability is a reviewed quality concern, but availability, backup, recovery, failure-handling, and incident-response targets remain open. | Define measurable target later |
| `VAL-16` | `NFR-05` | Testability / evidence boundary | Not testable yet | `SRC-01`; `INT-A-06`; `ASM-04`; `ASM-05`; `ASM-06`; `OQ-06`; `OQ-10`; `OQ-12`; `OQ-DRAFT-03`; `DR-02`; `DR-07`; `DR-10`; `DR-15` | Data integrity is a reviewed quality concern with assumption support, but identifier, timestamp, correction, receipt, and retention rules remain incomplete. | Define policy and target later |
| `VAL-17` | `CON-SPEC-01`; `CON-SPEC-02`; `CON-SPEC-03` | Consistency / traceability | Pass | `README.md`; reviewed Skill 01; reviewed Skill 02; `evaluation/ai-output-review.md` | Traceability, raw/reviewed separation, and evidence separation are consistently applied across reviewed outputs. | No action |
| `VAL-18` | `CON-SPEC-04` | Evidence boundary | Risk | `ASM-08`; reviewed Skill 01 constraints | Technology independence is consistent with the current baseline, but integration or architecture decisions remain open. | Preserve assumption label |
| `VAL-19` | `US-01` through `US-11` | Traceability | Pass | Reviewed Skill 04 traceability summary; reviewed Skill 03 `FR-*` items | Each reviewed product user story maps to an existing functional requirement. | No action |
| `VAL-20` | Skill 04 priorities | Priority-risk alignment | Pass | Reviewed Skill 04 prioritisation | MoSCoW labels do not hide readiness risk; high-priority partial items remain marked high risk. | No action |
| `VAL-21` | `DR-01` through `DR-18` | Evidence boundary | Pass | Reviewed Skill 03 deferred topics; reviewed Skill 04 deferred decision areas | Deferred topics remain decision-needed and are not treated as approved requirements. | No action |

## 6. Readiness and Testability Risks

| Risk area | Related items | Validation risk |
|---|---|---|
| Assignment details | `FR-01`; `FR-02`; `FR-03`; `US-01` to `US-03`; `DR-01` to `DR-03` | High-level requirements are valid, but detailed field validation and deadline behavior are not testable. |
| Submission workflow | `FR-04`; `FR-05`; `US-04`; `US-05`; `DR-03` to `DR-08` | Core submission and monitoring capabilities are important, but detailed scenarios remain blocked by unresolved policy. |
| Grading and feedback | `FR-06`; `FR-07`; `US-06`; `US-07`; `DR-10` | Capabilities are in scope, but visibility, publication, correction, and history rules are not validated. |
| Administration and security | `FR-08`; `FR-10`; `NFR-02`; `US-08`; `US-10`; `DR-12` to `DR-15` | User/configuration management is high-level only; security controls are not measurable or policy-complete. |
| Reporting | `FR-11`; `US-11`; `DR-11` | Reporting is mentioned but not specific enough for detailed validation. |
| Quality targets | `NFR-01` to `NFR-05`; `DR-16` | NFR candidates are not fully testable because measurable targets are missing. |
| Integration and data detail | `FR-09`; `DR-17`; `DR-18`; `ASM-08` | Course/admin data and system boundary remain unclear. |

## 7. Traceability and Consistency Findings

| Finding ID | Finding | Result |
|---|---|---|
| `TCF-01` | Reviewed user stories `US-01` through `US-11` trace to reviewed functional requirements `FR-01` through `FR-11`. | Pass |
| `TCF-02` | Reviewed prioritisation covers `FR-*`, `NFR-*`, and `CON-SPEC-*` items without turning `DR-*` items into requirements. | Pass |
| `TCF-03` | NFR candidates are consistently presented as partial quality concerns, not fully measurable requirements. | Pass |
| `TCF-04` | `ASM-*` references remain labelled and are not converted into confirmed facts. | Pass |
| `TCF-05` | Open questions remain unresolved and traceable. | Pass |
| `TCF-06` | The baseline is internally consistent but intentionally incomplete for detailed validation. | Partial |

## 8. Student Decisions Needed

Before reviewed validation can mark more items fully testable, the student must decide whether to:

1. keep all deferred topics open and accept only high-level validation;
2. approve stakeholder or simulated evidence for assignment fields, deadlines, late submission, resubmission, file limits, receipt evidence, status values, grade and feedback rules, reporting, authentication, retention, integrations, and configuration governance;
3. approve measurable NFR targets for usability, security, performance, reliability, backup, recovery, capacity, and data integrity;
4. decide whether proposed change requests should be rejected, deferred, or sent back through elicitation/specification review.

## 9. Quality Checks

| Check | Result |
|---|---|
| Based on reviewed Skill 01 through Skill 04 baselines. | Passed |
| Validation uses only reviewed Skill 03 requirements, reviewed Skill 04 user stories, and reviewed Skill 04 prioritisation. | Passed |
| No new requirement ID is created. | Passed |
| Deferred `DR-*` items remain blockers or decision areas, not approved requirements. | Passed |
| Open `OQ-*` and `OQ-DRAFT-*` items are not answered. | Passed |
| Partial and assumption-labelled items keep their status and risk visible. | Passed |
| NFR candidates without measurable targets are not marked fully testable. | Passed |
| No policy was invented for late submission, resubmission, file limits, grade publication, notifications, authentication, reporting detail, retention, integrations, or measurable NFR targets. | Passed |
| No final traceability matrix, final diagram, implementation task, or code design is produced. | Passed |
