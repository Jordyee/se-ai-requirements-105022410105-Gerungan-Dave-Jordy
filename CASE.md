# Student Task Management System — Case Study

## 1. Document Status

- **Project:** Student Task Management System
- **Course:** Software Engineering
- **Case source:** Assignment brief provided by the lecturer
- **Prepared by:** Gerungan Dave Jordy (105022410105)
- **Status:** Initial case baseline, before AI skills are executed
- **Last updated:** 22 June 2026

This document separates information stated in the assignment from assumptions and open questions. Any information not explicitly supported by the assignment must remain labelled until it is validated.

## 2. Background

Lecturers and students need a campus application for managing coursework assignments. The application is expected to support the assignment lifecycle, including assignment creation, deadline management, submission, grading, feedback, status monitoring, and reporting. Administrators support the process by managing users, courses, and system configuration.

The assignment brief does not describe the institution's current software, existing manual process, technical platform, detailed policies, or integration requirements. Those matters cannot yet be treated as facts.

## 3. Problem Statement

The university needs a consistent way for lecturers, students, and administrators to manage information and activities related to coursework assignments. Without a defined system and clear requirements, assignment information, submission status, deadlines, grading, and reporting may be difficult to manage consistently across the three stakeholder groups.

This problem statement describes the operational need without prescribing implementation technology.

## 4. Initial Business Objectives

| ID | Objective | Source | Validation status |
|---|---|---|---|
| OBJ-01 | Enable lecturers to create assignments and define deadlines. | Assignment brief | Confirmed by case |
| OBJ-02 | Enable students to view assignments and submit files. | Assignment brief | Confirmed by case |
| OBJ-03 | Enable lecturers to record grades and feedback. | Assignment brief | Confirmed by case |
| OBJ-04 | Enable students to monitor assignment status and deadlines. | Assignment brief | Confirmed by case |
| OBJ-05 | Enable administrators to manage users, courses, and system configuration. | Assignment brief | Confirmed by case |
| OBJ-06 | Protect usability, security, performance, reliability, and data integrity. | Assignment brief | Confirmed at quality-attribute level; measurable targets remain open |

## 5. Stakeholders

| ID | Stakeholder | Role in the case | Initial interest |
|---|---|---|---|
| STK-01 | Lecturer | Creates assignments, sets deadlines, grades submissions, and provides feedback. | Efficient assignment administration and accurate grading records. |
| STK-02 | Student | Views assignments, submits files, and monitors status and deadlines. | Clear instructions, reliable submission, and visible status. |
| STK-03 | Administrator | Manages users, courses, and system configuration. | Controlled access, valid master data, and maintainable configuration. |
| STK-04 | University or academic management | Owns the academic process affected by the system. | Reliable operation and useful reporting. **ASSUMPTION:** This stakeholder is inferred and must be validated. |
| STK-05 | IT support or system operator | May operate and support the application. | Supportability, security, availability, and recoverability. **ASSUMPTION:** This stakeholder is inferred and must be validated. |

## 6. Preliminary Scope

### In Scope — Explicitly Supported by the Case

- Lecturer assignment creation.
- Assignment deadline definition.
- Student access to assignment information.
- Student file submission.
- Submission status and deadline monitoring.
- Lecturer grading and feedback.
- Administrator management of users, courses, and system configuration.
- Assignment-related reporting.
- Consideration of usability, security, performance, reliability, and data integrity.

### Out of Scope — Until Explicitly Approved

The following capabilities are not stated in the assignment and must not be generated as requirements without additional evidence:

- Real-time chat or video conferencing.
- Plagiarism detection.
- Tuition payment or other financial processing.
- Student attendance management.
- Course-content streaming or learning-material authoring.
- Integration with external learning management, identity, email, or cloud-storage services.
- Native mobile applications.

Items in this list may later enter scope through elicitation and change management; they are not permanently rejected.

## 7. Known Constraints

| ID | Constraint | Status |
|---|---|---|
| CON-01 | The project must use the Student Task Management System case. | Confirmed by assignment |
| CON-02 | Requirements artefacts must remain traceable to stakeholders and elicitation sources. | Confirmed by assignment |
| CON-03 | Unsupported information must be labelled as an assumption or open question. | Confirmed by assignment |
| CON-04 | The final requirements baseline remains the student's responsibility even when AI produces drafts. | Confirmed by assignment |
| CON-05 | Implementation technology, budget, schedule, hosting environment, and integration constraints are not provided. | Known information gap |

## 8. Initial Quality Concerns

The assignment explicitly identifies five quality areas. Their measurable thresholds are intentionally not defined yet:

- Usability
- Security
- Performance
- Reliability
- Data integrity

These terms must be converted into measurable, testable non-functional requirements during specification. Values such as response time, uptime, retention period, file-size limit, and recovery time require evidence or an explicitly approved assumption.

## 9. Initial Success Indicators

These indicators describe observable outcomes without inventing numerical targets:

- A lecturer can complete the defined assignment-management workflow.
- A student can find an assignment, submit a file, and verify the submission status.
- A lecturer can record a grade and feedback for a student submission.
- An administrator can manage the required user and course data.
- Each accepted functional requirement can be traced to a stakeholder and source.
- Critical failures and invalid operations are handled without silently corrupting academic data.

Numerical success targets remain open for elicitation.

## 10. Open Questions

| ID | Question | Intended stakeholder | Why it matters |
|---|---|---|---|
| OQ-01 | What assignment fields are mandatory when a lecturer creates an assignment? | Lecturer | Defines creation rules and validation. |
| OQ-02 | Are late submissions blocked, accepted with a marker, or controlled per assignment? | Lecturer / academic management | Affects submission business rules. |
| OQ-03 | May students replace a submitted file before the deadline, and must version history be retained? | Lecturer / student | Affects data integrity and auditability. |
| OQ-04 | Which file types and maximum file sizes are allowed? | Lecturer / IT support | Affects validation, storage, and security. |
| OQ-05 | Which events require notifications, and through which channels? | Lecturer / student | Prevents unsupported notification features. |
| OQ-06 | Can grades or feedback be changed after publication? | Lecturer / academic management | Defines authorization and audit rules. |
| OQ-07 | What reports are required and who may access them? | Lecturer / administrator / management | The assignment mentions reporting but not its contents. |
| OQ-08 | How are users authenticated and roles assigned? | Administrator / IT support | Required for access-control requirements. |
| OQ-09 | What response-time, availability, backup, and recovery targets apply? | IT support / management | Required for measurable NFRs. |
| OQ-10 | What personal or academic data retention rules apply? | Administrator / management | Affects privacy and data lifecycle. |
| OQ-11 | Is the system standalone or integrated with an existing campus system? | Administrator / IT support | Affects scope and interfaces. |
| OQ-12 | Which timezone and deadline cut-off rules apply? | Lecturer / administrator | Prevents deadline ambiguity. |

## 11. Baseline Rule

Only statements labelled **Confirmed by case** may be treated as facts at this stage. Items labelled **ASSUMPTION** require review, while `OQ-*` items must remain unresolved until a stakeholder answer or an approved simulation provides evidence.
