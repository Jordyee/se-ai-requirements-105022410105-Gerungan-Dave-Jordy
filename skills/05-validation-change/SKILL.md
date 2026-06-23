---
name: 05-validation-change
description: Use this skill for Requirements Validation and Change Management in the Student Task Management System requirements-engineering assignment. It helps an AI agent validate only the reviewed Skill 03 requirements, reviewed Skill 04 user stories, and reviewed Skill 04 prioritisation; identify consistency, traceability, readiness, and testability risks; draft evidence-safe high-level use-case views; and document proposed change requests without approving new requirements, policies, measurable NFR targets, integrations, or deferred topics.
---

# Skill 05: Validation and Change

## Purpose

Use this skill after Skill 03 and Skill 04 have reviewed baselines.

This skill focuses on:

- validating reviewed requirements against reviewed user stories and prioritisation;
- checking consistency, ambiguity, traceability, priority-readiness mismatch, and testability;
- drafting high-level use-case views only from already reviewed requirements and user stories;
- recording validation findings without treating partial requirements as fully testable;
- documenting proposed change requests and impact analysis without silently approving the change.

This skill does not create new requirements, approve deferred topics, define missing policies, set measurable NFR targets, produce final traceability, produce final diagrams, or implement the system.

## Required Inputs

Read these files before producing any Skill 05 output:

- `README.md`
- `CASE.md`
- `CHANGELOG.md`
- `outputs/reviewed/01-inception.md`
- `outputs/reviewed/02-elicitation.md`
- `outputs/reviewed/03-requirements.md`
- `outputs/reviewed/04-user-stories.md`
- `outputs/reviewed/05-prioritization.md`
- `evaluation/ai-output-review.md`

Use the reviewed Skill 03 and Skill 04 baselines as the authority for validation. Raw outputs and placeholders are not authoritative if they conflict with reviewed outputs.

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
- `US-*` for reviewed user stories from Skill 04.

If the student supplies a new policy, scope choice, reporting detail, security decision, integration decision, retention rule, or measurable NFR target during Skill 05, do not use it directly as validated scope. Ask whether it should first be recorded through the appropriate evidence workflow and reviewed requirements baseline.

## Validation Scope Rules

Validation is a review of the current reviewed baseline, not a way to add detail.

| Source item | Skill 05 handling |
|---|---|
| Reviewed `FR-*` item | Validate against evidence, related `US-*`, priority, readiness, and open boundaries. |
| Reviewed `NFR-*` item | Validate only as a partial quality concern unless measurable targets are already approved. |
| Reviewed `US-*` item | Validate traceability back to `FR-*` and whether readiness matches the source requirement. |
| Reviewed priority item | Validate whether MoSCoW/value/risk labels are consistent with evidence and readiness. |
| `DR-*` deferred topic | Treat as a blocker or change candidate only; do not validate as an approved requirement. |
| `OQ-*` or `OQ-DRAFT-*` item | Treat as open evidence gap; do not answer it during validation. |
| `ASM-*` item | Keep assumption-labelled and risk-labelled; do not treat as confirmed fact. |

Validation may use only the requirements, user stories, and prioritisation already reviewed in Skill 03 and Skill 04. It may cite Skill 01 and Skill 02 to explain evidence gaps, but it must not create new validation criteria from earlier open questions.

## Restricted Topics

The following topics remain open unless a reviewed baseline is explicitly updated before Skill 05 execution:

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

These topics may appear only as open validation risks, blockers, impact areas, or student decisions needed.

## Validation Method

Use a concise validation matrix. Each validation item should include:

| Field | Required content |
|---|---|
| Validation ID | Stable ID such as `VAL-01`, `VAL-02`, and so on. |
| Reviewed item | `FR-*`, `NFR-*`, `US-*`, `CON-SPEC-*`, or priority item being checked. |
| Check type | `Traceability`, `Consistency`, `Ambiguity`, `Readiness`, `Testability`, `Priority-risk alignment`, or `Evidence boundary`. |
| Result | `Pass`, `Partial`, `Blocked`, `Risk`, or `Not testable yet`. |
| Evidence basis | Reviewed source IDs and item IDs. |
| Finding | What is valid, missing, inconsistent, or risky. |
| Required action | `No action`, `Clarify`, `Defer`, `Student approval needed`, or `Change request candidate`. |

Use `Pass` only when the item is supported by reviewed evidence and has no material ambiguity at its current level of detail.

Use `Partial` when the capability is valid at a high level but details remain open.

Use `Blocked` or `Not testable yet` when validation depends on unresolved policy, missing measurable targets, or deferred topics.

Use `Risk` when the item can remain in the baseline but needs visible caution, such as assumption-labelled security or data-integrity concerns.

## Use-Case View Rules

Skill 05 may draft high-level use-case views only as validation aids. A use-case view must not add workflow rules that are not present in reviewed requirements or reviewed user stories.

Each use-case candidate should include:

| Field | Required content |
|---|---|
| Use-case ID | Stable ID such as `UC-01`, `UC-02`, and so on. |
| Use-case name | Short capability name derived from reviewed `FR-*` and `US-*`. |
| Primary actor | Reviewed stakeholder from Skill 01 to Skill 04. |
| Source items | Related `FR-*`, `US-*`, `NFR-*`, or priority items. |
| Goal | Goal already supported by reviewed evidence. |
| Main success scenario | High-level steps only, avoiding unapproved details. |
| Open extensions or blockers | `OQ-*`, `OQ-DRAFT-*`, `DR-*`, or `ASM-*` boundaries that prevent detailed flow. |
| Validation note | Whether the use case is ready at high level, partial, or blocked. |

Do not add status values, file limits, notification channels, authentication flows, report layouts, grade publication rules, retry rules, retention periods, NFR targets, or integration steps unless they already exist in reviewed Skill 03 and Skill 04.

## Change Request Rules

A change request records a proposed change and its impact. It does not approve the change.

Use change request IDs such as `CR-01`, `CR-02`, and so on. Each change request should include:

| Field | Required content |
|---|---|
| Change request ID | Stable `CR-*` ID. |
| Request summary | The proposed change in one sentence. |
| Source of request | Student prompt, validation finding, stakeholder evidence, open question, or assumption. |
| Current baseline affected | Existing `FR-*`, `NFR-*`, `US-*`, `DR-*`, `CON-SPEC-*`, or priority item. |
| Proposed change type | `Clarification`, `Addition`, `Revision`, `Deferral`, `Removal`, or `Policy decision`. |
| Evidence status | `Reviewed evidence exists`, `Needs student approval`, `Needs stakeholder evidence`, or `Unsupported`. |
| Impact analysis | Affected stakeholders, requirements, stories, priorities, validation, and risks. |
| Recommendation | `Approve after evidence update`, `Reject`, `Defer`, or `Ask student/stakeholder`. |
| Approval status | `Proposed`, `Needs approval`, `Rejected`, `Deferred`, or `Approved only if reviewed baseline is updated`. |

Do not change a requirement, story, priority, use case, validation result, traceability item, or diagram directly because a change request exists. Approved changes must go through reviewed evidence and baseline updates first.

## Workflow

1. Confirm the task boundary.
   - Work only on Skill 05 validation and change management.
   - Do not produce final traceability or final diagrams.
   - Do not edit reviewed Skill 05 outputs unless raw Skill 05 output exists and the student explicitly asks for reviewed output.

2. Verify prerequisites.
   - Confirm that reviewed Skill 01 through Skill 04 outputs exist.
   - Confirm that `outputs/reviewed/03-requirements.md`, `outputs/reviewed/04-user-stories.md`, and `outputs/reviewed/05-prioritization.md` are the validation baseline.
   - Check `evaluation/ai-output-review.md` for corrections and review decisions.

3. Build the validation inventory.
   - Extract reviewed `FR-*`, `NFR-*`, `CON-SPEC-*`, `DR-*`, and traceability notes from Skill 03.
   - Extract reviewed `US-*` items from Skill 04 user stories.
   - Extract MoSCoW, value, and readiness risk from Skill 04 prioritisation.
   - Preserve each item's status, evidence, and open boundary.

4. Validate traceability and consistency.
   - Confirm each reviewed `US-*` maps to a reviewed `FR-*`.
   - Confirm each priority item maps to a reviewed requirement, quality concern, or artefact constraint.
   - Check that deferred topics remain deferred.
   - Check that partial and assumption-labelled items remain visibly risky.

5. Validate readiness and testability.
   - Mark high-level supported items as valid only at their supported level.
   - Mark partial requirements and NFR candidates as `Partial`, `Risk`, `Blocked`, or `Not testable yet` when details or measurable targets are missing.
   - Do not write acceptance tests that depend on unresolved policy or target decisions.

6. Draft high-level use-case views if requested as part of Skill 05 execution.
   - Derive each use case from reviewed `FR-*` and `US-*` items.
   - Keep steps broad and evidence-safe.
   - Put unresolved alternatives in open extensions or blockers instead of choosing one.

7. Identify change request candidates.
   - Convert validation findings into proposed `CR-*` entries only when a baseline change may be needed.
   - Separate clarification requests from additions, revisions, deferrals, removals, and policy decisions.
   - Mark evidence and approval status honestly.

8. Produce Skill 05 output.
   - If asked to execute the skill, write first AI versions only to raw Skill 05 output files.
   - Suggested raw files are `outputs/raw/06-use-case.md`, `outputs/raw/07-validation.md`, and `outputs/raw/08-change-request.md`.
   - Do not edit raw output after it has been created as first AI evidence; corrections belong in `evaluation/ai-output-review.md`.

## Output Structure

When the skill is executed, use this structure for the raw use-case output:

```markdown
# Skill 05 Raw Output: Use-Case View

## 1. Review Status and Boundary
## 2. Inputs and Evidence Sources
## 3. Use-Case Derivation Rules
## 4. Use-Case Candidates
## 5. Open Extensions and Blockers
## 6. Traceability to Requirements and User Stories
## 7. Student Decisions Needed
## 8. Quality Checks
```

When the skill is executed, use this structure for the raw validation output:

```markdown
# Skill 05 Raw Output: Requirements Validation

## 1. Review Status and Boundary
## 2. Inputs and Evidence Sources
## 3. Validation Method
## 4. Validation Inventory
## 5. Validation Matrix
## 6. Readiness and Testability Risks
## 7. Traceability and Consistency Findings
## 8. Student Decisions Needed
## 9. Quality Checks
```

When the skill is executed, use this structure for the raw change request output:

```markdown
# Skill 05 Raw Output: Change Requests

## 1. Review Status and Boundary
## 2. Inputs and Evidence Sources
## 3. Change Request Rules
## 4. Change Request Candidates
## 5. Impact Analysis
## 6. Approval and Evidence Status
## 7. Student Decisions Needed
## 8. Quality Checks
```

Each section must cite reviewed requirement IDs, story IDs, priority items, source IDs, answer IDs, assumption IDs, deferred-topic IDs, or open-question IDs.

## Quality Checks

Before finishing, verify:

- The output is based on reviewed Skill 01 through Skill 04 baselines.
- Validation uses only reviewed Skill 03 requirements, reviewed Skill 04 user stories, and reviewed Skill 04 prioritisation.
- No new requirement ID is created during Skill 05.
- No deferred `DR-*` item is treated as an approved requirement.
- No open `OQ-*` or `OQ-DRAFT-*` item is answered by the AI.
- Partial and assumption-labelled items keep their status and risk visible.
- NFR candidates without measurable targets are not marked fully testable.
- Change requests are marked proposed, deferred, rejected, or needing approval unless a reviewed baseline has already approved them.
- No policy is invented for late submissions, resubmissions, file limits, grade publication, notifications, authentication, reporting details, retention, integrations, or measurable NFR targets.
- No final traceability matrix, final diagram, implementation task, or code design is produced.

## Failure Conditions

Stop and ask the student if:

- validation would require approving an unresolved policy, target, integration, or security decision;
- a requested use-case step needs a deferred topic to be decided;
- the user asks to treat a partial or assumption-labelled requirement as fully testable;
- a change request would add, revise, or remove baseline scope without explicit student approval;
- the reviewed Skill 03 or Skill 04 baseline is missing or contradicts earlier reviewed outputs;
- the user asks for reviewed Skill 05 output before raw Skill 05 output exists and has been reviewed;
- the user asks Skill 05 to create final traceability, final diagrams, implementation tasks, or unsupported requirements.

## Related Examples

See `skills/05-validation-change/examples.md` for sample prompts, expected behavior, validation patterns, and evidence-safe change request handling.
