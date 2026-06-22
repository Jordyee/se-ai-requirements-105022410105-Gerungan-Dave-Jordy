---
name: 03-specification
description: Use this skill for Requirements Specification in the Student Task Management System requirements-engineering assignment. It helps an AI agent transform reviewed inception and elicitation evidence into traceable, testable functional and non-functional requirement statements while preserving open questions, assumptions, and student decisions. It must not invent detailed requirements, user stories, use cases, prioritisation, validation results, or change requests.
---

# Skill 03: Specification

## Purpose

Use this skill to prepare a requirements specification after Skill 01 and Skill 02 have reviewed baselines.

This skill focuses on:

- evidence-backed functional requirement statements;
- evidence-backed non-functional requirement statements where measurable targets exist;
- explicit exclusions or deferrals for unresolved topics;
- traceability from each requirement candidate to source evidence;
- consistency checks against open questions and assumptions;
- a clear list of student decisions needed before unsupported details can become requirements.

This skill does not produce user stories, use cases, prioritisation, validation results, or change requests. Those belong to later skills or later approved work.

## Required Inputs

Read these files before producing any specification output:

- `README.md`
- `CASE.md`
- `CHANGELOG.md`
- `inputs/stakeholder-notes.md`
- `inputs/interview-answers.md`
- `inputs/assumptions.md`
- `outputs/reviewed/01-inception.md`
- `outputs/reviewed/02-elicitation.md`
- `evaluation/ai-output-review.md`

Use source labels exactly:

- `SRC-01` for the assignment case brief and facts derived from it.
- `SRC-02` for the simulated interview record.
- `SRC-03` for the assumption register.
- `ASM-*` for individual assumptions.
- `INT-*` for individual simulated interview answers.
- `OQ-*` for open questions already identified in the case baseline.
- `OQ-DRAFT-*` for draft open questions retained from reviewed Skill 01.
- `ELQ-*` for elicitation questions created in Skill 02.

If the student later approves new simulated answers before or during Skill 03, record them first using the Skill 02 evidence capture rules before using them as specification evidence. Do not silently treat a chat message, assumption, or unanswered question as approved evidence.

## Evidence Rules

Separate every statement into one of these categories:

| Category | Meaning | Requirement use |
|---|---|---|
| Confirmed case fact | Stated in `SRC-01` or restated as `CASE-CONFIRMED` interview evidence. | May support high-level requirements. |
| Approved answer | Real stakeholder evidence or student-approved simulated evidence recorded with an ID, date, source type, and reviewer. | May support detailed requirements within the approved scope. |
| Partial answer | Confirms a topic exists but leaves policy, rule, target, or workflow details incomplete. | May support only the confirmed high-level topic; missing details must remain open. |
| Assumption | Listed in `inputs/assumptions.md` or explicitly approved as an assumption. | May support an assumption-labelled requirement only if the student approves using assumptions in Skill 03. |
| Open question | Missing or unresolved information. | Must not become a requirement. |
| Deferred item | An unresolved area intentionally left out of detailed specification. | Record as deferred, not as a requirement. |

Never turn an unanswered question, partial answer, assumption, likely policy, or convenient default into a final requirement.

## Specification Boundaries

Skill 03 may specify only what the evidence supports.

Currently unresolved or restricted areas include:

- late-submission handling;
- resubmission and version-history rules;
- file type and file-size limits;
- upload failure recovery behavior;
- grade and feedback publication, correction, and history rules;
- notification events and channels;
- authentication mechanism and role-assignment policy;
- report types, fields, recipients, and access rights;
- data retention and audit policy;
- campus-system integrations or standalone boundary;
- measurable usability, security, performance, reliability, backup, recovery, capacity, and data-integrity targets.

These areas must stay open, deferred, or assumption-labelled unless the student explicitly approves evidence for them.

## Requirement Style

Use stable requirement IDs:

- `FR-xx` for functional requirements.
- `NFR-xx` for non-functional requirements.
- `DR-xx` for deferred requirement topics.
- `RQ-xx` for requirement-level open questions if a new question is needed during specification.

Each requirement should include:

| Field | Required content |
|---|---|
| ID | Stable requirement ID. |
| Requirement statement | One clear "The system shall..." statement. |
| Type | Functional or non-functional. |
| Evidence | `SRC-*`, `INT-*`, `ASM-*`, `OQ-*`, `OQ-DRAFT-*`, or `ELQ-*` links. |
| Status | `Supported`, `Partial`, `Assumption-labelled`, or `Deferred`. |
| Notes or boundary | What is included, what is not specified, and what remains open. |

Use "shall" for supported requirements. Use "may" only for optional capability candidates that are explicitly labelled as open or assumption-based. Avoid implementation-specific wording unless a source provides it.

## Workflow

1. Confirm the task boundary.
   - Work only on requirements specification.
   - Do not write user stories, use cases, prioritisation, validation results, change requests, or implementation design.
   - Do not edit `outputs/reviewed/03-requirements.md` unless the student has reviewed the raw specification output and explicitly asks for reviewed output.

2. Verify prerequisites.
   - Confirm that `outputs/reviewed/01-inception.md` exists.
   - Confirm that `outputs/reviewed/02-elicitation.md` exists.
   - Use the reviewed baselines as the authority over raw outputs.
   - Check `evaluation/ai-output-review.md` for corrections and review decisions.

3. Build a specification readiness map.
   - List case-confirmed capabilities that can support high-level requirements.
   - List partially answered areas and the exact missing details.
   - List unanswered `OQ-*` and `OQ-DRAFT-*` items that must not become requirements.
   - List assumptions that require labels or student approval before use.

4. Draft only evidence-backed functional requirements.
   - Write high-level requirements for confirmed case capabilities: assignment creation, deadline definition, assignment viewing, file submission, status monitoring, grading, feedback, user management, course management, system configuration, and high-level reporting.
   - Do not add detailed fields, validation rules, status values, file policies, grading policies, report formats, notifications, integrations, or authentication rules unless approved evidence supports them.
   - Where a topic is confirmed but details are missing, write the narrow supported requirement and link the missing details to deferred items or open questions.

5. Draft only evidence-backed non-functional requirements.
   - Include quality areas confirmed by the case: usability, security, performance, reliability, and data integrity.
   - If no measurable target is approved, state the quality concern at a high level and mark measurable targets as open.
   - Do not invent response times, availability percentages, backup schedules, recovery targets, capacity numbers, security mechanisms, audit periods, or retention durations.

6. Record deferred topics.
   - Create `DR-xx` entries for unresolved policy or detail areas.
   - Link each deferred item to its `OQ-*`, `OQ-DRAFT-*`, `ELQ-*`, `INT-*`, or `ASM-*` basis.
   - Make clear that deferred items are not requirements yet.

7. Maintain traceability.
   - Every requirement and deferred item must cite evidence.
   - Trace requirements to objectives or stakeholder groups when the reviewed baselines support it.
   - Keep assumptions visibly labelled and separate from confirmed facts.

8. Ask before deciding.
   - If a requirement needs a policy, workflow, security, scope, integration, or measurable NFR choice not already approved, stop and ask the student.
   - Do not choose defaults because they seem normal for a task-management system.

9. Produce the specification output.
   - If asked to execute the skill, write the first AI version to `outputs/raw/03-requirements.md`.
   - The raw output should be a requirements specification draft with deferred topics and traceability.
   - Do not edit a raw output after it has been created as first AI evidence; corrections belong in `evaluation/ai-output-review.md`.

## Output Structure

When the skill is executed, use this structure for the raw specification output:

```markdown
# Skill 03 Raw Output: Requirements Specification

## 1. Review Status and Boundary
## 2. Inputs and Evidence Sources
## 3. Specification Readiness Map
## 4. Functional Requirements
## 5. Non-Functional Requirements
## 6. Deferred Requirement Topics
## 7. Open Questions Blocking Detail
## 8. Assumption-Labelled Items
## 9. Traceability Matrix
## 10. Student Decisions Needed
## 11. Quality Checks
```

Each section must cite source IDs, answer IDs, question IDs, or clearly state that the item remains unresolved.

## Quality Checks

Before finishing, verify:

- The output is based on reviewed Skill 01 and reviewed Skill 02 baselines.
- Every requirement has a stable `FR-*` or `NFR-*` ID.
- Every deferred topic has a stable `DR-*` ID.
- Confirmed case facts cite `SRC-01` or `CASE-CONFIRMED` `INT-*` entries.
- Simulated evidence remains labelled as simulation.
- Every assumption reference keeps its `ASM-*` ID and assumption status.
- Every open question keeps its original `OQ-*` or `OQ-DRAFT-*` ID.
- Partial and unanswered items remain visibly incomplete.
- No requirement is written from open questions about late submission, resubmission, file limits, grade publication, notifications, authentication, reporting, retention, integrations, or measurable NFR targets.
- No user stories, use cases, priorities, validation results, or change requests are included.
- The output states which decisions require student approval before details can be specified.

## Failure Conditions

Stop and ask the student if:

- the user asks the AI to fill unresolved policies or NFR targets without approved evidence;
- a requirement would require treating an assumption or open question as fact;
- the reviewed Skill 01 or Skill 02 baseline is missing;
- the user asks for user stories, use cases, prioritisation, validation results, or change requests during Skill 03;
- the user asks for reviewed Skill 03 output before raw Skill 03 output exists and has been reviewed;
- a source file contradicts another source in a way that affects the requirements specification.

## Related Examples

See `skills/03-specification/examples.md` for sample prompts, expected behavior, and evidence-safe specification patterns.
