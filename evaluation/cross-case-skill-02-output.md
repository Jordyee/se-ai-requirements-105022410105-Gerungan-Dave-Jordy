# Cross-Case Test Output: Skill 02 Elicitation

## Test Status

| Field | Value |
|---|---|
| Skill tested | `skills/02-elicitation/SKILL.md` |
| Test fixture | `evaluation/cross-case-library-borrowing-case.md` |
| Prior test output | `evaluation/cross-case-skill-01-output.md` |
| Test case | Library Book Borrowing System |
| Purpose | Check whether the elicitation workflow can plan questions for a different case without writing requirements. |
| Boundary | This is test evidence only. It is not part of the Student Task Management System reviewed baseline. |

## 1. Review Status and Boundary

The test uses the Library Book Borrowing System fixture and the Skill 01 cross-case output as a reviewed-style inception baseline for testing. The output remains an elicitation plan and evidence-capture draft. It does not approve policies, requirements, user stories, use cases, priorities, validation results, or change requests.

## 2. Inputs and Evidence Sources

| Source | Use in this test output |
|---|---|
| `evaluation/cross-case-library-borrowing-case.md` | Test fixture containing case brief, simulated interview notes, assumptions, and open questions. |
| `evaluation/cross-case-skill-01-output.md` | Cross-case inception output used as the prerequisite baseline. |
| `skills/02-elicitation/SKILL.md` | Elicitation workflow under test. |

## 3. Elicitation Objectives

| ID | Objective | Evidence basis | Status |
|---|---|---|---|
| LIB-ELO-01 | Clarify member workflow details for searching/viewing books, reserving, borrowing, returning, and monitoring loan status. | `SRC-01`; `LIB-INT-M-01`; `LIB-OQ-02` to `LIB-OQ-06` | Needs stakeholder answers |
| LIB-ELO-02 | Clarify librarian workflow details for catalogue management and borrowing/return recording. | `SRC-01`; `LIB-INT-L-01`; `LIB-INT-L-02`; `LIB-INT-L-03`; `LIB-OQ-01`; `LIB-OQ-04`; `LIB-OQ-08` | Needs stakeholder answers |
| LIB-ELO-03 | Clarify administrator responsibilities for accounts, configuration, authentication, roles, and integrations. | `SRC-01`; `LIB-INT-A-01`; `LIB-INT-A-02`; `LIB-OQ-07`; `LIB-OQ-10` | Needs stakeholder answers |
| LIB-ELO-04 | Clarify assumed secondary stakeholder concerns without treating them as confirmed primary actor facts. | `LIB-ASM-01`; `LIB-ASM-02`; `LIB-OQ-08`; `LIB-OQ-09`; `LIB-OQ-10` | Requires validation or student approval |

## 4. Stakeholder Coverage Map

| Stakeholder | Status | Elicitation focus | Evidence link |
|---|---|---|---|
| Member | Confirmed test-case stakeholder | Book discovery, reservations, borrowing, returns, loan status, renewals, overdue visibility, and notifications. | `SRC-01`; `LIB-INT-M-01`; `LIB-INT-M-02`; `LIB-INT-M-03`; `LIB-OQ-02` to `LIB-OQ-06` |
| Librarian | Confirmed test-case stakeholder | Catalogue metadata, borrowing and return recording, overdue handling, corrections, and reporting needs. | `SRC-01`; `LIB-INT-L-01`; `LIB-INT-L-02`; `LIB-INT-L-03`; `LIB-OQ-01`; `LIB-OQ-04`; `LIB-OQ-08` |
| Administrator | Confirmed test-case stakeholder | Member accounts, librarian accounts, system configuration, authentication, roles, and integrations. | `SRC-01`; `LIB-INT-A-01`; `LIB-INT-A-02`; `LIB-OQ-07`; `LIB-OQ-10` |
| Library management | Assumed secondary stakeholder | Borrowing policy, overdue policy, reporting, and oversight. | `LIB-ASM-01`; `LIB-OQ-04`; `LIB-OQ-08` |
| IT support or system operator | Assumed secondary stakeholder | Availability, security, backup, recovery, and integration constraints. | `LIB-ASM-02`; `LIB-OQ-07`; `LIB-OQ-09`; `LIB-OQ-10` |

## 5. Question Guide by Stakeholder

### Member Questions

| Question ID | Related item | Question | Evidence goal |
|---|---|---|---|
| LIB-ELQ-M-01 | `LIB-OQ-02` | What information helps you understand when a borrowed book is due? | Clarify loan-status and due-date needs without setting policy. |
| LIB-ELQ-M-02 | `LIB-OQ-03` | Should members be able to request a renewal, and what information should they see before requesting it? | Clarify renewal expectations without approving a rule. |
| LIB-ELQ-M-03 | `LIB-OQ-05` | What should members see when a book is already reserved or unavailable? | Clarify reservation queue expectations. |
| LIB-ELQ-M-04 | `LIB-OQ-06` | Which library events, if any, should notify members, and through what channels? | Clarify notification need without assuming channels. |

### Librarian Questions

| Question ID | Related item | Question | Evidence goal |
|---|---|---|---|
| LIB-ELQ-L-01 | `LIB-OQ-01`; `LIB-INT-L-02` | What book metadata must be recorded when a catalogue entry is created or updated? | Identify catalogue data without inventing fields. |
| LIB-ELQ-L-02 | `LIB-OQ-02` | How should librarians determine the due date for a loan? | Clarify due-date policy owner and rule. |
| LIB-ELQ-L-03 | `LIB-OQ-04`; `LIB-INT-L-03` | How should the system treat an overdue book record? | Clarify overdue policy without adding fine/payment scope. |
| LIB-ELQ-L-04 | `LIB-OQ-08` | What reports are useful to librarians, and what should each report contain? | Clarify reporting contents and access. |

### Administrator Questions

| Question ID | Related item | Question | Evidence goal |
|---|---|---|---|
| LIB-ELQ-A-01 | `SRC-01`; `LIB-INT-A-01` | What member-account and librarian-account data must administrators manage? | Clarify account-management scope. |
| LIB-ELQ-A-02 | `LIB-OQ-07`; `LIB-INT-A-02` | How should users be authenticated and how should roles be assigned? | Clarify security and role policy. |
| LIB-ELQ-A-03 | `LIB-OQ-10` | Is the borrowing system standalone or integrated with an existing campus identity or library catalogue system? | Clarify integration boundary. |
| LIB-ELQ-A-04 | `LIB-OQ-09`; `LIB-INT-A-03` | What response-time, availability, backup, and recovery expectations should be used later? | Gather measurable quality targets. |

### Library Management Questions

| Question ID | Related item | Question | Evidence goal |
|---|---|---|---|
| LIB-ELQ-MGMT-01 | `LIB-ASM-01`; `LIB-OQ-04` | Does library policy define overdue handling, fines, or escalation steps? | Validate whether management owns overdue policy. |
| LIB-ELQ-MGMT-02 | `LIB-ASM-01`; `LIB-OQ-08` | What summary reports, if any, does library management need? | Validate reporting needs for the assumed stakeholder. |

### IT Support Questions

| Question ID | Related item | Question | Evidence goal |
|---|---|---|---|
| LIB-ELQ-IT-01 | `LIB-ASM-02`; `LIB-OQ-07` | What access-control or account-management constraints must the system follow? | Clarify operational security expectations. |
| LIB-ELQ-IT-02 | `LIB-ASM-02`; `LIB-OQ-09` | What availability, backup, recovery, and incident-response targets apply? | Gather measurable reliability targets. |
| LIB-ELQ-IT-03 | `LIB-ASM-02`; `LIB-OQ-10` | Which existing systems, if any, must exchange data with the borrowing system? | Clarify integration scope. |

## 6. Existing Interview Answer Classification

| Response ID | Existing status | Test classification | Remaining gap |
|---|---|---|---|
| `LIB-INT-M-01` | CASE-CONFIRMED | Supports member activity coverage because it restates the test case. | Due dates, renewals, reservation queue, notifications, and detailed status remain open. |
| `LIB-INT-M-02` | UNANSWERED | Not ready for specification. | Notification events and channels. |
| `LIB-INT-M-03` | UNANSWERED | Not ready for specification. | Renewal rules. |
| `LIB-INT-L-01` | CASE-CONFIRMED | Supports librarian activity coverage because it restates the test case. | Catalogue metadata and detailed recording rules remain open. |
| `LIB-INT-L-02` | PARTIALLY ANSWERED | Confirms catalogue management topic, but not mandatory metadata. | Book metadata and validation rules. |
| `LIB-INT-L-03` | UNANSWERED | Not ready for specification. | Overdue policy. |
| `LIB-INT-A-01` | CASE-CONFIRMED | Supports administrator activity coverage because it restates the test case. | Account data, role assignment, and configuration detail remain open. |
| `LIB-INT-A-02` | UNANSWERED | Not ready for specification. | Authentication mechanism. |
| `LIB-INT-A-03` | CASE-CONFIRMED | Confirms quality areas at topic level. | Measurable targets remain open. |

## 7. Evidence Capture Template

| Field | Required content |
|---|---|
| Answer ID | Stable ID such as `LIB-INT-M-04`, `LIB-INT-L-04`, `LIB-INT-A-04`, `LIB-INT-MGMT-01`, or `LIB-INT-IT-01`. |
| Stakeholder | Member, librarian, administrator, library management, IT support, or another approved stakeholder. |
| Question ID | Related `LIB-ELQ-*` ID. |
| Source type | Real stakeholder answer, student-approved simulation, case-confirmed restatement, or assumption update. |
| Answer text | Recorded answer kept separate from AI interpretation. |
| Status | `CASE-CONFIRMED`, `ANSWERED`, `PARTIALLY ANSWERED`, `UNANSWERED`, or `ASSUMPTION-BASED`. |
| Date | Date recorded. |
| Reviewer or approver | Student or stakeholder who approved the entry. |
| Related open questions | Affected `LIB-OQ-*` IDs. |
| Specification readiness | Whether the answer can support later specification or still needs clarification. |

## 8. Open Questions and Decision Log

| ID | Current status | Owner | Decision needed before specification |
|---|---|---|---|
| `LIB-OQ-01` | Open | Librarian | Mandatory catalogue metadata. |
| `LIB-OQ-02` | Open | Librarian / library management | Loan duration and due-date rules. |
| `LIB-OQ-03` | Open | Member / librarian | Renewal rules. |
| `LIB-OQ-04` | Open | Librarian / library management | Overdue handling and possible fine policy. |
| `LIB-OQ-05` | Open | Member / librarian | Reservation queue behavior. |
| `LIB-OQ-06` | Open | Member / librarian | Notification events and channels. |
| `LIB-OQ-07` | Open | Administrator / IT support | Authentication and role assignment. |
| `LIB-OQ-08` | Open | Librarian / library management / administrator | Reporting contents and access. |
| `LIB-OQ-09` | Open | IT support / library management | Measurable NFR targets. |
| `LIB-OQ-10` | Open | Administrator / IT support | Standalone or integrated system boundary. |

## 9. Risks for Later Specification

| Risk ID | Risk | Evidence | Effect on later specification |
|---|---|---|---|
| LIB-ELR-01 | Catalogue requirements cannot be detailed until metadata is known. | `LIB-INT-L-02`; `LIB-OQ-01` | Blocks validation rules for catalogue management. |
| LIB-ELR-02 | Borrowing and return behavior cannot be detailed until due-date, renewal, overdue, and reservation rules are clarified. | `LIB-OQ-02` to `LIB-OQ-05` | Blocks detailed loan workflows and edge cases. |
| LIB-ELR-03 | Notifications are not approved. | `LIB-INT-M-02`; `LIB-OQ-06` | Blocks reminder or notification requirements. |
| LIB-ELR-04 | Security and integration decisions are open. | `LIB-INT-A-02`; `LIB-OQ-07`; `LIB-OQ-10` | Blocks detailed account, role, and interface requirements. |
| LIB-ELR-05 | NFRs are not measurable. | `LIB-INT-A-03`; `LIB-OQ-09` | Blocks testable usability, performance, reliability, and recovery requirements. |

## 10. Readiness Criteria for Later Specification

| Criterion | Current state |
|---|---|
| Cross-case Skill 01 output exists as a baseline. | Completed for this test. |
| Open questions are either answered, partially answered, or explicitly deferred. | Not completed; they remain open. |
| Student-approved policies exist for loan duration, renewal, overdue handling, notifications, authentication, reporting, integrations, and measurable NFR targets. | Not completed. |
| Assumptions keep `LIB-ASM-*` labels. | Preserved. |
| No final requirement is written from an unanswered item. | Preserved. |

## 11. Traceability Notes

- Confirmed test-case facts trace to `SRC-01` and case-confirmed simulated notes.
- Assumptions from the test fixture keep `LIB-ASM-*` IDs.
- Open questions keep `LIB-OQ-*` IDs.
- Elicitation questions use `LIB-ELQ-*` IDs.
- This output intentionally avoids requirements, user stories, use cases, priorities, validation results, and change requests.
