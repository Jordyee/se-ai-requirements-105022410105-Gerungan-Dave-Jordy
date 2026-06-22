# AI-Assisted Requirements Engineering Assignment

## Student Information

- **Name:** Gerungan Dave Jordy
- **Student ID:** 105022410105
- **Class:** Summer Class 2026
- **Course:** Software Engineering
- **Lecturer:** Andrew Tanny Liem

## Project

**Student Task Management System**

This repository demonstrates a traceable requirements-engineering workflow supported by reusable AI skills. AI produces drafts, while the student reviews evidence, approves assumptions, corrects errors, and owns the final requirements baseline.

## Assignment Objective

- Apply inception, elicitation, elaboration, specification, negotiation, prioritisation, validation, and change management.
- Design five reusable AI skills with explicit inputs, workflow, outputs, rules, quality checks, and failure conditions.
- Preserve raw AI output separately from student-reviewed output.
- Maintain traceability from stakeholder evidence to requirements and related artefacts.
- Test and improve at least two skills on a different case.

## Current Status

The repository structure and pre-skill context documents are prepared. Skill 01, Skill 02, and Skill 03 have been designed, executed, reviewed, and recorded in the evidence trail. Skills 04 and 05 remain pending until each workflow stage is deliberately implemented and executed.

## Case and Inputs

- [Case Study](CASE.md)
- [Stakeholder Notes](inputs/stakeholder-notes.md)
- [Simulated Interview Answers](inputs/interview-answers.md)
- [Assumption Register](inputs/assumptions.md)

## Skills

1. [Inception Skill](skills/01-inception/SKILL.md)
2. [Elicitation Skill](skills/02-elicitation/SKILL.md)
3. [Specification Skill](skills/03-specification/SKILL.md)
4. [Prioritisation Skill](skills/04-prioritization/SKILL.md)
5. [Validation and Change Skill](skills/05-validation-change/SKILL.md)

## Final Outputs

- [01 — Inception](outputs/reviewed/01-inception.md)
- [02 — Elicitation](outputs/reviewed/02-elicitation.md)
- [03 — Requirements](outputs/reviewed/03-requirements.md)
- [04 — User Stories](outputs/reviewed/04-user-stories.md)
- [05 — Prioritisation](outputs/reviewed/05-prioritization.md)
- [06 — Use Cases](outputs/reviewed/06-use-case.md)
- [07 — Validation](outputs/reviewed/07-validation.md)
- [08 — Change Request](outputs/reviewed/08-change-request.md)
- [Requirements Traceability](outputs/reviewed/requirements-traceability.md)
- [Use Case Diagram](diagrams/use-case-diagram.png)

> Skill 01, Skill 02, and Skill 03 have reviewed outputs. The remaining reviewed output links point to placeholders and will be completed only after the corresponding skill is executed and reviewed.

## Evaluation Evidence

- [Skill Test Results](evaluation/skill-test-results.md)
- [AI Output Review](evaluation/ai-output-review.md)
- [Reflection](evaluation/reflection.md)
- [Changelog](CHANGELOG.md)

## AI Usage

- **AI tool used for repository preparation:** OpenAI Codex
- **Model:** GPT-5
- **Preparation date:** 22 June 2026
- **Skills executed on the main case:** Skill 01, Skill 02, Skill 03
- **Cross-case skill tests:** None yet
- **Current human-review note:** The student must review and approve simulated inputs, assumptions, measurable targets, raw outputs, and all final requirements.

## Evidence Policy

- Files in `outputs/raw/` must preserve the first AI output without editing.
- Corrections and their rationale must be recorded in `evaluation/ai-output-review.md`.
- Final artefacts belong in `outputs/reviewed/`.
- Case facts, simulated answers, assumptions, and open questions must remain distinguishable.
- No unsupported feature may enter the reviewed baseline without evidence or an approved assumption.

## Submission Reminder

Before submission, complete the class field, verify every link, publish the required GitHub issues, retain at least eight meaningful commits, and confirm that the repository is publicly accessible unless GitHub Classroom is used.
