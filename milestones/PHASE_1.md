# Phase 1 — Grade and Grades (original GradeBook 0–1)

**Goal:** Build the two foundational classes and integrate them.

## Partner A: Grade (`feature/grade-class`)
- Implement `Grade(double)`, `getNumericGrade()`, `getLetterGrade()`, and `toString()`.
- Grade letters: A ≥90, B ≥80, C ≥70, D ≥60, otherwise F.
- Sample cases: `75.3 C`, `33.0 F`, `97.1 A`.
- Open a PR and request Partner B's review.

## Partner B: Grades (`feature/grades-class`)
- Store a `Grade[]` constructed from a `double[]`.
- Implement `setGrade`, `getSum`, `getLowGrade`, `getHighGrade`, `getNumGrades`, `toString`.
- Use `Grade` methods rather than duplicate grade-letter logic.
- Sample 1: `90 85 95.5 77.5 88` → sum `436.0`, count `5`, low `77.5`, high `95.5`.
- Sample 2: `10 70 90 92.5 85 95.5 77.5 88 100` → sum `708.5`, count `9`, low `10.0`, high `100.0`.
- Open a PR and request Partner A's review.

## Coordination and acceptance
1. Agree on `Grade.toString()` output before building `Grades.toString()`.
2. Partner B may write code against the agreed `Grade` interface while Partner A finishes implementation.
3. Review each other's PRs. Merge `Grade` first if `Grades` depends on its implementation; then update `Grades` branch from `main` and resolve any conflicts.
4. Both partners compile and run the integrated code on `main`.
5. Close both Issues and record passing sample cases in a checkpoint Issue.

**Discussion prompt:** Why does `Grades` store an array of `Grade` objects instead of an array of `double` values?
