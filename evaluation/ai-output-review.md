# AI Output Review

This file records student review decisions and corrections made after raw AI output is generated.

## Review 01: Skill 01 Inception

| Field | Value |
|---|---|
| Raw output reviewed | `outputs/raw/01-inception.md` |
| Reviewed output produced | `outputs/reviewed/01-inception.md` |
| Reviewer | Gerungan Dave Jordy |
| Review date | 22 June 2026 |
| Review decision | Accepted with minor clarification and formatting improvements |

### Findings

| ID | Finding | Action taken |
|---|---|---|
| REV-01 | No unsupported functional requirement was found in the raw output. | Kept the inception scope and did not add detailed requirements. |
| REV-02 | Assumptions were labelled with `ASM-*` identifiers and were not presented as confirmed facts. | Preserved this distinction in the reviewed output. |
| REV-03 | Simulated interview evidence was labelled and open matters were not silently decided. | Preserved unresolved policy questions for later elicitation. |
| REV-04 | `OQ-DRAFT-01`, `OQ-DRAFT-02`, and `OQ-DRAFT-03` were useful additions. | Retained all three draft questions in the reviewed baseline. |
| REV-05 | Some wording could be clearer for a reviewed baseline. | Tightened wording, reduced repetition, and made the review status explicit. |

### Corrections and Rationale

No factual correction was required. The reviewed output improves presentation and clarity while preserving the raw output's evidence boundaries.

The reviewed baseline intentionally does not decide late submission, resubmission, file-size limits, grade publication, notifications, authentication, reporting access, data retention, integrations, or measurable NFR targets. These remain open for later elicitation or explicit student approval.

## Review 02: Skill 02 Elicitation

| Field | Value |
|---|---|
| Raw output reviewed | `outputs/raw/02-elicitation.md` |
| Reviewed output produced | `outputs/reviewed/02-elicitation.md` |
| Reviewer | Gerungan Dave Jordy |
| Review date | 23 June 2026 |
| Review decision | Accepted with minor clarification and status updates |

### Findings

| ID | Finding | Action taken |
|---|---|---|
| REV-02-01 | The raw output stayed within elicitation planning and evidence capture. | Preserved the boundary and did not add final requirements. |
| REV-02-02 | The raw output kept assumptions, simulated evidence, partial answers, and unanswered items distinguishable. | Preserved `ASM-*`, `INT-*`, `OQ-*`, and `OQ-DRAFT-*` labels in the reviewed output. |
| REV-02-03 | The question guide covered confirmed stakeholders and labelled secondary stakeholders as assumptions. | Kept lecturer, student, administrator, academic management, and IT support coverage with evidence labels. |
| REV-02-04 | No unsupported policy decision was found in the raw output. | Kept late submission, resubmission, file limits, grade publication, notifications, authentication, reporting, retention, integrations, and measurable NFR targets open. |
| REV-02-05 | Some wording needed to better reflect reviewed status. | Updated review status, readiness criteria, and student decisions needed before Skill 03. |

### Corrections and Rationale

No factual correction was required. The reviewed output improves presentation and explicitly marks student review status while preserving the raw output's elicitation boundaries.

The reviewed Skill 02 baseline intentionally does not approve new simulated answers or final requirements. It keeps unresolved policy and quality-target decisions open before Skill 03.

## Review 03: Skill 03 Specification

| Field | Value |
|---|---|
| Raw output reviewed | `outputs/raw/03-requirements.md` |
| Reviewed output produced | `outputs/reviewed/03-requirements.md` |
| Reviewer | Gerungan Dave Jordy |
| Review date | 23 June 2026 |
| Review decision | Accepted with structural revisions for clarity and evidence discipline |

### Findings

| ID | Finding | Action taken |
|---|---|---|
| REV-03-01 | The raw output stayed within requirements specification and did not create user stories, use cases, prioritisation, validation results, or change requests. | Preserved the Skill 03 boundary in the reviewed output. |
| REV-03-02 | Some `OQ-*` and `ELQ-*` references appeared in evidence positions, even though open questions and elicitation questions are not evidence that a requirement is valid. | Separated supporting evidence from open issues and related questions in the reviewed output. |
| REV-03-03 | Non-functional requirement statements used "shall consider", which is too weak to be a fully testable NFR. | Reframed them as quality concerns and partial NFR candidates until measurable targets are approved. |
| REV-03-04 | The traceability requirement was placed among functional product requirements, even though it is an assignment artefact constraint rather than a Student Task Management System user feature. | Moved traceability into specification constraints and artefact requirements. |
| REV-03-05 | Requirement statuses such as `Supported` could be read as stronger than intended for high-level requirements with missing policy details. | Clarified status values as `Supported at high level` or `Partial`, with unresolved details kept deferred. |

### Corrections and Rationale

No factual correction was required. The raw Skill 03 output correctly avoided unsupported decisions for late submission, resubmission, file limits, grade publication, notifications, authentication, reporting, retention, integrations, and measurable NFR targets.

The reviewed output revises structure and wording because a requirements specification must distinguish between:

- evidence that supports a requirement;
- open questions that block details;
- elicitation questions that show what still needs to be asked;
- assumptions that may inform later work but are not confirmed facts.

This matters because mixing open questions into evidence columns can make an unresolved issue look like proof. Likewise, weak NFR wording such as "shall consider performance" is useful as a quality concern, but it is not yet a measurable, testable requirement. Keeping those items partial protects traceability and makes clear what the student still needs to approve.

The reviewed Skill 03 baseline remains intentionally high-level. It does not approve new simulated policies, measurable targets, integrations, user stories, use cases, priorities, validation results, or change requests.

## Review 04: Skill 04 User Stories and Prioritisation

| Field | Value |
|---|---|
| Raw output reviewed | `outputs/raw/04-user-stories.md`; `outputs/raw/05-prioritization.md` |
| Reviewed output produced | `outputs/reviewed/04-user-stories.md`; `outputs/reviewed/05-prioritization.md` |
| Reviewer | Gerungan Dave Jordy |
| Review date | 23 June 2026 |
| Review decision | Accepted with simplification and structure revisions |

### Findings

| ID | Finding | Action taken |
|---|---|---|
| REV-04-01 | The raw output stayed within Skill 04 and did not create use cases, validation results, implementation tasks, or change requests. | Preserved the boundary in the reviewed outputs. |
| REV-04-02 | The raw user-story output included NFR-derived and artefact-constraint items as story candidates, which made the story list heavier than needed. | Kept product user stories limited to functional requirements and moved NFRs/constraints into supporting consideration sections. |
| REV-04-03 | The raw outputs correctly preserved deferred topics and open questions, but repeated some details across several tables. | Condensed repeated deferred-topic material while preserving IDs and traceability. |
| REV-04-04 | Raw prioritisation correctly warned that MoSCoW labels do not approve unresolved policy details. | Preserved that warning and made the distinction between priority and readiness more explicit. |
| REV-04-05 | No unsupported policy decision was found in the raw outputs. | Kept late submission, resubmission, file limits, grade publication, notifications, authentication, reporting detail, retention, integrations, and measurable NFR targets open. |

### Corrections and Rationale

No factual correction was required. The reviewed outputs improve readability and reduce duplication while preserving the raw output's evidence discipline.

The reviewed user-story output keeps product-facing stories focused on `FR-01` through `FR-11`. NFR and artefact-constraint items remain important, but they are better handled as quality and assignment considerations because they are not product user actions and several are still partial or assumption-labelled.

The reviewed prioritisation output preserves MoSCoW labels, value, and readiness risk. It does not treat deferred topics as approved requirements. High-priority items with unresolved details remain explicitly risky rather than fully ready.

## Review 05: Skill 05 Use Cases, Validation, and Change Requests

| Field | Value |
|---|---|
| Raw output reviewed | `outputs/raw/06-use-case.md`; `outputs/raw/07-validation.md`; `outputs/raw/08-change-request.md` |
| Reviewed output produced | `outputs/reviewed/06-use-case.md`; `outputs/reviewed/07-validation.md`; `outputs/reviewed/08-change-request.md` |
| Reviewer | Gerungan Dave Jordy |
| Review date | 23 June 2026 |
| Review decision | Accepted with simplification and consolidation |

### Findings

| ID | Finding | Action taken |
|---|---|---|
| REV-05-01 | The raw outputs stayed within Skill 05 and did not create final traceability, final diagrams, implementation tasks, or unsupported requirements. | Preserved the boundary in reviewed outputs. |
| REV-05-02 | The raw use-case output was correct but repeated blocker details in several sections. | Simplified the use-case table and consolidated shared open boundaries. |
| REV-05-03 | The raw validation output was accurate but long because it validated almost every item separately. | Grouped validation findings by capability area while preserving key IDs. |
| REV-05-04 | The raw change request output listed ten candidates with overlapping decision areas. | Consolidated them into six broader change request groups. |
| REV-05-05 | No unsupported policy decision was found in the raw outputs. | Kept late submission, resubmission, file limits, grade publication, notifications, authentication, reporting detail, retention, integrations, and measurable NFR targets open. |

### Corrections and Rationale

No factual correction was required. The reviewed outputs improve readability and make the raw-vs-reviewed comparison clearer.

The reviewed use-case output keeps only high-level scenarios because detailed flows would require unresolved policies. The reviewed validation output confirms that traceability and priority-risk alignment are sound, while many items remain partial or not testable yet. The reviewed change request output groups related proposed changes into decision areas so the student can decide what to approve, defer, or reject later.
