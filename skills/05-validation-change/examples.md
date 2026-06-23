# Examples for Skill 05: Validation and Change

## Example 1 - Execute Skill 05 without approving new detail

**User prompt**

```text
Use Skill 05 to create raw use-case, validation, and change request outputs.
```

**Expected behavior**

- Read reviewed Skill 01 through Skill 04 outputs first.
- Create only raw Skill 05 outputs, such as `outputs/raw/06-use-case.md`, `outputs/raw/07-validation.md`, and `outputs/raw/08-change-request.md`.
- Validate only reviewed Skill 03 requirements, reviewed Skill 04 user stories, and reviewed Skill 04 prioritisation.
- Keep `DR-*` topics deferred or blocked.
- Do not edit reviewed outputs until the student reviews the raw outputs.

**Acceptable output pattern**

```markdown
| Validation ID | Reviewed item | Check type | Result | Finding | Required action |
|---|---|---|---|---|---|
| VAL-01 | `FR-01`; `US-01` | Traceability | Pass | The story maps to the reviewed assignment creation requirement at a high level. | No action |
| VAL-02 | `FR-04`; `US-04` | Testability | Partial | File submission is supported, but file policy, late submission, resubmission, failure handling, and receipt proof remain open. | Defer detail / student approval needed |
```

## Example 2 - Validate a partial requirement safely

**User prompt**

```text
Validate the student file submission requirement.
```

**Expected behavior**

- Use reviewed `FR-04`, `US-04`, and the priority entry for `FR-04`.
- Confirm that file submission is valid at a high level.
- Mark detailed validation as partial or blocked because unresolved policy remains open.
- Do not invent file type, file size, late-submission, resubmission, retry, or receipt rules.

**Acceptable output pattern**

```markdown
| Validation ID | Reviewed item | Check type | Result | Evidence basis | Finding |
|---|---|---|---|---|---|
| VAL-04 | `FR-04`; `US-04` | Readiness / testability | Partial | `SRC-01`; `INT-S-01`; `OQ-02`; `OQ-03`; `OQ-04`; `OQ-DRAFT-03`; `DR-03` to `DR-07` | Student file submission is case-supported and prioritised as Must, but detailed validation is blocked by unresolved submission policy and receipt evidence. |
```

## Example 3 - Keep NFR candidates not fully testable

**User prompt**

```text
Validate performance and reliability requirements.
```

**Expected behavior**

- Use reviewed `NFR-03` and `NFR-04`.
- Mark both as not fully testable because measurable targets remain open.
- Do not invent response times, availability percentages, backup schedules, recovery targets, capacity numbers, or load profiles.

**Acceptable output pattern**

```markdown
| Validation ID | Reviewed item | Check type | Result | Finding |
|---|---|---|---|---|
| VAL-NFR-03 | `NFR-03` | Testability | Not testable yet | Performance is a reviewed quality concern, but response-time, capacity, throughput, and load targets remain open under `OQ-09` and `DR-16`. |
| VAL-NFR-04 | `NFR-04` | Testability | Not testable yet | Reliability is a reviewed quality concern, but availability, backup, recovery, upload failure, and incident-response details remain open. |
```

## Example 4 - Draft a high-level use-case view without choosing policy

**User prompt**

```text
Write a use case for submitting an assignment.
```

**Expected behavior**

- Derive the use case from `FR-04` and `US-04`.
- Keep the main success scenario high level.
- Put late submission, resubmission, upload failure, file limits, and receipt proof into open extensions or blockers.

**Acceptable output pattern**

```markdown
| Field | Content |
|---|---|
| Use-case ID | `UC-04` |
| Use-case name | Submit assignment file |
| Primary actor | Student |
| Source items | `FR-04`; `US-04` |
| Main success scenario | Student selects an assignment, provides a file for submission, and the system records the submission at a high level. |
| Open extensions or blockers | File policy, late submission, resubmission, upload failure handling, and receipt evidence remain open under `DR-03` to `DR-07`. |
| Validation note | Ready only at high level; detailed flow is partial. |
```

## Example 5 - Document a proposed change without approving it

**User prompt**

```text
Add notifications when deadlines are near.
```

**Expected behavior**

- Do not add notification requirements directly.
- Record a change request candidate if Skill 05 is being executed.
- Mark evidence status as needing approval because notifications remain open under `OQ-05` and `DR-09`.

**Acceptable output pattern**

```markdown
| Change request ID | Request summary | Current baseline affected | Evidence status | Impact analysis | Approval status |
|---|---|---|---|---|---|
| CR-01 | Add deadline reminder notifications. | `DR-09`; `OQ-05`; possibly `FR-05` and `US-05` | Needs student approval / stakeholder evidence | Could affect student monitoring, notification channels, priority, usability, and validation criteria. | Proposed / Needs approval |
```

## Example 6 - Ask before turning an open policy into validation criteria

**User prompt**

```text
Validate that late submissions are accepted for 24 hours.
```

**Expected behavior**

Do not validate the 24-hour rule because late-submission handling remains open.

**Acceptable response pattern**

```text
Late-submission handling is still deferred under `DR-03` and open under `OQ-02`. I can document "accept late submissions for 24 hours" as a proposed change request, but I cannot validate it as baseline behavior unless you approve and update the reviewed requirements first.
```

## Example 7 - Reject final artefacts during Skill 05 design or raw execution

**User prompt**

```text
Use Skill 05 and also finalise the traceability matrix and diagram.
```

**Expected behavior**

Keep Skill 05 limited to high-level use-case views, validation findings, and change request candidates. Do not create final traceability or final diagrams.

**Acceptable response pattern**

```text
Skill 05 can prepare raw use-case, validation, and change request artefacts. Final traceability and final diagrams are later deliverables, so I will keep them out of this step.
```
