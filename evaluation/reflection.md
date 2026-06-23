# Reflection

## Project Context

This assignment used AI assistance to support requirements engineering for the Student Task Management System. The work was organised into five reusable skills: inception, elicitation, specification, prioritisation, and validation/change management. Each stage preserved raw AI output separately from student-reviewed output so the final baseline could show both AI contribution and human review.

## What Worked Well

The staged workflow helped keep the project controlled. Skill 01 and Skill 02 forced the early work to focus on stakeholders, scope, evidence, and open questions instead of jumping directly to requirements. Skill 03 then produced high-level requirements only from reviewed evidence. Skill 04 turned those requirements into user stories and priorities while keeping readiness risk visible. Skill 05 validated the baseline and grouped change requests without approving them.

The most useful AI contribution was structure. AI helped draft tables, traceability links, open-question lists, validation findings, and final diagrams faster than writing each artefact manually. It also helped maintain consistent IDs such as `FR-*`, `US-*`, `UC-*`, `DR-*`, and `CR-*`.

## Where AI Needed Careful Review

AI can easily make unresolved topics look decided. Areas such as late submission, resubmission, file limits, grade publication, notifications, authentication, reporting detail, retention, integrations, and measurable NFR targets were repeatedly at risk of becoming hidden assumptions. I had to keep these topics open unless there was evidence or explicit approval.

Another risk was mixing evidence types. Open questions and elicitation questions are useful, but they are not proof that a requirement is valid. The reviewed Skill 03 output corrected this by separating supporting evidence from open issues. This made the later traceability matrix more reliable.

## What Was Verified

- Raw AI outputs are preserved under `outputs/raw/`.
- Student-reviewed outputs are preserved under `outputs/reviewed/`.
- Skill 01 through Skill 05 each have reviewed artefacts.
- Final traceability connects objectives, stakeholders, requirements, stories, priorities, use cases, validation findings, deferred topics, and proposed change requests.
- The use-case diagram includes only reviewed high-level use cases `UC-01` through `UC-11`.
- Deferred topics remain deferred and proposed change requests remain unapproved.
- Skill 01 and Skill 02 were tested on a different case, the Library Book Borrowing System.
- The cross-case test produced evidence files and led to small revisions in the two tested skills.

## What Was Not Fully Verified

- No real stakeholder interview was conducted; the interview answers are educational simulations.
- The requirements are not implementation-tested because this assignment is about requirements engineering, not building the system.
- Non-functional requirements are not fully testable because measurable targets were not approved.
- Detailed policies for submission, grading, authentication, reporting, retention, integrations, and notifications remain unresolved.
- Only two skills were cross-case tested because the assignment requires at least two.

## Revisions Made After Testing

Cross-case testing showed that Skill 01 and Skill 02 worked conceptually, but their instructions were too tightly tied to the Student Task Management System file structure. I revised both skills to explicitly support controlled cross-case testing.

Skill 01 was revised to:

- allow controlled cross-case skill testing;
- distinguish main assignment inputs from test fixture inputs;
- define source mapping for cross-case tests;
- keep cross-case evidence under `evaluation/`;
- state that cross-case outputs are not part of the main reviewed baseline.

Skill 02 was revised to:

- allow controlled cross-case skill testing;
- require a cross-case Skill 01 output or equivalent inception baseline;
- keep elicitation test evidence under `evaluation/`;
- require cross-case outputs to cite their fixture and avoid changing the main baseline.

## What I Learned

The main lesson is that AI is useful for producing structured drafts, but requirements quality depends on review discipline. A polished table is not automatically correct. Each row still needs evidence, a clear status, and a boundary between what is known and what remains undecided.

I also learned that reusable skills need to be tested on a different case. A skill can look good when it only works for the original project, but cross-case testing reveals hidden assumptions in the instructions.

## Rules to Apply Next Time

- Keep raw AI output separate from reviewed output.
- Do not let AI answer policy questions silently.
- Treat assumptions as assumptions even when they seem reasonable.
- Keep open questions visible until there is evidence or approval.
- Separate evidence from unresolved questions.
- Test reusable skills on a different case before calling them reusable.
- Record every material revision in the changelog.

## Next Improvement

The next improvement would be to test Skill 03, Skill 04, and Skill 05 on the same Library Book Borrowing System fixture. That would show whether the full requirements workflow generalises beyond inception and elicitation.
