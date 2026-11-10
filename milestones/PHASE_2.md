# Phase 2 — Student and Class (original GradeBook 2–3)

**Goal:** Represent individual students and an entire class using the existing grade classes.

## Partner B: Student (`feature/student-class`)
- Store a student name and a `Grades` object.
- Implement the original methods: `setName`, `setGrade`, `getNumGrades`, `getSum`, `getAverage`, `getAverageMinusLow`, `getHighGrade`, `getLowGrade`.
- Use `Grades` methods to perform grade calculations.
- Sample: Billy Bob (`90, 85, 95.5, 77.5, 88`) → average `87.2`; average excluding lowest `89.625`.
- Sample: Sally Sue (`100, 100, 99`) → average `99.66666666666667`; excluding lowest `100.0`.

## Partner A: Class (`feature/class-management`)
- Store the class name and a `Student[]`.
- Implement `addStudent`, class name/average, student average by index/name, student name by index, highest/lowest average student, and failure list.
- Use `Student` methods rather than duplicate calculations.
- Original example: Jimmy `82.50`, Sandy `87.50`, Fred `52.20`, Sam `100.00`; class average `80.55`; highest `Sam`, lowest `Fred`, failure list `Fred` for the example's threshold.

## Coordination and acceptance
1. Agree on Student constructor(s) and how `Class` obtains the student's name; these signatures are not fully given in the source documents.
2. Each partner opens an Issue and a PR. Review each other's implementation, not just its output.
3. Merge `Student` before `Class` if required; update the dependent branch and retest.
4. Both partners run integrated sample cases on `main` and record results.

**Discussion prompt:** How can `Class` compute an average without directly inspecting the internal `Grade[]` array?
