# Examples for Skill 02: Elicitation

## Example 1 - Execute the elicitation skill

**User prompt**

```text
Use Skill 02 to create the raw elicitation output for this repository.
```

**Expected behavior**

- Read the required context files before drafting.
- Create only `outputs/raw/02-elicitation.md`.
- Do not edit `outputs/reviewed/02-elicitation.md`.
- Do not create final requirements, user stories, use cases, priorities, validation results, or change requests.
- Build an elicitation plan, stakeholder question guide, interview-answer classification, and evidence capture template.

**Acceptable output pattern**

```markdown
## Stakeholder Coverage Map

| Stakeholder | Status | Elicitation focus | Evidence link |
|---|---|---|---|
| Lecturer | Confirmed case stakeholder | Assignment fields, late submission, resubmission, grade publication, and reports. | `SRC-01`; `INT-L-02`; `INT-L-03`; `OQ-01`; `OQ-02`; `OQ-03`; `OQ-06`; `OQ-07` |
| Student | Confirmed case stakeholder | Submission confirmation, file limits, upload failure handling, notifications, and feedback visibility. | `SRC-01`; `INT-S-02`; `INT-S-03`; `INT-S-04`; `INT-S-05`; `INT-S-06`; `OQ-04`; `OQ-05` |
| IT support or system operator | Assumed secondary stakeholder | Authentication, availability, backup, recovery, and measurable NFRs. | `ASM-02`; `OQ-08`; `OQ-09`; `OQ-11` |
```

## Example 2 - Write neutral elicitation questions

**User prompt**

```text
Make interview questions about late submissions and resubmissions.
```

**Expected behavior**

- Ask neutral questions.
- Do not decide the policy.
- Link questions to open question IDs.

**Acceptable output pattern**

```markdown
| Question ID | Stakeholder | Question | Related open question |
|---|---|---|---|
| ELQ-L-03 | Lecturer | How should the system treat a submission received after the deadline? | `OQ-02` |
| ELQ-L-04 | Lecturer | Should students be allowed to replace a submitted file before the deadline? If yes, what previous submission evidence must be retained? | `OQ-03` |
| ELQ-S-03 | Student | What information would help you know whether your submitted file was accepted successfully? | `OQ-DRAFT-03` |
```

## Example 3 - Handle a request to invent stakeholder answers

**User prompt**

```text
Assume late submissions are accepted for 24 hours and write the elicitation result.
```

**Expected behavior**

Ask for student approval before recording the policy, because late-submission behavior is unresolved.

**Acceptable response pattern**

```text
Late-submission behavior is unresolved in `INT-L-03` and `OQ-02`. Do you want me to record "late submissions are accepted for 24 hours" as a student-approved simulated answer, keep it as an assumption, or leave it open for elicitation?
```

## Example 4 - Classify existing simulated answers

**User prompt**

```text
Summarize which interview answers are ready for specification.
```

**Expected behavior**

- Identify case-confirmed answers as evidence.
- Identify partial answers as incomplete.
- Keep unanswered items unresolved.
- Avoid writing requirements.

**Acceptable output pattern**

```markdown
| Response ID | Status | Skill 02 classification | Remaining gap |
|---|---|---|---|
| INT-L-01 | CASE-CONFIRMED | Can support later lecturer workflow topics because it restates `SRC-01`. | Detailed assignment fields and policies remain open. |
| INT-L-05 | PARTIALLY ANSWERED | Confirms grading and feedback are in scope, but not publication timing. | Publication, visibility, and correction rules. |
| INT-S-03 | UNANSWERED | Not ready for specification. | File type and maximum file size policy. |
```

## Example 5 - Refuse premature requirements

**User prompt**

```text
Use Skill 02 and turn the answers into functional requirements.
```

**Expected behavior**

Decline the specification part and keep the work at elicitation level.

**Acceptable response pattern**

```text
Skill 02 can classify elicitation evidence and identify which questions are answered, partially answered, or still open. It should not write functional requirements. I can prepare the elicitation plan and evidence table now; functional requirements belong to Skill 03 after review.
```

## Example 6 - Record a new answer safely

**User prompt**

```text
Record this simulated lecturer answer: lecturers can edit grades until they publish them.
```

**Expected behavior**

Ask whether the answer is student-approved simulated evidence before treating it as usable input.

**Acceptable response pattern**

```text
This is a new simulated policy answer, not a case fact. Should I record it as a student-approved simulated `INT-*` answer with today's date and reviewer name, or keep grade-editing rules open under `OQ-06`?
```
