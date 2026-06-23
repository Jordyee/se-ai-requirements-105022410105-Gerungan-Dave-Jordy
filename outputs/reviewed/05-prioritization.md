# 05 Prioritisation: Reviewed Baseline

## Review Status

| Field | Value |
|---|---|
| Raw source | `outputs/raw/05-prioritization.md` |
| Reviewed by | Gerungan Dave Jordy |
| Review date | 23 June 2026 |
| Review outcome | Accepted with simplification and clearer separation between priority and readiness |
| Important boundary | This reviewed output prioritises existing reviewed Skill 03 items only. It does not approve deferred topics, detailed policies, measurable NFR targets, use cases, validation results, or change requests. |

This reviewed version preserves the raw output's MoSCoW/value-risk approach but shortens repeated explanation. Priority means relative importance for planning and discussion; it does not mean unresolved details are approved.

## 1. Inputs and Evidence Sources

| Source | Use in this reviewed output |
|---|---|
| `outputs/raw/05-prioritization.md` | First AI prioritisation output reviewed for this stage. |
| `outputs/reviewed/01-inception.md` | Reviewed objectives, stakeholders, risks, and open questions. |
| `outputs/reviewed/02-elicitation.md` | Reviewed answer classification and open decision log. |
| `outputs/reviewed/03-requirements.md` | Authoritative source for `FR-*`, `NFR-*`, `DR-*`, and `CON-SPEC-*` items. |
| `evaluation/ai-output-review.md` | Review corrections and rationale. |

## 2. Review Revisions from Raw Output

| Raw output issue or improvement area | Reviewed revision |
|---|---|
| Raw output had a long readiness map and traceability table. | Condensed into a single priority table plus focused blocker list. |
| Raw output prioritised NFRs alongside FRs but some NFRs are not measurable. | Kept NFRs in the priority table with explicit `Partial` or `Assumption-labelled` readiness. |
| Raw output listed all deferred topics in full. | Grouped deferred topics by decision area for easier review. |
| Raw output included artefact constraints. | Preserved them as assignment workflow priorities, separate from product capability priorities. |

## 3. Prioritisation Method

| Dimension | Values | Reviewed rule |
|---|---|---|
| MoSCoW | `Must`, `Should`, `Could`, `Won't for now` | Used only for reviewed requirements, quality concerns, artefact constraints, and explicit deferred-topic handling. |
| Value | `High`, `Medium`, `Low` | Based on reviewed objectives, stakeholder need, and assignment evidence value. |
| Readiness risk | `Low`, `Medium`, `High` | Based on open questions, partial answers, assumption labels, and missing measurable targets. |

`Must` does not mean "fully specified." Several `Must` items remain high risk because the case confirms the capability but not its detailed policy.

## 4. Reviewed MoSCoW Prioritisation

| Item | MoSCoW | Value | Readiness risk | Review rationale |
|---|---|---|---|---|
| `FR-01` Assignment creation | Must | High | Medium | Core lecturer capability for `OBJ-01`; fields and validation remain open under `OQ-01` and `DR-01`. |
| `FR-02` Deadline definition | Must | High | High | Core lecturer capability for `OBJ-01`; deadline cutoff, timezone, and late-submission handling remain open. |
| `FR-03` Assignment viewing | Must | High | Medium | Core student capability for `OBJ-02`; exact student-facing fields remain open. |
| `FR-04` File submission | Must | High | High | Core student capability for `OBJ-02`; file policy, failure handling, late submission, resubmission, and receipt proof remain unresolved. |
| `FR-05` Status and deadline monitoring | Must | High | High | Directly supports `OBJ-04`; status values and update rules remain open. |
| `FR-06` Grade recording | Must | High | High | Core lecturer capability for `OBJ-03`; publication and correction rules remain open. |
| `FR-07` Feedback provision | Must | High | High | Core lecturer capability for `OBJ-03`; visibility, history, and correction rules remain open. |
| `FR-08` User management | Must | High | High | Core administrator capability for `OBJ-05`; authentication and role assignment remain open. |
| `FR-09` Course management | Must | High | Medium | Core administrator capability for `OBJ-05`; course data and integration boundary remain open. |
| `FR-10` System configuration | Must | High | High | Core administrator capability; configuration governance remains open. |
| `FR-11` Reporting | Should | Medium | High | Reporting is case-supported only at a high level; report contents and access rights remain undefined. |
| `NFR-01` Usability | Should | High | High | Confirmed quality area, but usability criteria are not measurable yet. |
| `NFR-02` Security | Must | High | High | Important for academic data and role-based operations; mechanism, audit, role, and retention policies remain open. |
| `NFR-03` Performance | Should | Medium | High | Confirmed quality area, but response-time, capacity, throughput, and load targets remain open. |
| `NFR-04` Reliability | Should | High | High | Important for submission and record access; availability, backup, recovery, and upload failure rules remain open. |
| `NFR-05` Data integrity | Must | High | High | Important for academic records; identifier, timestamp, correction, receipt, and retention rules remain incomplete. |
| `CON-SPEC-01` Traceability | Must | High | Low | Required for assignment evidence quality. |
| `CON-SPEC-02` Raw/reviewed separation | Must | High | Low | Required by repository evidence policy. |
| `CON-SPEC-03` Evidence separation | Must | High | Low | Required to keep facts, simulated evidence, assumptions, open questions, and deferred topics distinguishable. |
| `CON-SPEC-04` Technology independence | Should | Medium | Medium | Useful working rule while integration and architecture boundaries remain open. |

## 5. Priority Groups

| Group | Items | Meaning |
|---|---|---|
| Core product Musts | `FR-01` to `FR-10`; `NFR-02`; `NFR-05` | Highest business and academic-record importance, but many remain partial at the detail level. |
| Important Shoulds | `FR-11`; `NFR-01`; `NFR-03`; `NFR-04`; `CON-SPEC-04` | Important but blocked by missing detail, measurable targets, or lower immediate centrality. |
| Assignment evidence Musts | `CON-SPEC-01`; `CON-SPEC-02`; `CON-SPEC-03` | Required to satisfy the assignment workflow and preserve traceability. |
| Deferred / not approved as requirements | `DR-01` through `DR-18` | Decision-needed topics only; not approved scope or acceptance details. |

No reviewed item is labelled `Could` in this baseline because the currently specified product capabilities are either core case capabilities or partial but important quality/reporting concerns. No deferred topic is labelled as an approved `Must`, `Should`, or `Could` requirement.

## 6. Deferred Decision Areas

| Decision area | Related IDs | Review handling |
|---|---|---|
| Assignment creation and deadline details | `DR-01`; `DR-02`; `OQ-01`; `OQ-12` | Keep open; do not add fields, validation, timezone, or cutoff rules. |
| Submission policy | `DR-03` to `DR-08`; `OQ-02`; `OQ-03`; `OQ-04`; `OQ-DRAFT-01`; `OQ-DRAFT-03` | High decision urgency, but not approved as detailed requirements. |
| Notifications | `DR-09`; `OQ-05` | Not approved as a requirement in this baseline. |
| Grade and feedback policy | `DR-10`; `OQ-06` | High decision urgency; publication, correction, visibility, and history remain open. |
| Reporting detail | `DR-11`; `OQ-07`; `ASM-01`; `ASM-06` | Reporting remains high-level only. |
| Security, roles, audit, and retention | `DR-12`; `DR-13`; `DR-15`; `OQ-08`; `OQ-10`; `ASM-03`; `ASM-06` | High decision urgency; no mechanism or retention rule is approved. |
| Measurable quality targets | `DR-16`; `OQ-09`; `ASM-02` | Required before later validation can be testable. |
| Integration and administrator-managed data detail | `DR-17`; `DR-18`; `OQ-11`; `OQ-DRAFT-02`; `ASM-08` | Keep open until explicitly approved. |

## 7. Student Decisions Still Needed

Before later stages can safely add more detail, the student must decide whether to:

1. Keep all deferred topics open through Skill 05 and validation.
2. Approve simulated evidence for late submission, resubmission, file limits, grade publication, notifications, authentication, reporting, retention, integrations, or measurable NFR targets.
3. Keep NFRs as partial quality concerns or approve measurable targets so they can become testable.
4. Keep reporting as high-level only or add detailed report requirements through approved evidence.

## 8. Traceability Summary

| Priority item type | Items | Traceability source |
|---|---|---|
| Functional requirements | `FR-01` to `FR-11` | Reviewed Skill 03 functional requirements and traceability matrix. |
| Quality concerns / partial NFR candidates | `NFR-01` to `NFR-05` | Reviewed Skill 03 quality concerns and partial NFR candidates. |
| Artefact constraints | `CON-SPEC-01` to `CON-SPEC-04` | Reviewed Skill 03 specification constraints and assignment evidence policy. |
| Deferred blockers | `DR-01` to `DR-18` | Reviewed Skill 03 deferred requirement topics. |

## 9. Quality Checks

| Check | Result |
|---|---|
| Raw Skill 04 prioritisation output was preserved separately. | Passed |
| Priority labels apply only to reviewed Skill 03 items. | Passed |
| Partial and assumption-labelled statuses remain visible. | Passed |
| Deferred topics remain decision-needed, not approved requirements. | Passed |
| Open questions keep their original `OQ-*` or `OQ-DRAFT-*` IDs. | Passed |
| No policy was invented for late submission, resubmission, file limits, grade publication, notifications, authentication, reporting detail, retention, integrations, or measurable NFR targets. | Passed |
| No use cases, validation results, change requests, implementation tasks, or acceptance tests are included. | Passed |
