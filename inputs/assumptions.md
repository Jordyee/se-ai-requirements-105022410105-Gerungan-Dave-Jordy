# Assumption Register

## Usage Rules

- An assumption is not a confirmed fact.
- Every assumption must keep its `ASM-*` identifier when referenced.
- AI output must label assumptions explicitly.
- Assumptions affecting scope, policy, security, or measurable NFRs require student approval before entering the reviewed baseline.

## Review Record

- **Reviewed by:** Gerungan Dave Jordy
- **Review date:** 22 June 2026
- **Review outcome:** ASM-01, ASM-02, ASM-04, ASM-05, and ASM-06 are accepted as working assumptions. ASM-03 is revised to avoid overclaiming account-role behaviour. ASM-07 and ASM-08 are retained as approved working boundaries/rules.

## Current Assumptions

| ID | Assumption | Reason | Risk if incorrect | Validation owner | Status |
|---|---|---|---|---|---|
| ASM-01 | University or academic management is a secondary stakeholder. | Academic management may need oversight or summary information about assignment activities, but is not expected to perform daily workflows such as creating assignments, submitting work, or grading submissions. | Missing or incorrect approval, oversight, and reporting requirements. | Student / lecturer | Accepted |
| ASM-02 | IT support or a system operator is a secondary stakeholder. | Security, availability, backup, and recovery require an operational owner. | NFRs may lack an accountable stakeholder. | Student / lecturer | Accepted |
| ASM-03 | The system distinguishes at least three user roles: lecturer, student, and administrator. It is not yet confirmed whether one account may hold more than one role. | The case defines different capabilities for three actor types, but does not confirm detailed account-role rules. | Access-control requirements may be modelled too narrowly or too broadly. | Administrator | Revised |
| ASM-04 | Assignment and submission records require stable identifiers. | Traceability and reliable record management need unambiguous references. | Duplicate or incorrectly associated records. | Administrator / lecturer | Accepted |
| ASM-05 | The system records timestamps for deadlines and submissions. | Deadline and submission-status monitoring depend on time data. | Late/on-time status cannot be determined consistently. | Lecturer / administrator | Accepted |
| ASM-06 | Only authorised users may view or modify grades and submissions. | The case explicitly requires security and academic data integrity. | Privacy breach or unauthorised academic-record changes. | Administrator / management | Accepted |
| ASM-07 | The initial project excludes chat, plagiarism detection, payment, attendance, and video conferencing. | None are stated in the case. | Needed capabilities could be omitted if stakeholders later request them. | Student / lecturer | Accepted working scope boundary |
| ASM-08 | The application will be described independently of a specific implementation technology during requirements engineering. | No architecture or platform is provided. | Premature design constraints could distort requirements. | Student | Accepted working rule |

## Unresolved Policy Decisions

These are not assumptions yet and must remain open:

- Late-submission behavior.
- Resubmission and version-history behavior.
- Allowed file types and maximum file size.
- Grade publication and correction rules.
- Notification channels.
- Authentication mechanism.
- Reporting contents and access rights.
- Data retention, backup, and recovery targets.
- Performance and availability targets.
- External system integrations.

## Change Procedure

When an assumption is reviewed:

1. Record the evidence or decision source.
2. Change its status to `Accepted`, `Rejected`, or `Revised`.
3. Record the date and reviewer.
4. Update affected artefacts and traceability links.
5. Record material changes in `CHANGELOG.md`.
