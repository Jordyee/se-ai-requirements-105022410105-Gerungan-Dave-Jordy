---
name: 04-prioritization
description: Use this skill for User Story Derivation and Requirements Prioritisation in the Student Task Management System requirements-engineering assignment. It helps an AI agent derive traceable user-story candidates and prioritise only the reviewed Skill 03 requirements using evidence, readiness, value, risk, and MoSCoW labels while preserving deferred topics, assumptions, open questions, and student approval boundaries. It must not invent new requirements, policy decisions, use cases, validation results, or change requests.
---

# Skill 04: User Story Derivation and Prioritisation

## Purpose

Use this skill after Skill 03 has a reviewed requirements baseline.

This skill focuses on:

- deriving user-story candidates only from reviewed `FR-*`, `NFR-*`, and specification constraints;
- prioritising reviewed requirements with MoSCoW and value-risk reasoning;
- making evidence readiness visible before priority is assigned;
- keeping partial, assumption-labelled, and deferred topics visibly risky or blocked;
- identifying student decisions required before priorities can become final reviewed artefacts.

This skill does not create new requirements, use cases, validation results, change requests, implementation plans, or hidden policy decisions.

## Required Inputs

Read these files before producing any Skill 04 output:

- `README.md`
- `CASE.md`
- `CHANGELOG.md`
- `outputs/reviewed/01-inception.md`
- `outputs/reviewed/02-elicitation.md`
- `outputs/reviewed/03-requirements.md`
- `evaluation/ai-output-review.md`

Use the reviewed Skill 03 baseline as the authority for requirements. Raw outputs and older placeholders are not authoritative if they conflict with reviewed Skill 03.

Use source labels exactly:

- `SRC-01` for the assignment case brief and facts derived from it.
- `SRC-02` for the simulated interview record.
- `SRC-03` for the assumption register.
- `ASM-*` for individual assumptions.
- `INT-*` for individual simulated interview answers.
- `OQ-*` for open questions already identified in the case baseline.
- `OQ-DRAFT-*` for draft open questions retained from reviewed Skill 01.
- `ELQ-*` for elicitation questions created in Skill 02.
- `FR-*` for reviewed functional requirements from Skill 03.
- `NFR-*` for reviewed quality concerns or partial non-functional requirement candidates from Skill 03.
- `DR-*` for deferred requirement topics from Skill 03.
- `CON-SPEC-*` for Skill 03 specification constraints and artefact requirements.

If the student supplies new policy, scope, security, reporting, integration, or measurable NFR decisions during Skill 04, do not use them directly as priorities. Ask whether they should first be recorded through the appropriate earlier evidence workflow and reviewed requirements baseline.

## Evidence And Readiness Rules

Prioritisation is not allowed to upgrade weak evidence.

| Item status | Meaning | Skill 04 handling |
|---|---|---|
| Supported at high level | Reviewed Skill 03 says the capability is supported by case evidence, but details may still be open. | May receive a priority, with readiness notes. |
| Partial | Reviewed Skill 03 says the topic exists but policy, workflow, visibility, target, or measurement details are incomplete. | May receive a priority only with `Partial readiness` and explicit risk or blocker notes. |
| Assumption-labelled | Reviewed Skill 03 uses an `ASM-*` item as a labelled working assumption. | May be included only with assumption status visible; do not treat as confirmed fact. |
| Deferred topic | Reviewed Skill 03 lists the item as `DR-*`. | Do not prioritise as an approved requirement; list as deferred, blocked, or decision-needed. |
| Open question | The item is unresolved under `OQ-*` or `OQ-DRAFT-*`. | Do not convert into a story, requirement, priority, or acceptance detail. |

Never let a MoSCoW label, value score, urgency score, or risk score imply that an unresolved policy is approved.

## Prioritisation Boundaries

Use only the requirements and constraints already present in `outputs/reviewed/03-requirements.md`.

Currently open or restricted topics include:

- late-submission handling;
- resubmission and version-history rules;
- file type and file-size limits;
- upload failure recovery behavior;
- grade and feedback publication, correction, visibility, and history rules;
- notification events and channels;
- authentication mechanism and role-assignment policy;
- report types, fields, recipients, filters, and access rights;
- audit and data retention policy;
- campus-system integrations or standalone boundary;
- measurable usability, security, performance, reliability, backup, recovery, capacity, and data-integrity targets.

These topics may appear only as open risks, deferred topics, or student decisions needed unless the reviewed requirements baseline is updated first.

## User Story Rules

User stories are derived views of existing requirements, not new requirements.

Use story IDs such as `US-01`, `US-02`, and so on. Each story must include:

| Field | Required content |
|---|---|
| Story ID | Stable `US-*` ID. |
| User story | "As a [reviewed stakeholder], I want [capability], so that [reviewed objective or need]." |
| Source requirement | One or more existing `FR-*`, `NFR-*`, or `CON-SPEC-*` IDs. |
| Evidence | The supporting evidence already cited by the source requirement. |
| Readiness | `Ready at high level`, `Partial`, `Assumption-labelled`, or `Blocked/deferred`. |
| Boundary | What the story does not decide. |

Do not add acceptance criteria that require unresolved policies, file limits, status values, reports, authentication behavior, integrations, retention periods, or measurable NFR targets.

## Prioritisation Method

Use a simple, explainable method:

1. MoSCoW label:
   - `Must` for essential case-confirmed capabilities or assignment constraints.
   - `Should` for important capabilities with lower immediate dependency or partial readiness.
   - `Could` for useful but less central capabilities that are still evidence-backed.
   - `Won't for now` only for explicitly deferred or out-of-scope items from reviewed baselines.
2. Value level:
   - `High`, `Medium`, or `Low` stakeholder or assignment value.
3. Risk/readiness level:
   - `High`, `Medium`, or `Low` delivery or specification risk, based on unresolved questions and assumption status.
4. Rationale:
   - Cite reviewed evidence and explain why the priority does not resolve open issues.

Do not use numeric scoring unless the student explicitly asks for it and confirms the scale. If numeric scoring is used later, the scale and weight choices must be documented as student-approved prioritisation criteria.

## Workflow

1. Confirm the task boundary.
   - Work only on Skill 04 user-story derivation and prioritisation.
   - Do not create use cases, validation results, change requests, implementation tasks, or new requirements.
   - Do not edit reviewed Skill 04 outputs unless raw Skill 04 output exists and the student explicitly asks for reviewed output.

2. Verify prerequisites.
   - Confirm that `outputs/reviewed/01-inception.md` exists.
   - Confirm that `outputs/reviewed/02-elicitation.md` exists.
   - Confirm that `outputs/reviewed/03-requirements.md` exists.
   - Check `evaluation/ai-output-review.md` for Skill 03 corrections and evidence-discipline rules.

3. Build the prioritisation inventory.
   - Extract reviewed `FR-*`, `NFR-*`, and `CON-SPEC-*` items from Skill 03.
   - Extract `DR-*` items separately as deferred topics.
   - Preserve each item's reviewed status, evidence, open issues, and traceability links.

4. Build a readiness map.
   - Mark each source item as supported at high level, partial, assumption-labelled, or deferred.
   - List the exact open `OQ-*`, `OQ-DRAFT-*`, `ASM-*`, or `DR-*` references that affect readiness.
   - Highlight partial NFR candidates as not yet measurable or fully testable.

5. Derive user-story candidates.
   - Create story candidates only from reviewed Skill 03 requirements.
   - Use only reviewed stakeholders: lecturer, student, administrator, and assumption-labelled secondary stakeholders where relevant.
   - Keep story boundaries explicit when source requirements are partial.
   - Do not create stories from `DR-*` items unless the story is clearly marked blocked or deferred and not part of the approved story set.

6. Assign priority labels.
   - Apply MoSCoW labels to reviewed requirements or derived story candidates.
   - Pair every priority with readiness and risk status.
   - Use `Won't for now` for explicitly excluded or deferred items only when that wording matches reviewed baselines.
   - Do not use priority to approve late submission, resubmission, file limits, grade publication, notifications, authentication, reporting details, retention, integrations, or NFR targets.

7. Explain value and risk.
   - Link priority rationale to objectives, stakeholders, and reviewed Skill 03 evidence.
   - Explain how unresolved questions affect implementation readiness.
   - Keep deferred topics visible as blockers, not hidden in rationale text.

8. Identify negotiation or approval points.
   - List priority conflicts and decisions that require student or stakeholder approval.
   - Escalate any policy, scope, security, reporting, integration, or measurable quality-target choice before using it.

9. Produce Skill 04 output.
   - If asked to execute the skill, write the first AI version to raw Skill 04 output files only.
   - Suggested raw files are `outputs/raw/04-user-stories.md` and `outputs/raw/05-prioritization.md`, matching the reviewed output structure.
   - Do not edit raw output after it has been created as first AI evidence; corrections belong in `evaluation/ai-output-review.md`.

## Output Structure

When the skill is executed, use this structure for the raw user-story output:

```markdown
# Skill 04 Raw Output: User Stories

## 1. Review Status and Boundary
## 2. Inputs and Evidence Sources
## 3. Story Derivation Rules
## 4. User Story Candidates
## 5. Deferred or Blocked Story Candidates
## 6. Traceability to Reviewed Requirements
## 7. Student Decisions Needed
## 8. Quality Checks
```

When the skill is executed, use this structure for the raw prioritisation output:

```markdown
# Skill 04 Raw Output: Requirements Prioritisation

## 1. Review Status and Boundary
## 2. Inputs and Evidence Sources
## 3. Prioritisation Method
## 4. Requirements Readiness Map
## 5. MoSCoW Prioritisation Table
## 6. Value-Risk Notes
## 7. Deferred Topics and Blockers
## 8. Priority Conflicts and Student Decisions Needed
## 9. Traceability Matrix
## 10. Quality Checks
```

Each section must cite requirement IDs, source IDs, answer IDs, assumption IDs, or open question IDs from reviewed baselines.

## Quality Checks

Before finishing, verify:

- The output is based on reviewed Skill 01, Skill 02, and Skill 03 baselines.
- No new requirement ID is created during Skill 04.
- Every user story maps back to an existing `FR-*`, `NFR-*`, or `CON-SPEC-*` item.
- Every priority maps back to an existing reviewed requirement, quality concern, or artefact constraint.
- `DR-*` items remain deferred or blocked, not approved requirements.
- Partial and assumption-labelled items keep their status and risk visible.
- Open questions keep their original `OQ-*` or `OQ-DRAFT-*` IDs.
- No policy is invented for late submissions, resubmissions, file limits, grade publication, notifications, authentication, reporting details, retention, integrations, or measurable NFR targets.
- No use cases, validation results, change requests, implementation design, or acceptance tests are produced.
- The output states which priorities or conflicts require student approval before becoming reviewed artefacts.

## Failure Conditions

Stop and ask the student if:

- prioritising an item requires approving a policy or NFR target that is still open;
- a requested story would require inventing a requirement not present in reviewed Skill 03;
- a deferred `DR-*` topic is being treated as an approved requirement;
- the reviewed Skill 03 baseline is missing or contradicts earlier reviewed outputs;
- the user asks for reviewed Skill 04 output before raw Skill 04 output exists and has been reviewed;
- the user asks Skill 04 to create use cases, validation results, change requests, or implementation tasks.

## Related Examples

See `skills/04-prioritization/examples.md` for sample prompts, expected behavior, and evidence-safe prioritisation patterns.
