# GradeBook — Partner Java Project

**Team:** Two developers | **Workflow:** Asynchronous GitHub collaboration | **Language:** Java

## Project brief
Build a console-based gradebook in three releases. A `Grade` stores one numeric score and its letter equivalent; `Grades` stores an array of `Grade` objects; `Student` owns a name and a `Grades` object; `Class` stores an array of `Student` objects; two runners collect data from the keyboard and a file. Every release builds on the previous release. Both partners write Java, test the combined program, review one another's pull requests (PRs), and merge approved work.

The original six labs are adapted into one project. The required public methods are specified in `docs/INTERFACES.md`. **Do not rename `Class` to `SchoolClass` for this assignment**: the original lab names it `Class`. Do not replace the required arrays with `ArrayList`.

## Learning goals
- Implement object composition and arrays of object references.
- Delegate calculations through the class hierarchy instead of duplicating logic.
- Use loops, methods, input, and file reading to build a working program.
- Collaborate asynchronously using GitHub Issues, branches, PRs, reviews, and merges.

## Repository map
```text
src/                       Java starter files and student implementations
  Grade.java               GradeBook 0
  Grades.java              GradeBook 1
  Student.java             GradeBook 2
  Class.java               GradeBook 3
  GradeBookRunner.java     GradeBook 4: keyboard input
  GradeBookFileRunner.java GradeBook 5: file input
gradebook.dat               Sample data for final phase
milestones/                Requirements and acceptance criteria by phase
docs/                      GitHub workflow, interfaces, test checklist
.github/                   Issue and pull request templates
```
The original starter code and runners are included in `src/` on `main`. Some files intentionally contain empty methods; `Grade.java` is only a placeholder, and `GradeBookFileRunner.java` does not compile until its missing `theClass` setup is implemented. Compilation becomes a phase checkpoint, not a prerequisite for the untouched starter repository. **Do not submit independent lab branches**: use a shared team repository with feature branches merged into `main` after review.

## Project schedule
| Release | Original labs | Partner A lead | Partner B lead | Deliverable |
|---|---|---|---|---|
| 1: Foundations | GradeBook 0–1 | `Grade.java` | `Grades.java` | Grades stored and summarized |
| 2: Student/class | GradeBook 2–3 | `Class.java` | `Student.java` | Class statistics and student lookups |
| 3: Input | GradeBook 4–5 | Keyboard runner | File runner | Two input methods, consistent reports |

A *lead* is responsible for implementation, not exclusive ownership. Both partners must review, test, and understand the other's work. See the milestone files for exact requirements.

## Required GitHub evidence (each phase)
1. Create or claim a GitHub Issue for each assigned component; add acceptance criteria and assign an owner.
2. Create a new feature branch from the latest `main` (example: `feature/grade-class`).
3. Make meaningful commits; push the branch and open a PR that links the Issue (`Closes #12` if appropriate).
4. Request your partner's review. Reviewer checks the code, tests it, and leaves **at least one substantive comment** about correctness, a test case, or a design decision (not merely “looks good”).
5. Author responds to review feedback and makes necessary changes. Reviewer approves when ready.
6. Merge into `main` **only after** the code compiles, agreed acceptance criteria are met, and the partner approves. Update/close the Issue.
7. Both partners run the integrated program on `main` and record the result in the phase checkpoint Issue.

**Asynchronous rule:** Work need not occur at the same time. Communicate decisions in Issues/PRs; do not rely only on private messages. Never commit directly to `main` during the project.

## Required deliverables
- One shared GitHub repository containing the working code for all three phases.
- Six implementation Issues and their associated PRs (or a clearly documented equivalent split approved by the teacher).
- At least one meaningful review by each partner in **each phase**.
- Completed phase checkpoints and a final test summary.
- Both runners operating on the same `Grade` → `Grades` → `Student` → `Class` model.

## How to start
1. Read `docs/GITHUB_WORKFLOW.md` together.
2. Review `docs/INTERFACES.md` and agree on the class contracts before writing code.
3. Create the two Phase 1 Issues using `.github/ISSUE_TEMPLATE/feature.md`.
4. Create branches from `main` and begin work. Use `milestones/PHASE_1.md` for the acceptance criteria.

## Decisions requiring teacher clarification
The original labs do not specify behavior for empty grade arrays, ties, invalid input, or every boundary condition. The team should document proposed behavior in an Issue and obtain teacher approval **before** treating it as a requirement. `docs/DECISIONS.md` lists these items.

## Academic and collaboration expectations
Write your own assigned implementation, understand all merged code, and give actionable feedback. Do not approve a PR you have not examined. Follow the course's AI-use policy, if any, as provided separately by the teacher.
