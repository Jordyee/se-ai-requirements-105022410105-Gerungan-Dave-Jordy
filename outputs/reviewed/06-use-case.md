# 06 Use Cases: Reviewed Baseline

## Review Status

| Field | Value |
|---|---|
| Raw source | `outputs/raw/06-use-case.md` |
| Reviewed by | Gerungan Dave Jordy |
| Review date | 23 June 2026 |
| Review outcome | Accepted with simplification and clearer grouping |
| Important boundary | This is a reviewed high-level use-case view, not a detailed use-case specification, final use-case diagram, or implementation design. |

This reviewed version keeps the raw output's evidence boundaries but simplifies the presentation. The use cases remain high level because Skill 03 and Skill 04 did not approve detailed policies, measurable NFR targets, integrations, or deferred topics.

## 1. Inputs and Evidence Sources

| Source | Use in this reviewed output |
|---|---|
| `outputs/raw/06-use-case.md` | First AI use-case output reviewed for this stage. |
| `outputs/reviewed/03-requirements.md` | Authoritative source for `FR-*`, `NFR-*`, `DR-*`, and `CON-SPEC-*` items. |
| `outputs/reviewed/04-user-stories.md` | Authoritative source for `US-*` items and story readiness. |
| `outputs/reviewed/05-prioritization.md` | Reviewed priority and readiness-risk baseline. |
| `evaluation/ai-output-review.md` | Review record and correction rationale. |

## 2. Review Revisions from Raw Output

| Raw output issue or improvement area | Reviewed revision |
|---|---|
| Raw output repeated detailed blocker lists in several places. | Consolidated blockers into one grouped section. |
| Raw use-case rows were correct but verbose. | Kept the same use cases with shorter goals, scenarios, and validation notes. |
| Raw output included a traceability table and decision list that overlapped with validation and change-request outputs. | Kept only the traceability needed for use-case review. |

No new requirement, policy, detailed scenario, acceptance criterion, final traceability item, or diagram content is added in this reviewed version.

## 3. Reviewed Use-Case View

| Use case | Actor | Source | High-level goal | Reviewed status |
|---|---|---|---|---|
| `UC-01` Create assignment | Lecturer | `FR-01`; `US-01`; `OBJ-01` | Define coursework tasks. | Ready at high level; assignment fields and validation remain open. |
| `UC-02` Define deadline | Lecturer | `FR-02`; `US-02`; `OBJ-01` | Set assignment due timing. | Ready at high level; timezone, cutoff, deadline-change, and late-submission rules remain open. |
| `UC-03` View assignment | Student | `FR-03`; `US-03`; `OBJ-02` | Review assignment information. | Ready at high level; displayed fields remain open. |
| `UC-04` Submit file | Student | `FR-04`; `US-04`; `OBJ-02` | Submit coursework work. | Ready at high level with high detail risk; submission policies remain open. |
| `UC-05` Monitor status and deadline | Student | `FR-05`; `US-05`; `OBJ-04` | Track progress and deadline information. | Partial; status values and update rules remain open. |
| `UC-06` Record grade | Lecturer | `FR-06`; `US-06`; `OBJ-03` | Capture assessed result. | Partial; publication, correction, visibility, and history remain open. |
| `UC-07` Provide feedback | Lecturer | `FR-07`; `US-07`; `OBJ-03` | Record assessment comments. | Partial; feedback visibility and history remain open. |
| `UC-08` Manage users | Administrator | `FR-08`; `US-08`; `OBJ-05` | Support user participation. | Ready at high level with assumption-labelled role boundary. |
| `UC-09` Manage courses | Administrator | `FR-09`; `US-09`; `OBJ-05` | Organise assignment activity by course. | Ready at high level; course data and integration boundary remain open. |
| `UC-10` Manage configuration | Administrator | `FR-10`; `US-10`; `OBJ-05` | Control system settings at a high level. | Ready at high level; configuration governance remains open. |
| `UC-11` Access reporting | Lecturer / administrator | `FR-11`; `US-11` | Review assignment activity. | Partial; report contents and access rights remain open. |

## 4. Shared Open Boundaries

| Boundary area | Related IDs |
|---|---|
| Assignment fields, validation, deadline time rules, late submission, and resubmission. | `OQ-01`; `OQ-02`; `OQ-03`; `OQ-12`; `DR-01` to `DR-04` |
| File policy, upload failure handling, receipt proof, and status values. | `OQ-04`; `OQ-DRAFT-01`; `OQ-DRAFT-03`; `DR-05` to `DR-08` |
| Notifications. | `OQ-05`; `DR-09` |
| Grade and feedback publication, correction, visibility, and history. | `OQ-06`; `DR-10` |
| Reporting detail and access rights. | `OQ-07`; `DR-11`; `ASM-01`; `ASM-06` |
| Authentication, role assignment, audit, retention, and configuration governance. | `OQ-08`; `OQ-10`; `OQ-DRAFT-02`; `ASM-03`; `ASM-06`; `DR-12` to `DR-15` |
| Measurable NFR targets, integration boundary, and administrator-managed data detail. | `OQ-09`; `OQ-11`; `ASM-02`; `ASM-08`; `DR-16` to `DR-18` |

## 5. Traceability Summary

| Use cases | Traceability summary |
|---|---|
| `UC-01` to `UC-10` | Derived from Must functional requirements `FR-01` to `FR-10` and user stories `US-01` to `US-10`. |
| `UC-11` | Derived from Should requirement `FR-11` and user story `US-11`; still partial because reporting detail is open. |
| All use cases | Preserve reviewed Skill 04 readiness risk; priority does not approve deferred detail. |

## 6. Quality Checks

| Check | Result |
|---|---|
| Raw Skill 05 use-case output was preserved separately. | Passed |
| Reviewed use cases derive only from reviewed `FR-*` and `US-*` items. | Passed |
| No new requirement or policy is added. | Passed |
| Deferred topics remain open boundaries, not approved scenario steps. | Passed |
| No final diagram or final traceability matrix is produced. | Passed |
