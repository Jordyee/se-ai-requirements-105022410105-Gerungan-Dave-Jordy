# Requirements Traceability Matrix: Reviewed Final Baseline

## Review Status

| Field | Value |
|---|---|
| Artefact purpose | Final traceability matrix for the reviewed requirements-engineering baseline. |
| Prepared for | Student Task Management System requirements assignment. |
| Reviewed artefacts used | Skill 01 through Skill 05 reviewed outputs only. |
| Important boundary | This matrix traces existing reviewed artefacts. It does not approve new requirements, policies, measurable NFR targets, detailed use cases, or change requests. |

Open topics remain open. Late submission, resubmission, file limits, grade publication, notifications, authentication, reporting detail, retention, integrations, and measurable NFR targets are traced as unresolved or deferred where applicable.

## Sources Read

| Source | Use in this final matrix |
|---|---|
| `outputs/reviewed/01-inception.md` | Objectives, stakeholders, constraints, quality concerns, assumptions, and open questions. |
| `outputs/reviewed/02-elicitation.md` | Elicitation status, stakeholder question coverage, answer classification, and open decision log. |
| `outputs/reviewed/03-requirements.md` | Authoritative reviewed `FR-*`, `NFR-*`, `DR-*`, and `CON-SPEC-*` baseline. |
| `outputs/reviewed/04-user-stories.md` | Reviewed `US-*` story derivation from functional requirements. |
| `outputs/reviewed/05-prioritization.md` | Reviewed MoSCoW priority, value, and readiness-risk status. |
| `outputs/reviewed/06-use-case.md` | Reviewed high-level `UC-*` use-case view. |
| `outputs/reviewed/07-validation.md` | Reviewed validation findings and remaining validation risks. |
| `outputs/reviewed/08-change-request.md` | Proposed `CR-*` decision groups; none approved. |
| `evaluation/ai-output-review.md` | Student review decisions and correction rationale for raw AI outputs. |

## Coverage Summary

| Coverage area | Result |
|---|---|
| Functional requirements | `FR-01` to `FR-11` are traceable to reviewed objectives, stakeholders, evidence, user stories, priorities, use cases, and validation findings. |
| Product user stories | `US-01` to `US-11` each map to one reviewed functional requirement. |
| Use cases | `UC-01` to `UC-11` each derive from reviewed `FR-*` and `US-*` items. |
| Prioritisation | `FR-01` to `FR-10` are Must; `FR-11` is Should; NFR and constraint priorities follow reviewed Skill 04. |
| NFR candidates | `NFR-01` to `NFR-05` are traceable as quality concerns, but not fully testable because measurable targets remain open. |
| Constraints | `CON-SPEC-01` to `CON-SPEC-04` trace to assignment evidence discipline and reviewed Skill 03. |
| Deferred topics | `DR-01` to `DR-18` remain decision-needed blockers, not approved requirements. |
| Change requests | `CR-01` to `CR-06` remain proposed / needs approval. No final baseline change is approved by this matrix. |

## Stakeholder and Objective Traceability

| Stakeholder or objective | Reviewed status | Related requirements | Related stories | Related use cases | Open or deferred boundaries |
|---|---|---|---|---|---|
| `STK-01` Lecturer | Confirmed case stakeholder | `FR-01`; `FR-02`; `FR-06`; `FR-07`; `FR-11`; related `NFR-*` | `US-01`; `US-02`; `US-06`; `US-07`; `US-11` | `UC-01`; `UC-02`; `UC-06`; `UC-07`; `UC-11` | Assignment fields, deadlines, late submission, resubmission, grade/feedback policy, reporting detail. |
| `STK-02` Student | Confirmed case stakeholder | `FR-03`; `FR-04`; `FR-05`; related `NFR-*` | `US-03`; `US-04`; `US-05` | `UC-03`; `UC-04`; `UC-05` | File policy, receipt proof, upload failure handling, status values, grade/feedback visibility. |
| `STK-03` Administrator | Confirmed case stakeholder | `FR-08`; `FR-09`; `FR-10`; `FR-11`; related `NFR-*` | `US-08`; `US-09`; `US-10`; `US-11` | `UC-08`; `UC-09`; `UC-10`; `UC-11` | Authentication, role assignment, audit, retention, course data, configuration governance, integration boundary. |
| `STK-04` University or academic management | Assumed secondary stakeholder through `ASM-01` | Possible relevance to `FR-11`; `NFR-02`; `NFR-05` | No primary product story approved | No primary use case approved | Reporting, grade governance, policy, and retention remain assumption-supported and unresolved. |
| `STK-05` IT support or system operator | Assumed secondary stakeholder through `ASM-02` | Possible relevance to `NFR-02`; `NFR-03`; `NFR-04`; `NFR-05` | No product story approved | No primary use case approved | Operational security, availability, backup, recovery, monitoring, file constraints, and integrations remain unresolved. |
| `OBJ-01` Create assignments and deadlines | Confirmed by case | `FR-01`; `FR-02` | `US-01`; `US-02` | `UC-01`; `UC-02` | `DR-01`; `DR-02`; `DR-03`; `CR-01` proposed only. |
| `OBJ-02` View assignments and submit files | Confirmed by case | `FR-03`; `FR-04` | `US-03`; `US-04` | `UC-03`; `UC-04` | `DR-01`; `DR-03` to `DR-07`; `CR-01`; `CR-02` proposed only. |
| `OBJ-03` Record grades and feedback | Confirmed by case | `FR-06`; `FR-07` | `US-06`; `US-07` | `UC-06`; `UC-07` | `DR-10`; `CR-03` proposed only. |
| `OBJ-04` Monitor status and deadlines | Confirmed by case | `FR-05` | `US-05` | `UC-05` | `DR-02`; `DR-07`; `DR-08`; `CR-02` proposed only. |
| `OBJ-05` Manage users, courses, and configuration | Confirmed by case | `FR-08`; `FR-09`; `FR-10` | `US-08`; `US-09`; `US-10` | `UC-08`; `UC-09`; `UC-10` | `DR-12` to `DR-18`; `CR-04`; `CR-06` proposed only. |
| `OBJ-06` Consider quality areas | Confirmed at quality-area level | `NFR-01` to `NFR-05` | No product story approved | No product use case approved | `DR-16`; measurable targets remain open; `CR-06` proposed only. |
| `OBJ-07` Maintain traceability | Assignment constraint | `CON-SPEC-01`; related `CON-SPEC-02`; `CON-SPEC-03` | Not a product story | Not a product use case | Traceability evidence must remain separated from raw AI output and unsupported assumptions. |

## Functional Requirement Matrix

| Requirement | Stakeholder / objective | Evidence and elicitation status | Story and priority | Use case | Validation finding | Proposed CR link | Final trace status |
|---|---|---|---|---|---|---|---|
| `FR-01` Allow lecturers to create assignments. | Lecturer; `OBJ-01` | `SRC-01`; `INT-L-01`; high-level supported. `OQ-01` remains open. | `US-01`; Must; high value; medium readiness risk. | `UC-01` Create assignment. | Partial at detail level: fields and validation remain open. | `CR-01` proposed / needs approval. | Covered at high level; detailed fields deferred through `DR-01`. |
| `FR-02` Allow lecturers to define assignment deadlines. | Lecturer; `OBJ-01` | `SRC-01`; `INT-L-01`; high-level supported. `OQ-02` and `OQ-12` remain open. | `US-02`; Must; high value; high readiness risk. | `UC-02` Define deadline. | Partial at detail level: timezone, cutoff, deadline change, and late submission remain open. | `CR-01` proposed / needs approval. | Covered at high level; deadline policy deferred through `DR-02` and `DR-03`. |
| `FR-03` Allow students to view assignment information. | Student; `OBJ-02` | `SRC-01`; `INT-S-01`; high-level supported. Exact fields remain open. | `US-03`; Must; high value; medium readiness risk. | `UC-03` View assignment. | Partial at detail level: displayed fields remain open. | `CR-01` proposed / needs approval. | Covered at high level; field detail deferred through `DR-01`. |
| `FR-04` Allow students to submit files for assignments. | Student; `OBJ-02` | `SRC-01`; `INT-S-01`; high-level supported. `OQ-02`, `OQ-03`, `OQ-04`, and `OQ-DRAFT-03` remain open. | `US-04`; Must; high value; high readiness risk. | `UC-04` Submit file. | Partial / risk: submission policy, file policy, receipt proof, and failure handling remain unresolved. | `CR-02` proposed / needs approval. | Covered at high level; submission details deferred through `DR-03` to `DR-07`. |
| `FR-05` Allow students to monitor assignment status and deadlines. | Student; `OBJ-04` | `SRC-01`; `INT-S-01`; `INT-S-02`; partial. `OQ-DRAFT-01`, `OQ-DRAFT-03`, and `OQ-12` remain open. | `US-05`; Must; high value; high readiness risk. | `UC-05` Monitor status and deadline. | Partial / risk: status values, confirmation details, and update rules remain open. | `CR-02` proposed / needs approval. | Partially covered; status model and receipt evidence deferred through `DR-02`, `DR-07`, and `DR-08`. |
| `FR-06` Allow lecturers to record grades for submissions. | Lecturer; `OBJ-03` | `SRC-01`; `INT-L-01`; `INT-L-05`; partial. `OQ-06` remains open. | `US-06`; Must; high value; high readiness risk. | `UC-06` Record grade. | Partial: publication, correction, visibility, and history rules remain open. | `CR-03` proposed / needs approval. | Partially covered; grade policy deferred through `DR-10`. |
| `FR-07` Allow lecturers to provide feedback for submissions. | Lecturer; `OBJ-03` | `SRC-01`; `INT-L-01`; `INT-L-05`; partial. `OQ-06` remains open. | `US-07`; Must; high value; high readiness risk. | `UC-07` Provide feedback. | Partial: feedback publication, visibility, history, and correction rules remain open. | `CR-03` proposed / needs approval. | Partially covered; feedback policy deferred through `DR-10`. |
| `FR-08` Allow administrators to manage users. | Administrator; `OBJ-05` | `SRC-01`; `INT-A-01`; high-level supported. `OQ-08` and `ASM-03` remain open/assumption-labelled. | `US-08`; Must; high value; high readiness risk. | `UC-08` Manage users. | Partial / risk: authentication, role assignment, and managed user fields remain open. | `CR-04` proposed / needs approval. | Covered at high level; account and role details deferred through `DR-12`, `DR-13`, and `DR-18`. |
| `FR-09` Allow administrators to manage courses. | Administrator; `OBJ-05` | `SRC-01`; `INT-A-01`; high-level supported. `OQ-11` remains open. | `US-09`; Must; high value; medium readiness risk. | `UC-09` Manage courses. | Partial / risk: course data and integration boundary remain open. | `CR-04`; `CR-06` proposed / need approval. | Covered at high level; course data and integration detail deferred through `DR-17` and `DR-18`. |
| `FR-10` Allow administrators to manage system configuration. | Administrator; `OBJ-05` | `SRC-01`; `INT-A-01`; high-level supported. `OQ-DRAFT-02` remains open. | `US-10`; Must; high value; high readiness risk. | `UC-10` Manage configuration. | Partial / risk: configuration governance and exact settings remain open. | `CR-04`; `CR-06` proposed / need approval. | Covered at high level; governance and managed-data detail deferred through `DR-14` and `DR-18`. |
| `FR-11` Support assignment-related reporting at a high level. | Lecturer / administrator; assumed management relevance | `SRC-01`; `INT-L-06`; partial. `OQ-07`, `ASM-01`, and `ASM-06` remain open/assumption-labelled. | `US-11`; Should; medium value; high readiness risk. | `UC-11` Access reporting. | Partial / risk: report contents and access rights remain undefined. | `CR-05` proposed / needs approval. | Partially covered at high level only; reporting detail deferred through `DR-11`. |

## Quality and Constraint Matrix

| Item | Stakeholder / objective | Evidence and status | Priority | Story / use case handling | Validation finding | Final trace status |
|---|---|---|---|---|---|---|
| `NFR-01` Usability concern. | Lecturer / student / administrator; `OBJ-06` | `SRC-01`; `INT-A-06`; partial. `OQ-09` remains open. | Should; high value; high readiness risk. | Not a product story or use case. | Not testable yet because usability criteria are not approved. | Traceable as quality concern; measurable target deferred through `DR-16`. |
| `NFR-02` Security concern. | Administrator / assumed IT support; `OBJ-06` | `SRC-01`; `INT-A-06`; `ASM-06`; partial / assumption-labelled. `OQ-08` and `OQ-10` remain open. | Must; high value; high readiness risk. | Not a product story or use case. | Not testable yet because authentication, authorisation, audit, role, and retention policies are not approved. | Traceable as quality concern; policy detail deferred through `DR-12`, `DR-13`, `DR-15`, and `DR-16`. |
| `NFR-03` Performance concern. | Core stakeholders; `OBJ-06` | `SRC-01`; `INT-A-06`; partial. `OQ-09` remains open. | Should; medium value; high readiness risk. | Not a product story or use case. | Not testable yet because response-time, throughput, capacity, and load targets are not approved. | Traceable as quality concern; measurable target deferred through `DR-16`. |
| `NFR-04` Reliability concern. | Student / lecturer / assumed IT support; `OBJ-06` | `SRC-01`; `INT-A-06`; `ASM-02`; partial / assumption-linked. `OQ-04` and `OQ-09` remain open. | Should; high value; high readiness risk. | Not a product story or use case. | Not testable yet because availability, backup, recovery, and upload failure rules are not approved. | Traceable as quality concern; reliability detail deferred through `DR-06` and `DR-16`. |
| `NFR-05` Data integrity concern. | Lecturer / student / administrator; `OBJ-06` | `SRC-01`; `INT-A-06`; `ASM-04`; `ASM-05`; `ASM-06`; partial / assumption-labelled. | Must; high value; high readiness risk. | Not a product story or use case. | Not testable yet because identifier, timestamp, correction, receipt, and retention rules are incomplete. | Traceable as quality concern; detailed integrity policy deferred through `DR-02`, `DR-07`, `DR-10`, and `DR-15`. |
| `CON-SPEC-01` Preserve traceability between accepted requirements and sources. | `OBJ-07`; assignment evidence discipline | `README.md`; reviewed Skill 01 and Skill 02 traceability notes; supported. | Must; high value; low readiness risk. | Not a product story or use case. | Pass. | Covered by reviewed artefact structure and this final matrix. |
| `CON-SPEC-02` Keep raw AI output separate from reviewed output. | Assignment evidence discipline | `README.md`; `evaluation/ai-output-review.md`; supported. | Must; high value; low readiness risk. | Not a product story or use case. | Pass. | Covered by `outputs/raw/`, `outputs/reviewed/`, and review records. |
| `CON-SPEC-03` Keep facts, simulated evidence, assumptions, open questions, and deferred topics distinguishable. | Assignment evidence discipline | `README.md`; `SRC-01`; `SRC-02`; `SRC-03`; supported. | Must; high value; low readiness risk. | Not a product story or use case. | Pass. | Covered by labels such as `SRC-*`, `INT-*`, `ASM-*`, `OQ-*`, `DR-*`, and `CR-*`. |
| `CON-SPEC-04` Remain independent of implementation technology unless approved. | Assignment evidence discipline; `ASM-08` | `ASM-08`; reviewed Skill 01 constraints; assumption-labelled working rule. | Should; medium value; medium readiness risk. | Not a product story or use case. | Pass / risk. | Covered as working rule; architecture and integration choices remain open. |

## Deferred Topic Matrix

| Deferred item | Related baseline items | Related open questions or assumptions | Related proposed CR | Final trace status |
|---|---|---|---|---|
| `DR-01` Mandatory assignment fields and validation rules. | `FR-01`; `FR-03`; `US-01`; `US-03`; `UC-01`; `UC-03` | `INT-L-02`; `OQ-01` | `CR-01` | Deferred; not approved as detailed requirement. |
| `DR-02` Deadline timezone, cutoff, and deadline-change behavior. | `FR-02`; `FR-05`; `US-02`; `US-05`; `UC-02`; `UC-05` | `OQ-12`; `ASM-05` | `CR-01`; `CR-02` | Deferred; not approved as detailed requirement. |
| `DR-03` Late-submission handling. | `FR-02`; `FR-04`; `US-02`; `US-04`; `UC-02`; `UC-04` | `INT-L-03`; `OQ-02` | `CR-01`; `CR-02` | Deferred; not approved as policy. |
| `DR-04` Resubmission and version-history behavior. | `FR-04`; `US-04`; `UC-04` | `INT-L-04`; `OQ-03` | `CR-02` | Deferred; not approved as policy. |
| `DR-05` File type, file-size, storage, and upload security constraints. | `FR-04`; `US-04`; `UC-04` | `INT-S-03`; `OQ-04` | `CR-02` | Deferred; not approved as file policy. |
| `DR-06` Upload failure handling and recovery behavior. | `FR-04`; `NFR-04`; `US-04`; `UC-04` | `INT-S-04`; `OQ-04` | `CR-02`; `CR-06` | Deferred; not approved as failure-handling rule. |
| `DR-07` Submission confirmation, receipt evidence, and dispute-handling proof. | `FR-04`; `FR-05`; `NFR-05`; `US-04`; `US-05`; `UC-04`; `UC-05` | `INT-S-02`; `OQ-DRAFT-03` | `CR-02` | Deferred; not approved as receipt evidence rule. |
| `DR-08` Submission-status values and update rules. | `FR-05`; `US-05`; `UC-05` | `OQ-DRAFT-01` | `CR-02` | Deferred; not approved as status model. |
| `DR-09` Notification events and channels. | Related to student/lecturer workflows only if later approved | `INT-S-05`; `OQ-05` | `CR-05` | Deferred; notifications are not an approved requirement. |
| `DR-10` Grade and feedback publication, correction, history, and visibility. | `FR-06`; `FR-07`; `NFR-05`; `US-06`; `US-07`; `UC-06`; `UC-07` | `INT-L-05`; `INT-S-06`; `OQ-06`; `ASM-06` | `CR-03` | Deferred; not approved as grade/feedback policy. |
| `DR-11` Reporting contents, filters, recipients, and access rights. | `FR-11`; `US-11`; `UC-11` | `INT-L-06`; `OQ-07`; `ASM-01`; `ASM-06` | `CR-05` | Deferred; reporting remains high level only. |
| `DR-12` Authentication mechanism and account-management policy. | `FR-08`; `NFR-02`; `US-08`; `UC-08` | `INT-A-02`; `OQ-08` | `CR-04` | Deferred; authentication is not specified. |
| `DR-13` Role assignment and multi-role account behavior. | `FR-08`; `NFR-02`; `US-08`; `UC-08` | `INT-A-03`; `OQ-08`; `ASM-03` | `CR-04` | Deferred; role assignment workflow is not specified. |
| `DR-14` System-wide configuration governance. | `FR-10`; `US-10`; `UC-10` | `OQ-DRAFT-02` | `CR-04` | Deferred; configuration authority is not specified. |
| `DR-15` Audit and data retention policy. | `NFR-02`; `NFR-05`; administration baseline | `INT-A-05`; `OQ-10`; `ASM-06` | `CR-04` | Deferred; audit and retention are not approved. |
| `DR-16` Measurable usability, security, performance, reliability, backup, recovery, and capacity targets. | `NFR-01` to `NFR-05` | `INT-A-06`; `OQ-09`; `ASM-02` | `CR-06` | Deferred; NFRs are not fully testable. |
| `DR-17` External integration or standalone system boundary. | `FR-09`; `FR-10`; `CON-SPEC-04` | `INT-A-04`; `OQ-11`; `ASM-08` | `CR-06` | Deferred; no integration decision exists. |
| `DR-18` Detailed administrator-managed data for users, courses, and configuration. | `FR-08`; `FR-09`; `FR-10`; `US-08`; `US-09`; `US-10`; `UC-08`; `UC-09`; `UC-10` | `INT-A-01`; `OQ-DRAFT-02` | `CR-04`; `CR-06` | Deferred; exact managed data is not specified. |

## Change Request Traceability

| Proposed change request | Related items | Validation motivation | Current status |
|---|---|---|---|
| `CR-01` Assignment and deadline detail. | `FR-01` to `FR-03`; `US-01` to `US-03`; `UC-01` to `UC-03`; `DR-01` to `DR-03` | Assignment and deadline capabilities are valid at high level but incomplete in detail. | Proposed / needs approval; not part of final approved baseline. |
| `CR-02` Submission and monitoring detail. | `FR-04`; `FR-05`; `US-04`; `US-05`; `UC-04`; `UC-05`; `DR-03` to `DR-08` | Submission and monitoring are core but high risk because policies and status details are unresolved. | Proposed / needs approval; not part of final approved baseline. |
| `CR-03` Grade and feedback policy. | `FR-06`; `FR-07`; `US-06`; `US-07`; `UC-06`; `UC-07`; `DR-10` | Grading and feedback are in scope but publication, correction, visibility, and history rules are open. | Proposed / needs approval; not part of final approved baseline. |
| `CR-04` Administration and security policy. | `FR-08` to `FR-10`; `NFR-02`; `NFR-05`; `US-08` to `US-10`; `UC-08` to `UC-10`; `DR-12` to `DR-15`; `DR-18` | Administration, security, accountability, and data integrity are important but unresolved in detail. | Proposed / needs approval; not part of final approved baseline. |
| `CR-05` Reporting and notification scope. | `FR-11`; `US-11`; `UC-11`; `DR-09`; `DR-11` | Reporting is high level only, and notifications are not approved. | Proposed / needs approval; not part of final approved baseline. |
| `CR-06` Measurable NFR and integration boundary. | `NFR-01` to `NFR-05`; `FR-09`; `FR-10`; `DR-16`; `DR-17` | NFR validation and integration boundary cannot become testable until targets or decisions are approved. | Proposed / needs approval; not part of final approved baseline. |

## Final Traceability Assessment

| Assessment area | Result |
|---|---|
| Horizontal traceability | Passed for reviewed artefacts: objectives and stakeholders trace to `FR-*`, `US-*`, `UC-*`, validation findings, and proposed `CR-*` groups. |
| Vertical traceability | Passed for high-level functional scope: each reviewed `FR-*` maps forward to a reviewed story and use case. |
| Evidence discipline | Passed: source evidence, assumptions, open questions, deferred topics, and proposed change requests remain distinguishable. |
| Completeness at current baseline level | Partial by design: core capabilities are covered at high level, but detailed policies and measurable NFR targets remain unresolved. |
| Approval boundary | Passed: no deferred topic or proposed change request is treated as approved. |

## Recommended Next Actions

1. Review this final traceability matrix against the reviewed Skill 01 to Skill 05 outputs.
2. Keep `CR-01` to `CR-06` as proposed only unless the student explicitly approves changes with supporting evidence.
3. Before adding detailed policies or measurable targets, answer the related `OQ-*` or `OQ-DRAFT-*` items and update the reviewed baseline through change control.
