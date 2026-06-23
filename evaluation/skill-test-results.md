# Skill Test Results

## Test Summary

| Field | Value |
|---|---|
| Test date | 23 June 2026 |
| Tester / reviewer | Gerungan Dave Jordy, with AI assistance |
| Cross-case fixture | `evaluation/cross-case-library-borrowing-case.md` |
| Different case used | Library Book Borrowing System |
| Skills tested | Skill 01 Inception; Skill 02 Elicitation |
| Purpose | Verify that reusable skills can work beyond the main Student Task Management System case while preserving evidence discipline. |

## Evidence Files

| File | Purpose |
|---|---|
| `evaluation/cross-case-library-borrowing-case.md` | Mini case fixture with case brief, simulated interview notes, assumptions, and open questions. |
| `evaluation/cross-case-skill-01-output.md` | Cross-case output produced using the Skill 01 inception workflow. |
| `evaluation/cross-case-skill-02-output.md` | Cross-case output produced using the Skill 02 elicitation workflow. |
| `skills/01-inception/SKILL.md` | Revised after testing to clarify cross-case test mode. |
| `skills/02-elicitation/SKILL.md` | Revised after testing to clarify cross-case test mode and prerequisite baseline handling. |

## Test Method

1. Created a different requirements case: Library Book Borrowing System.
2. Defined source mapping so the skills could still separate case facts, simulated notes, assumptions, and open questions.
3. Applied Skill 01 to produce a cross-case inception output.
4. Applied Skill 02 to produce a cross-case elicitation plan using the Skill 01 test output as its baseline.
5. Checked whether each skill avoided premature requirements, unsupported policy choices, measurable NFR targets, and main-case contamination.
6. Revised the skill instructions where the test exposed reusable-skill weaknesses.

## Skill 01 Test: Project Inception and Stakeholder Discovery

| Check | Result |
|---|---|
| Can identify confirmed stakeholders in a different case. | Passed. It identified member, librarian, and administrator as confirmed stakeholders. |
| Can keep inferred stakeholders assumption-labelled. | Passed. Library management and IT support were kept as assumptions. |
| Can define problem, objectives, scope, constraints, risks, and open questions without writing requirements. | Passed. The output stayed at inception level. |
| Can avoid unsupported policies. | Passed. Renewal, overdue, notification, authentication, reporting, integration, and measurable NFR details stayed open. |
| Can preserve source labels. | Passed with fixture-specific labels such as `LIB-INT-*`, `LIB-ASM-*`, and `LIB-OQ-*`. |

### Weakness Found

The original Skill 01 instruction was too specific to the Student Task Management System. It named the main project in the trigger description and only described the main assignment input files and output path. That made cross-case testing possible only by interpretation, not by explicit instruction.

### Revision Made

Updated `skills/01-inception/SKILL.md` to:

- mention controlled cross-case skill testing in the skill description;
- separate main assignment inputs from cross-case fixture inputs;
- define source mapping for cross-case tests;
- require cross-case test evidence to be written under `evaluation/` or another requested test path;
- add a quality check that cross-case outputs must state they are not part of the main reviewed baseline.

## Skill 02 Test: Elicitation

| Check | Result |
|---|---|
| Can use a cross-case inception output as prerequisite baseline. | Passed after applying an explicit cross-case baseline rule. |
| Can create stakeholder-specific elicitation questions. | Passed. It produced member, librarian, administrator, library management, and IT support question groups. |
| Can classify simulated answers safely. | Passed. Case-confirmed, partial, and unanswered notes remained separated. |
| Can avoid writing requirements from unanswered items. | Passed. Loan duration, renewal, overdue, notifications, authentication, reporting, integrations, and measurable NFR targets remained open. |
| Can preserve evidence capture structure. | Passed. It defined a safe answer template for future stakeholder answers. |

### Weakness Found

The original Skill 02 instruction assumed `outputs/reviewed/01-inception.md` from the main case as the only prerequisite baseline. That is correct for the assignment workflow, but unclear for cross-case testing.

### Revision Made

Updated `skills/02-elicitation/SKILL.md` to:

- mention controlled cross-case skill testing in the skill description;
- separate main assignment inputs from cross-case test fixture inputs;
- require a cross-case Skill 01 output or equivalent inception baseline before using Skill 02;
- require cross-case outputs to stay under `evaluation/` or another requested test path;
- add a quality check that cross-case outputs must cite the fixture and avoid changing the main reviewed baseline.

## Overall Test Result

| Area | Result |
|---|---|
| Reusability | Passed after small instruction revisions. |
| Evidence discipline | Passed. Facts, simulated notes, assumptions, open questions, and decisions remained separated. |
| Boundary control | Passed. No new main-case requirements, policies, use cases, priorities, validation results, or change requests were created. |
| Revision need | Minor revisions were needed to make cross-case testing explicit. |

## Remaining Limitations

- Only Skill 01 and Skill 02 were tested on the different case because the assignment requires at least two skills.
- The Library Book Borrowing System fixture is intentionally small, so it tests transferability and evidence discipline rather than full end-to-end requirements depth.
- The cross-case outputs are test evidence, not student-reviewed baselines for a second full project.

## Conclusion

The two tested skills can be reused on a different requirements case when the source mapping and output boundary are explicit. The revisions improve clarity without changing the main Student Task Management System baseline.
