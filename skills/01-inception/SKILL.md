---
name: inception
description: Use this skill for Project Inception and Stakeholder Discovery in the Student Task Management System requirements-engineering assignment. It helps an AI agent analyse the case baseline, identify evidence-backed stakeholders, separate facts from assumptions, define the initial problem, objectives, scope, constraints, risks, and open questions, and prepare raw inception output for later student review without moving into elicitation, specification, prioritisation, validation, or change management.
---

# Skill 01: Project Inception and Stakeholder Discovery

## Purpose

Use this skill to create the first requirements-engineering view of the project:

- problem context
- stakeholder discovery
- high-level business objectives
- preliminary scope
- constraints
- risks and stakeholder tensions
- open questions for later elicitation

This skill does not produce final requirements. It prepares an inception draft that the student must review before it can become part of the reviewed baseline.

## Required Inputs

Read these files before producing any inception output:

- `README.md`
- `CASE.md`
- `CHANGELOG.md`
- `inputs/stakeholder-notes.md`
- `inputs/interview-answers.md`
- `inputs/assumptions.md`

Use source labels exactly:

- `SRC-01` for the assignment case brief and facts derived from it.
- `SRC-02` for the simulated interview record.
- `SRC-03` for the assumption register.
- `ASM-*` for individual assumptions.
- `INT-*` for individual simulated interview answers.
- `OQ-*` for open questions already identified in the case baseline.

## Evidence Rules

Separate every statement into one of these categories:

| Category | Meaning | Allowed wording |
|---|---|---|
| Confirmed case fact | Stated in the assignment case or restated as `CASE-CONFIRMED` interview evidence. | "The case confirms..." |
| Simulated evidence | Recorded in `inputs/interview-answers.md` and labelled as simulation. | "The simulated interview record states..." |
| Assumption | Listed in `inputs/assumptions.md`; even accepted assumptions are not facts. | "Assumption ASM-xx states..." |
| Open question | Missing or unresolved information. | "This remains open..." |
| Derived need | A cautious interpretation from confirmed evidence. | "This suggests a need for..." |

Never present assumptions, inferred stakeholders, potential tensions, or unanswered interview items as confirmed facts.

## Workflow

1. Confirm the task boundary.
   - Work only on inception and stakeholder discovery.
   - Do not continue to Skill 02 elicitation.
   - Do not create functional requirements, user stories, use cases, MoSCoW priorities, validation results, or change requests.

2. Build an evidence inventory.
   - List case-confirmed actors, capabilities, quality concerns, and constraints from `CASE.md`.
   - List simulated interview answers that are `CASE-CONFIRMED`, `PARTIALLY ANSWERED`, or `UNANSWERED`.
   - List assumptions by ID and status without converting them into facts.

3. Identify stakeholders.
   - Include confirmed stakeholders: lecturer, student, administrator.
   - Include inferred stakeholders only if labelled as assumptions, such as university or academic management (`ASM-01`) and IT support or system operator (`ASM-02`).
   - For each stakeholder, record interest, evidence source, and uncertainty.

4. Frame the problem and objectives.
   - State the project problem without prescribing implementation technology.
   - Create high-level objectives only from confirmed case facts or clearly labelled assumptions.
   - Keep measurable targets open unless a student-approved source provides them.

5. Define preliminary scope.
   - Separate "in scope by case evidence" from "out of scope until approved".
   - Use `ASM-07` only as an accepted working boundary, not as permanent rejection.
   - Do not invent integrations, notifications, mobile apps, plagiarism checks, analytics dashboards, or external services.

6. Capture constraints and quality concerns.
   - Include assignment constraints from `CASE.md` and `README.md`.
   - Treat usability, security, performance, reliability, and data integrity as quality areas requiring later measurable definition.
   - Do not assign numeric thresholds unless the student has approved them.

7. Capture risks, tensions, and open questions.
   - Convert unclear areas into open questions rather than decisions.
   - Preserve existing `OQ-*` questions and add new `OQ-DRAFT-*` questions only when necessary.
   - Mark stakeholder tensions as investigation topics, not confirmed conflicts.

8. Ask before deciding.
   - If a policy decision affects scope, security, workflow, grading, file handling, notifications, reporting, integrations, or measurable NFRs, stop and ask the student.
   - Do not silently choose a convenient default.

9. Produce the inception output.
   - If asked to execute the skill, write the first AI version to `outputs/raw/01-inception.md`.
   - Do not write to `outputs/reviewed/01-inception.md` unless the student explicitly asks for reviewed output after reviewing the raw version.
   - In this repository setup task, only edit this skill file and `examples.md`.

## Output Structure

When the skill is executed, use this structure for the raw inception output:

```markdown
# Skill 01 Raw Output: Project Inception and Stakeholder Discovery

## 1. Evidence Summary
## 2. Problem Statement
## 3. Initial Business Objectives
## 4. Stakeholder Discovery
## 5. Preliminary Scope
## 6. Constraints
## 7. Quality Concerns
## 8. Risks and Stakeholder Tensions
## 9. Open Questions for Elicitation
## 10. Student Decisions Needed
## 11. Traceability Notes
```

Each section must cite source IDs or clearly state that the item is unresolved.

## Quality Checks

Before finishing, verify:

- Confirmed case facts cite `SRC-01` or a `CASE-CONFIRMED` `INT-*` entry.
- Simulated answers remain labelled as simulation.
- Every assumption reference keeps its `ASM-*` ID.
- Inferred stakeholders are labelled as assumptions.
- No policy choice is invented for late submissions, resubmission, file limits, grade publication, notifications, authentication, reporting access, retention, performance, availability, backup, recovery, or integrations.
- The output does not contain detailed software requirements, user stories, use cases, priorities, validation results, or change requests.
- The output states which decisions require student approval before later specification.

## Failure Conditions

Stop and ask the student if:

- a requested output requires treating an assumption as fact;
- a missing policy must be chosen before writing the output;
- the user asks for reviewed output before raw output exists and has been reviewed;
- the task moves into Skill 02 or later stages;
- a source file is missing or contradicts another source in a way that affects the inception baseline.

## Related Examples

See `skills/01-inception/examples.md` for sample prompts, expected behavior, and evidence-safe output patterns.
