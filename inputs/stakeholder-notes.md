# Stakeholder Notes

## Document Purpose

These notes are the initial stakeholder evidence available before elicitation. They are derived from the assignment brief, not from real interviews. Inferred stakeholders and interpretations are labelled explicitly.

## Source Register

| Source ID | Source | Reliability | Notes |
|---|---|---|---|
| SRC-01 | AI-Assisted Requirements Engineering assignment brief | Primary case source | Defines actors, core capabilities, quality concerns, deliverables, and AI-use rules. |
| SRC-02 | Simulated interview record in `inputs/interview-answers.md` | Educational simulation | May be used only with its simulation label; unanswered matters remain open questions. |
| SRC-03 | Assumption register in `inputs/assumptions.md` | Unvalidated working input | Must never be represented as confirmed stakeholder fact. |

## Stakeholder Notes

### STK-01 — Lecturer

**Evidence from SRC-01**

- Creates assignments.
- Sets deadlines.
- Provides grades and feedback.

**Initial needs derived directly from the evidence**

- A way to define and publish assignment information.
- A way to identify student submissions.
- A way to record grades and feedback.

**Information not yet known**

- Mandatory assignment fields.
- Late-submission policy.
- Resubmission policy.
- Grade publication and revision rules.
- Required reports.

### STK-02 — Student

**Evidence from SRC-01**

- Views assignments.
- Submits files.
- Monitors assignment status and deadlines.

**Initial needs derived directly from the evidence**

- Clear access to applicable assignments and deadlines.
- A reliable file-submission mechanism.
- Confirmation of submission status.

**Information not yet known**

- Accepted file formats and limits.
- Whether submission replacement is permitted.
- Notification preferences.
- Expected handling of failed uploads.

### STK-03 — Administrator

**Evidence from SRC-01**

- Manages users.
- Manages courses.
- Manages system configuration.

**Initial needs derived directly from the evidence**

- Controlled management of users and roles.
- Valid course data.
- Manageable configuration.

**Information not yet known**

- Authentication mechanism.
- Role-assignment policy.
- Audit requirements.
- Integration with existing campus data.

### STK-04 — University or Academic Management

**Status:** `ASSUMPTION` — inferred secondary stakeholder.

Potential interests include academic-policy compliance, reporting, and reliable academic records. No direct statement from this stakeholder is available.

### STK-05 — IT Support or System Operator

**Status:** `ASSUMPTION` — inferred secondary stakeholder.

Potential interests include system availability, security, backup, recovery, monitoring, and supportability. No direct statement from this stakeholder is available.

## Potential Stakeholder Tensions

The following are investigation topics, not confirmed conflicts:

- Students may prefer flexible resubmission, while lecturers may require a controlled final submission.
- Lecturers may prefer flexible grading changes, while academic management may require an audit trail.
- Users may prefer convenience, while administrators and IT support require stronger security controls.
- Detailed reporting may conflict with privacy and least-privilege access.

## Evidence Handling Rules

- Cite `SRC-01` for facts stated by the assignment.
- Cite a specific interview response ID for simulated elicitation evidence.
- Cite an `ASM-*` ID when using an assumption.
- Do not convert potential needs, tensions, or inferred stakeholders into requirements without review.
