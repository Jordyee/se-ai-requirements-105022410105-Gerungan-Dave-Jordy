# Cross-Case Test Output: Skill 01 Inception

## Test Status

| Field | Value |
|---|---|
| Skill tested | `skills/01-inception/SKILL.md` |
| Test fixture | `evaluation/cross-case-library-borrowing-case.md` |
| Test case | Library Book Borrowing System |
| Purpose | Check whether the inception workflow can work on a different case without creating premature requirements. |
| Boundary | This is test evidence only. It is not part of the Student Task Management System reviewed baseline. |

## 1. Evidence Summary

| Source | Role in test output | Use rule |
|---|---|---|
| `SRC-01` | Library borrowing case brief from the test fixture. | Use as confirmed test-case evidence. |
| `SRC-02` | Simulated interview notes from the test fixture. | Use only with simulation labels and response status. |
| `SRC-03` | Test assumption register from the test fixture. | Use only as labelled assumptions. |

Confirmed test-case facts:

- Members search or view available books, reserve books, borrow books, return books, and monitor current loan status (`SRC-01`; `LIB-INT-M-01`).
- Librarians manage the book catalogue and record borrowing and returns (`SRC-01`; `LIB-INT-L-01`).
- Administrators manage member accounts, librarian accounts, and system configuration (`SRC-01`; `LIB-INT-A-01`).
- Usability, security, performance, reliability, and data integrity must be considered (`SRC-01`; `LIB-INT-A-03`).

## 2. Problem Statement

The campus library needs a consistent way to manage physical book borrowing activities across members, librarians, and administrators. The case confirms the need to support book discovery, reservations, borrowing, returns, loan-status monitoring, catalogue management, account management, and system configuration (`SRC-01`).

The case does not provide implementation technology, authentication mechanism, due-date policy, renewal policy, overdue handling, notification channels, fine/payment handling, reporting detail, integrations, or measurable quality targets. These must remain open unless later evidence or student approval exists.

## 3. Initial Business Objectives

| ID | Objective | Evidence | Status |
|---|---|---|---|
| LIB-OBJ-01 | Enable members to search or view available books. | `SRC-01`; `LIB-INT-M-01` | Confirmed by test case |
| LIB-OBJ-02 | Enable members to reserve, borrow, return, and monitor books. | `SRC-01`; `LIB-INT-M-01` | Confirmed by test case |
| LIB-OBJ-03 | Enable librarians to manage the catalogue and record borrowing and returns. | `SRC-01`; `LIB-INT-L-01` | Confirmed by test case |
| LIB-OBJ-04 | Enable administrators to manage accounts and configuration. | `SRC-01`; `LIB-INT-A-01` | Confirmed by test case |
| LIB-OBJ-05 | Consider usability, security, performance, reliability, and data integrity. | `SRC-01`; `LIB-INT-A-03` | Confirmed at quality-area level; measurable targets remain open |

## 4. Stakeholder Discovery

| Stakeholder | Status | Evidence | Initial interest | Uncertainty |
|---|---|---|---|---|
| Member | Confirmed test-case stakeholder | `SRC-01`; `LIB-INT-M-01` | Search/view books, reserve books, borrow and return books, and monitor current loans. | Renewal, overdue, reservation queue, notification, and account access details remain undefined. |
| Librarian | Confirmed test-case stakeholder | `SRC-01`; `LIB-INT-L-01` | Manage catalogue entries and record borrowing/return activities. | Mandatory book metadata, overdue handling, correction rules, and reporting detail remain undefined. |
| Administrator | Confirmed test-case stakeholder | `SRC-01`; `LIB-INT-A-01` | Manage member accounts, librarian accounts, and system configuration. | Authentication, role assignment, audit, retention, and integrations remain undefined. |
| Library management | Assumed secondary stakeholder | `LIB-ASM-01` | Possible policy and reporting oversight. | No direct stakeholder statement is available. |
| IT support or system operator | Assumed secondary stakeholder | `LIB-ASM-02` | Possible availability, backup, recovery, and security ownership. | No direct stakeholder statement or measurable target is available. |

## 5. Preliminary Scope

### In scope by test-case evidence

- Member book search or viewing (`SRC-01`; `LIB-INT-M-01`).
- Member reservation, borrowing, return, and loan-status monitoring (`SRC-01`; `LIB-INT-M-01`).
- Librarian catalogue management (`SRC-01`; `LIB-INT-L-01`).
- Librarian borrowing and return recording (`SRC-01`; `LIB-INT-L-01`).
- Administrator member, librarian account, and configuration management (`SRC-01`; `LIB-INT-A-01`).
- Consideration of usability, security, performance, reliability, and data integrity (`SRC-01`; `LIB-INT-A-03`).

### Out of scope until approved

- Online fine payment (`LIB-ASM-05`).
- E-book lending (`LIB-ASM-05`).
- Native mobile applications (`LIB-ASM-05`).
- External identity, catalogue, or library-management integrations (`LIB-OQ-10`).
- Notification channels and reminder behavior (`LIB-OQ-06`).
- Reporting detail and access rules (`LIB-OQ-08`).

## 6. Constraints

| ID | Constraint | Evidence | Status |
|---|---|---|---|
| LIB-CON-01 | Facts, simulated notes, assumptions, and open questions must remain distinguishable. | Test fixture purpose and source mapping | Test evidence rule |
| LIB-CON-02 | Implementation technology is not provided. | `SRC-01` | Known information gap |
| LIB-CON-03 | Fine/payment handling, e-book lending, and mobile apps are excluded unless later approved. | `LIB-ASM-05` | Working scope boundary |
| LIB-CON-04 | The system distinguishes member, librarian, and administrator responsibilities at a high level. | `SRC-01` | Confirmed at role-capability level; account-role behavior remains open |

## 7. Quality Concerns

| Quality area | Confirmed concern | Open measurement question |
|---|---|---|
| Usability | Members, librarians, and administrators need usable borrowing workflows. | What task-completion criteria or usability expectations apply? |
| Security | Account and borrowing data need role-appropriate protection. | What authentication, authorisation, audit, and role-assignment policies apply? |
| Performance | Book search, reservation, borrowing, return, and administration workflows should be responsive. | What response-time and capacity targets apply? |
| Reliability | Borrowing and return records should be dependable. | What availability, backup, recovery, and incident targets apply? |
| Data integrity | Book, member, reservation, loan, and return records need consistency. | What identifier, timestamp, correction, and retention rules apply? |

## 8. Risks and Stakeholder Tensions

| ID | Risk or tension | Evidence | Why it matters |
|---|---|---|---|
| LIB-RISK-01 | Loan duration and due-date rules are unknown. | `LIB-OQ-02` | Affects borrowing, loan status, and overdue handling. |
| LIB-RISK-02 | Renewal and reservation queue rules are unknown. | `LIB-OQ-03`; `LIB-OQ-05` | Affects member expectations and catalogue availability. |
| LIB-RISK-03 | Overdue handling and fine/payment scope are unclear. | `LIB-OQ-04`; `LIB-ASM-05` | Could incorrectly add payment or policy requirements. |
| LIB-RISK-04 | Authentication, role assignment, and integrations are unknown. | `LIB-OQ-07`; `LIB-OQ-10` | Affects security and system boundary. |
| LIB-RISK-05 | Measurable quality targets are unknown. | `LIB-OQ-09` | Prevents fully testable NFRs. |

## 9. Open Questions for Elicitation

The cross-case output retained the test fixture's `LIB-OQ-01` through `LIB-OQ-10` open questions. No open question was converted into a requirement or policy.

## 10. Student Decisions Needed

Before a later specification step, the student would need to decide whether to:

1. keep policy areas open and write only high-level requirements;
2. approve simulated evidence for renewal, overdue handling, notifications, authentication, reporting, integrations, or measurable NFR targets;
3. keep online fine payment, e-book lending, and mobile apps outside the baseline.

## 11. Traceability Notes

- Test-case facts trace to `SRC-01` and case-confirmed simulated notes such as `LIB-INT-M-01`, `LIB-INT-L-01`, `LIB-INT-A-01`, and `LIB-INT-A-03`.
- Assumptions retain `LIB-ASM-*` labels.
- Open questions retain `LIB-OQ-*` labels.
- This output does not create functional requirements, user stories, use cases, priorities, validation results, or change requests.
