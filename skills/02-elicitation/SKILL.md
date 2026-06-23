---
name: 02-elicitation
description: Use this skill for Elicitation in the main Student Task Management System requirements-engineering assignment or for controlled cross-case skill testing. It helps an AI agent plan stakeholder elicitation, prepare interview and clarification questions, capture evidence safely, classify answers as answered, partially answered, unanswered, or assumption-based, and prepare traceable material for later specification without writing final requirements, user stories, use cases, prioritisation, validation results, or change requests.
---

# Skill 02: Elicitation

## Purpose

Use this skill to design and execute a disciplined elicitation step after Skill 01 has a reviewed inception baseline.

This skill focuses on:

- elicitation objectives;
- stakeholder interview planning;
- stakeholder-specific question guides;
- capture of simulated answers and unresolved questions;
- separation of confirmed facts, simulated evidence, assumptions, partial answers, unanswered items, and student decisions;
- readiness notes for later requirements specification.

This skill does not produce final requirements. It prepares traceable elicitation material that the student must review before it can feed Skill 03.

## Required Inputs

For the main Student Task Management System assignment, read these files before producing any elicitation output:

- `README.md`
- `CASE.md`
- `CHANGELOG.md`
- `inputs/stakeholder-notes.md`
- `inputs/interview-answers.md`
- `inputs/assumptions.md`
- `outputs/reviewed/01-inception.md`
- `evaluation/ai-output-review.md`

For cross-case skill testing, read the supplied test case fixture and its cross-case Skill 01 or inception baseline instead. The fixture must provide enough source mapping to distinguish case facts, simulated notes, assumptions, and open questions. If the fixture does not provide a reviewed-style inception baseline, create or request that baseline before using Skill 02.

Use source labels exactly:

- `SRC-01` for the assignment case brief and facts derived from it.
- `SRC-02` for the simulated interview record.
- `SRC-03` for the assumption register.
- `ASM-*` for individual assumptions.
- `INT-*` for individual simulated interview answers.
- `OQ-*` for open questions already identified in the case baseline.
- `OQ-DRAFT-*` for draft open questions retained from the reviewed Skill 01 baseline.

If new elicitation questions are created, give them `ELQ-*` IDs. If new simulated or student-approved answers are provided later, they must receive a new `INT-*` style ID, date, source label, and reviewer or approver before being used as evidence.

## Evidence Rules

Separate every statement into one of these categories:

| Category | Meaning | Allowed wording |
|---|---|---|
| Confirmed case fact | Stated in the assignment case or restated as `CASE-CONFIRMED` interview evidence. | "The case confirms..." |
| Simulated evidence | Recorded in `inputs/interview-answers.md` or explicitly approved as a simulated answer. | "The simulated interview record states..." |
| Partial answer | A response that confirms a topic exists but does not define the policy, rule, threshold, or workflow. | "This is partially answered because..." |
| Unanswered item | A question with no case-supported or approved answer. | "This remains unanswered..." |
| Assumption | Listed in `inputs/assumptions.md`; even accepted assumptions are not facts. | "Assumption ASM-xx states..." |
| Student decision needed | A scope, policy, security, or measurable NFR choice that belongs to the student. | "Student approval is required before..." |

Never turn an unanswered question, a partial answer, or an assumption into a requirement.

## Workflow

1. Confirm the task boundary.
   - Work only on elicitation.
   - Do not continue to requirements specification, user stories, use cases, prioritisation, validation, or change management.
   - Do not fill `outputs/reviewed/02-elicitation.md` unless the student has reviewed the raw elicitation output and explicitly asks for reviewed output.

2. Verify the prerequisite baseline.
   - Confirm that `outputs/reviewed/01-inception.md` exists.
   - Use the reviewed Skill 01 baseline as the starting point for stakeholder coverage, open questions, risks, and student decisions.
   - Preserve the reviewed decision that `OQ-DRAFT-01`, `OQ-DRAFT-02`, and `OQ-DRAFT-03` remain open for elicitation.
   - For cross-case testing, confirm that the fixture has a cross-case inception output or equivalent baseline, and keep the output clearly labelled as test evidence.

3. Build an elicitation coverage map.
   - Map each stakeholder to topics that need clarification.
   - Include confirmed stakeholders: lecturer, student, and administrator.
   - Include assumed secondary stakeholders, such as university or academic management and IT support or system operator, only with their `ASM-*` labels.
   - Link each topic to existing `OQ-*`, `OQ-DRAFT-*`, `INT-*`, or `ASM-*` evidence.

4. Create stakeholder-specific question guides.
   - Use open-ended questions first to discover missing workflow details.
   - Use follow-up questions to clarify policies, exceptions, data, access, quality targets, and evidence needs.
   - Give every question a stable `ELQ-*` ID.
   - Avoid leading questions that silently choose a policy.

5. Classify existing simulated answers.
   - Mark `CASE-CONFIRMED` answers as supporting case facts only when they restate `SRC-01`.
   - Mark `PARTIALLY ANSWERED` answers as incomplete and list what remains missing.
   - Mark `UNANSWERED` answers as unresolved.
   - Do not invent answers for `UNANSWERED` items.

6. Prepare evidence capture rules.
   - Define how a later answer should be recorded: answer ID, stakeholder, question ID, source type, status, date, reviewer, answer text, and affected open questions.
   - Distinguish real stakeholder answers from educational simulations.
   - If the student wants to simulate an answer, ask whether it should be recorded as a student-approved simulated answer or remain an assumption/open question.

7. Identify student decisions needed before specification.
   - Escalate decisions about late submissions, resubmissions, file limits, grade publication, notifications, authentication, reporting, retention, integrations, and measurable NFR targets.
   - Do not choose defaults for convenience.

8. Produce the elicitation output.
   - If asked to execute the skill, write the first AI version to `outputs/raw/02-elicitation.md`.
   - The raw output should be an elicitation plan and evidence-capture draft, not a final requirements document.
   - Do not edit a raw output after it has been created as first AI evidence; corrections belong in `evaluation/ai-output-review.md`.
   - If running a cross-case skill test, write the test evidence under `evaluation/` or another explicitly requested test path, not under the main case `outputs/raw/` or `outputs/reviewed/` folders.

## Output Structure

When the skill is executed, use this structure for the raw elicitation output:

```markdown
# Skill 02 Raw Output: Elicitation Plan and Evidence Capture

## 1. Review Status and Boundary
## 2. Inputs and Evidence Sources
## 3. Elicitation Objectives
## 4. Stakeholder Coverage Map
## 5. Question Guide by Stakeholder
## 6. Existing Interview Answer Classification
## 7. Evidence Capture Template
## 8. Open Questions and Decision Log
## 9. Risks for Later Specification
## 10. Readiness Criteria for Skill 03
## 11. Traceability Notes
```

Each section must cite source IDs, question IDs, or clearly state that the item remains unresolved.

## Quality Checks

Before finishing, verify:

- The output is based on the reviewed Skill 01 baseline, not only the original case.
- Cross-case test outputs cite the test fixture and state that they are not part of the main reviewed baseline.
- Confirmed case facts cite `SRC-01` or `CASE-CONFIRMED` `INT-*` entries.
- Simulated evidence remains labelled as simulation.
- Every assumption reference keeps its `ASM-*` ID.
- Every elicitation question has an `ELQ-*` ID.
- Every open question keeps its original `OQ-*` or `OQ-DRAFT-*` ID.
- Partially answered and unanswered matters remain visibly incomplete.
- No policy is invented for late submissions, resubmissions, file limits, grade publication, notifications, authentication, reporting access, retention, performance, availability, backup, recovery, or integrations.
- The output does not contain final functional requirements, non-functional requirements, user stories, use cases, priorities, validation results, or change requests.
- The output states what must be answered or approved before Skill 03 can write requirements.

## Failure Conditions

Stop and ask the student if:

- the user asks the AI to invent stakeholder answers without labelling them as simulation or assumptions;
- a policy, scope, security, or measurable NFR decision must be chosen before continuing;
- the reviewed Skill 01 baseline is missing;
- the user asks to write final requirements, user stories, use cases, priorities, validation results, or change requests during Skill 02;
- the user asks for reviewed Skill 02 output before raw Skill 02 output exists and has been reviewed;
- a source file contradicts another source in a way that affects the elicitation baseline.

## Related Examples

See `skills/02-elicitation/examples.md` for sample prompts, expected behavior, and evidence-safe elicitation patterns.
