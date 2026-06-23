# Cross-Case Test Fixture: Library Book Borrowing System

## Purpose

This fixture is used only to test whether Skill 01 and Skill 02 can generalise to a different requirements-engineering case. It is not part of the Student Task Management System reviewed baseline.

## Source Mapping for Skill Tests

| Skill source label | Test fixture source |
|---|---|
| `SRC-01` | Library borrowing case brief below. |
| `SRC-02` | Simulated interview notes below. |
| `SRC-03` | Test assumption register below. |

## Library Borrowing Case Brief

A campus library needs a system to help manage physical book borrowing. Library members should be able to search or view available books, reserve books, borrow available books, return borrowed books, and monitor their current loan status. Librarians should be able to manage the book catalogue and record borrowing and returns. Administrators should be able to manage member accounts, librarian accounts, and system configuration.

The system should consider usability, security, performance, reliability, and data integrity. The case does not specify implementation technology, authentication mechanism, loan duration, renewal rules, overdue policy, notification channels, fine/payment handling, reporting detail, external integrations, or measurable non-functional targets.

## Simulated Interview Notes

No real stakeholder interview was conducted. These notes are an educational simulation based only on the test case brief.

| Response ID | Stakeholder | Question | Recorded answer | Status |
|---|---|---|---|---|
| LIB-INT-M-01 | Member | What activities must library members perform? | Members search or view books, reserve books, borrow books, return books, and monitor loan status. | CASE-CONFIRMED |
| LIB-INT-M-02 | Member | Should members receive due-date reminders? | The case does not define notification behavior. | UNANSWERED |
| LIB-INT-M-03 | Member | Can members renew a borrowed book? | Renewal rules are not provided. | UNANSWERED |
| LIB-INT-L-01 | Librarian | What activities must librarians perform? | Librarians manage the catalogue and record borrowing and returns. | CASE-CONFIRMED |
| LIB-INT-L-02 | Librarian | What book metadata is mandatory? | The case confirms catalogue management but does not define required metadata. | PARTIALLY ANSWERED |
| LIB-INT-L-03 | Librarian | What should happen when a book is overdue? | Overdue policy is not provided. | UNANSWERED |
| LIB-INT-A-01 | Administrator | What activities must administrators perform? | Administrators manage member accounts, librarian accounts, and system configuration. | CASE-CONFIRMED |
| LIB-INT-A-02 | Administrator | How are users authenticated? | Authentication mechanism is not provided. | UNANSWERED |
| LIB-INT-A-03 | Administrator | What quality concerns matter? | Usability, security, performance, reliability, and data integrity must be considered. | CASE-CONFIRMED |

## Test Assumption Register

| ID | Assumption | Status | Boundary |
|---|---|---|---|
| LIB-ASM-01 | Library management may be a secondary stakeholder for policy and reporting oversight. | Working assumption | Does not define reports, policies, or approval authority. |
| LIB-ASM-02 | IT support or a system operator may be a secondary stakeholder for availability, security, backup, and recovery. | Working assumption | Does not define measurable NFR targets. |
| LIB-ASM-03 | Books, members, reservations, and loans require stable identifiers. | Working assumption | Does not define identifier format or database design. |
| LIB-ASM-04 | Borrowing and return events require timestamps. | Working assumption | Does not define due-date or overdue rules. |
| LIB-ASM-05 | Online fine payment, e-book lending, and mobile apps are outside the test baseline unless later approved. | Working scope boundary | Exclusions can change only through later evidence or approval. |

## Open Questions for Testing

| ID | Question |
|---|---|
| LIB-OQ-01 | What book metadata is mandatory in the catalogue? |
| LIB-OQ-02 | What loan duration and due-date rules apply? |
| LIB-OQ-03 | Are renewals allowed, and under what conditions? |
| LIB-OQ-04 | How should overdue books be handled? |
| LIB-OQ-05 | Are reservation queues required when multiple members want the same book? |
| LIB-OQ-06 | Should members receive notifications, and through which channels? |
| LIB-OQ-07 | What authentication and role-assignment rules apply? |
| LIB-OQ-08 | What reports are required and who may access them? |
| LIB-OQ-09 | What response-time, availability, backup, and recovery targets apply? |
| LIB-OQ-10 | Should the system integrate with an existing campus identity or library catalogue system? |
