# Examples for Skill 03: Specification

## Example 1 - Execute the specification skill safely

**User prompt**

```text
Use Skill 03 to create the raw requirements specification for this repository.
```

**Expected behavior**

- Read the required context files before drafting.
- Create only `outputs/raw/03-requirements.md`.
- Do not edit `outputs/reviewed/03-requirements.md`.
- Do not create user stories, use cases, prioritisation, validation results, or change requests.
- Write only evidence-backed requirements and defer unsupported details.

**Acceptable output pattern**

```markdown
## Functional Requirements

| ID | Requirement statement | Evidence | Status | Notes or boundary |
|---|---|---|---|---|
| FR-01 | The system shall allow lecturers to create assignments. | `SRC-01`; `INT-L-01` | Supported | Mandatory fields remain open under `OQ-01`. |
| FR-02 | The system shall allow students to submit files for assignments. | `SRC-01`; `INT-S-01` | Supported | File type, file size, failure handling, late submission, and resubmission rules remain open under `OQ-02`, `OQ-03`, and `OQ-04`. |
```

## Example 2 - Keep unresolved policies deferred

**User prompt**

```text
Write the submission requirements including late submissions and resubmissions.
```

**Expected behavior**

- Specify only that file submission is in scope.
- Do not decide whether late submissions are blocked, accepted, or marked.
- Do not decide whether resubmission is allowed or whether version history is retained.
- Add deferred topics linked to the open questions.

**Acceptable output pattern**

```markdown
| ID | Deferred topic | Evidence | Reason |
|---|---|---|---|
| DR-01 | Late-submission handling | `OQ-02`; `INT-L-03` | No approved policy states whether late submissions are blocked, accepted, marked, or controlled per assignment. |
| DR-02 | Resubmission and version history | `OQ-03`; `INT-L-04` | No approved policy states whether students may replace submitted files or whether previous versions must be retained. |
```

## Example 3 - Handle a request to invent a policy

**User prompt**

```text
Set late submissions to be accepted for 24 hours and include it in the requirements.
```

**Expected behavior**

Ask for student approval before using that policy as specification evidence.

**Acceptable response pattern**

```text
Late-submission handling is still open under `OQ-02` and `INT-L-03`. Do you want me to record "late submissions are accepted for 24 hours" as a student-approved simulated answer first, or should it remain deferred from Skill 03?
```

## Example 4 - Non-functional requirements without invented targets

**User prompt**

```text
Write performance and reliability requirements.
```

**Expected behavior**

- Include only high-level quality concerns confirmed by the case.
- Do not invent response time, availability, backup, recovery, or capacity targets.
- Mark measurable targets as open.

**Acceptable output pattern**

```markdown
| ID | Requirement statement | Evidence | Status | Notes or boundary |
|---|---|---|---|---|
| NFR-01 | The system shall consider performance for assignment-related workflows. | `SRC-01`; `INT-A-06` | Partial | Measurable response-time and capacity targets remain open under `OQ-09`. |
| NFR-02 | The system shall consider reliability for assignment submission and record access. | `SRC-01`; `INT-A-06` | Partial | Availability, backup, and recovery targets remain open under `OQ-09`. |
```

## Example 5 - Refuse later-stage artefacts

**User prompt**

```text
Use Skill 03 to write requirements, user stories, use cases, priorities, and validation criteria.
```

**Expected behavior**

Keep Skill 03 limited to requirements specification and explain that later artefacts belong to later skills or later approved work.

**Acceptable response pattern**

```text
Skill 03 can draft traceable functional and non-functional requirements plus deferred topics. It should not produce user stories, use cases, prioritisation, validation results, or change requests in this step.
```

## Example 6 - Assumption-labelled requirement candidate

**User prompt**

```text
Use the IT support assumption to specify backup requirements.
```

**Expected behavior**

Do not turn `ASM-02` into a confirmed operational requirement. Ask for approval or keep the item assumption-labelled and incomplete.

**Acceptable response pattern**

```text
`ASM-02` identifies IT support or system operator as an assumed stakeholder, but it does not define backup targets. Should backup requirements stay open under `OQ-09`, or do you want to approve a simulated target before Skill 03 uses it?
```
