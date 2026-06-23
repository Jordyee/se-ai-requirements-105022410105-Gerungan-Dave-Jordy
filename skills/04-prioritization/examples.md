# Examples for Skill 04: User Story Derivation and Prioritisation

## Example 1 - Execute Skill 04 without inventing policy

**User prompt**

```text
Use Skill 04 to create raw user stories and prioritisation for this repository.
```

**Expected behavior**

- Read reviewed Skill 01, Skill 02, and Skill 03 outputs first.
- Create only raw Skill 04 outputs, such as `outputs/raw/04-user-stories.md` and `outputs/raw/05-prioritization.md`.
- Derive stories only from existing `FR-*`, `NFR-*`, and `CON-SPEC-*` items in reviewed Skill 03.
- Keep `DR-*` topics deferred or blocked.
- Do not edit reviewed outputs until the student reviews the raw outputs.

**Acceptable output pattern**

```markdown
| Story ID | User story | Source requirement | Readiness | Boundary |
|---|---|---|---|---|
| US-01 | As a lecturer, I want to create assignments, so that coursework tasks can be defined for students. | `FR-01` | Ready at high level | Mandatory fields and validation remain open under `OQ-01`. |
| US-02 | As a student, I want to submit files for assignments, so that I can provide coursework work through the system. | `FR-04` | Ready at high level with partial detail | File policy, late submission, resubmission, upload failure, and receipt proof remain open. |
```

## Example 2 - Prioritise a partial requirement safely

**User prompt**

```text
Prioritise the file submission requirement.
```

**Expected behavior**

- Use reviewed `FR-04`.
- Show stakeholder value and centrality.
- Preserve partial readiness because file limits, late submission, resubmission, failure handling, and receipt evidence remain open.
- Do not decide the missing policies.

**Acceptable output pattern**

```markdown
| Requirement | MoSCoW | Value | Risk/readiness | Rationale |
|---|---|---|---|---|
| `FR-04` Student file submission | Must | High | High risk / partial detail | The case confirms student file submission through `SRC-01` and `INT-S-01`, but `OQ-02`, `OQ-03`, `OQ-04`, and `OQ-DRAFT-03` still block detailed rules. |
```

## Example 3 - Keep deferred topics out of approved priorities

**User prompt**

```text
Make late submissions a Must requirement.
```

**Expected behavior**

Do not turn late-submission handling into an approved requirement. It remains deferred under Skill 03.

**Acceptable response pattern**

```text
Late-submission handling is deferred as `DR-03` and remains open under `OQ-02` and `INT-L-03`. I can list it as a high-risk decision needed, but I cannot prioritise it as an approved requirement unless the reviewed requirements baseline is updated first.
```

## Example 4 - Avoid invented acceptance criteria

**User prompt**

```text
Write user stories with acceptance criteria for submissions, including allowed PDF files up to 10 MB.
```

**Expected behavior**

- Derive the submission story from `FR-04`.
- Do not add PDF or 10 MB because file type and size limits remain open.
- Ask whether the proposed file policy should be approved through the earlier evidence workflow.

**Acceptable response pattern**

```text
`FR-04` supports a high-level submission story, but file type and size limits remain open under `OQ-04`. Should "PDF files up to 10 MB" be recorded first as a student-approved simulated policy, or should the story keep file limits deferred?
```

## Example 5 - Prioritise NFR candidates without measurable targets

**User prompt**

```text
Prioritise performance and reliability.
```

**Expected behavior**

- Use `NFR-03` and `NFR-04` from reviewed Skill 03.
- Mark both as partial because measurable targets remain open.
- Do not invent response times, availability percentages, backup schedules, or recovery targets.

**Acceptable output pattern**

```markdown
| Requirement | MoSCoW | Value | Risk/readiness | Rationale |
|---|---|---|---|---|
| `NFR-03` Performance quality concern | Should | Medium | High risk / not measurable | The case confirms performance as a quality area, but response-time, capacity, and load targets remain open under `OQ-09`. |
| `NFR-04` Reliability quality concern | Should | Medium | High risk / not measurable | The case confirms reliability as a quality area, but availability, backup, recovery, and failure-handling targets remain open under `OQ-04` and `OQ-09`. |
```

## Example 6 - Refuse use cases during Skill 04

**User prompt**

```text
Use Skill 04 to write user stories, priorities, use cases, validation results, and change requests.
```

**Expected behavior**

Keep Skill 04 limited to user-story derivation and prioritisation. Do not create later artefacts.

**Acceptable response pattern**

```text
Skill 04 can derive traceable user-story candidates and prioritise reviewed requirements. Use cases, validation results, and change requests belong to later approved work, so I will not create them in this step.
```
