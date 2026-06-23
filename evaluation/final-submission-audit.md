# Final Submission Audit

## Audit Scope

This audit checks the repository against the submission rules that are written inside the repository. It does not invent requirements from an unavailable external rubric.

## Sources Used

| Source | Use |
|---|---|
| `README.md` | Assignment objectives, final output list, evidence policy, and submission reminder. |
| `CASE.md` | Confirmed case baseline, scope, constraints, open questions, and source discipline. |
| `CHANGELOG.md` | Material change history. |
| `git status`, `git log`, and `git ls-files` | Commit, tracking, and workspace checks. |
| `gh repo view` | GitHub repository visibility check. |
| `gh issue list`, `gh api`, and `gh issue close` | GitHub issue presence, creation, and completion check. |

## Written Rules Checked

| Rule from repository | Audit result |
|---|---|
| Apply inception, elicitation, elaboration/specification, negotiation/prioritisation, validation, and change management. | Passed. Skill 01 through Skill 05 outputs exist and are reviewed. |
| Design five reusable AI skills with explicit workflow, outputs, rules, quality checks, and failure conditions. | Passed. Five skill folders exist with `SKILL.md` and examples. |
| Preserve raw AI output separately from student-reviewed output. | Passed. Numbered raw outputs are under `outputs/raw/`; reviewed outputs are under `outputs/reviewed/`. |
| Maintain traceability from stakeholder evidence to requirements and related artefacts. | Passed. Final traceability matrix exists at `outputs/reviewed/requirements-traceability.md`. |
| Test and improve at least two skills on a different case. | Passed. Skill 01 and Skill 02 were tested on the Library Book Borrowing System fixture and revised. |
| Complete the class field. | Passed. README lists `Summer Class 2026`. |
| Verify every README link. | Passed. Local README links were checked successfully. |
| Retain at least eight meaningful commits. | Passed. Repository had 22 commits before this final audit commit. |
| Confirm repository visibility unless GitHub Classroom is used. | Passed. `gh repo view` reported repository visibility as `PUBLIC`. |
| Publish required GitHub issues. | Passed at minimal marker level. Because the repository does not state a required issue count, title, or format, one factual completed issue was created and closed: `#1` "Finalize submission audit and ignore non-submission files". |

## Artefact Tracking Check

The following required artefact groups are tracked in Git:

- project metadata: `README.md`, `CASE.md`, `CHANGELOG.md`;
- inputs: `inputs/stakeholder-notes.md`, `inputs/interview-answers.md`, `inputs/assumptions.md`;
- five skills and examples under `skills/`;
- numbered raw outputs `outputs/raw/01-inception.md` through `outputs/raw/08-change-request.md`;
- reviewed outputs `outputs/reviewed/01-inception.md` through `outputs/reviewed/08-change-request.md`;
- final traceability matrix;
- final use-case diagram `.drawio` and `.png`;
- evaluation evidence including AI output review, skill test results, reflection, cross-case fixture, and cross-case outputs.

## Gitignore and Non-Submission Files

| Item | Handling |
|---|---|
| Local agent memory files | `.gitignore` now ignores `AGENT_MEMORY*.md` and `*_MEMORY*.md`. The existing memory file is outside this repository and is not tracked. |
| Obsolete placeholder raw-output stubs | `outputs/raw/*-ai-output.md` is ignored. These placeholder files are kept locally but removed from Git tracking. |
| Tool and OS noise | `.codex/`, `.agents/`, `Thumbs.db`, `Desktop.ini`, and `.DS_Store` are ignored. |

The numbered raw outputs remain tracked because they are actual evidence artefacts.

## Final Audit Result

The repository is ready for submission based on the written rules available in `README.md` and `CASE.md`. A minimal factual GitHub issue marker exists and is closed as completed. If the lecturer has a separate issue rubric, compare issue `#1` with that rubric before submission.

## Recommended Student Action Before Clicking Submit

1. Open the GitHub repository and confirm the latest commits are visible.
2. Confirm whether the lecturer requires a specific GitHub issue format beyond the completed issue marker `#1`.
3. Review the final traceability matrix, use-case diagram, skill test results, and reflection as the final human owner of the submission.
