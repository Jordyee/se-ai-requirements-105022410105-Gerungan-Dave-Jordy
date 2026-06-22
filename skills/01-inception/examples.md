# Examples for Skill 01: Project Inception and Stakeholder Discovery

## Example 1 - Execute the inception skill

**User prompt**

```text
Use Skill 01 to create the raw project inception output for this repository.
```

**Expected behavior**

- Read the required context files before drafting.
- Create only `outputs/raw/01-inception.md`.
- Do not edit `outputs/reviewed/01-inception.md`.
- Do not continue to elicitation, requirements specification, prioritisation, validation, or change management.
- Label assumptions and simulated evidence explicitly.

**Acceptable output pattern**

```markdown
## Stakeholder Discovery

| Stakeholder | Status | Evidence | Initial interest |
|---|---|---|---|
| Lecturer | Confirmed case stakeholder | SRC-01; INT-L-01 | Create assignments, set deadlines, grade submissions, and provide feedback. |
| Student | Confirmed case stakeholder | SRC-01; INT-S-01 | View assignments, submit files, and monitor status and deadlines. |
| Administrator | Confirmed case stakeholder | SRC-01; INT-A-01 | Manage users, courses, and system configuration. |
| University or academic management | Assumption | ASM-01 | Possible oversight and reporting interest; not confirmed as a daily user. |
```

## Example 2 - Handle an unsupported policy request

**User prompt**

```text
Use Skill 01 and assume students can submit late work for up to 24 hours.
```

**Expected behavior**

Ask the student for approval before using that policy, because late-submission behavior is unresolved.

**Acceptable response pattern**

```text
Late-submission behavior is listed as an unresolved policy decision. Do you want me to record "students can submit late work for up to 24 hours" as a new student-approved assumption, or should it remain an open question for elicitation?
```

## Example 3 - Keep assumptions separate from facts

**User prompt**

```text
Identify all stakeholders for the project.
```

**Expected behavior**

- Confirm lecturer, student, and administrator as case-supported stakeholders.
- Include university or academic management and IT support only as assumed secondary stakeholders.
- Preserve `ASM-01` and `ASM-02`.

**Evidence-safe wording**

```text
The case confirms lecturer, student, and administrator as stakeholders. Assumption ASM-01 adds university or academic management as a secondary stakeholder, and assumption ASM-02 adds IT support or system operator as a secondary stakeholder. These two inferred stakeholders should remain labelled as assumptions until validated.
```

## Example 4 - Avoid premature requirements

**User prompt**

```text
Use Skill 01 to write the login, upload, and grading requirements.
```

**Expected behavior**

Decline the specification part and keep the work at inception level.

**Acceptable response pattern**

```text
Skill 01 can identify security, submission, and grading areas as inception topics, but it should not write detailed software requirements. I can produce a problem statement, stakeholder map, preliminary scope, constraints, risks, and open questions. Detailed requirements belong to the later specification skill.
```

## Example 5 - Student decision needed

**User prompt**

```text
Create the inception output and include performance targets.
```

**Expected behavior**

Do not invent response-time, availability, recovery, or capacity targets. Ask for a student decision or keep them open.

**Acceptable response pattern**

```text
Performance and reliability targets are not provided by the case. Should I leave them as open questions, or do you want to approve specific simulated targets for later use?
```
