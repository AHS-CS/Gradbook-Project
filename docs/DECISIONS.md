# Decisions to agree on before implementation

The original lab sheets leave these details open. Create a GitHub Issue (or a clearly labeled comment on the relevant feature Issue) recording the decision and teacher approval.

1. **Constructors:** The provided GradeBook 2 and 3 documents mention constructors but do not give their signatures. Use the actual starter code if supplied; otherwise agree on signatures before implementation.
2. **Student name access:** `Class` needs a way to get a student's name; agree on the API if not in starter code.
3. **No grades / one grade:** Define behavior for `getAverage`, `getAverageMinusLow`, `getLowGrade`, and `getHighGrade` when there are too few grades.
4. **Class average:** The examples suggest the arithmetic mean of *student averages*; verify with the teacher rather than substituting the mean of all individual grades.
5. **Failure threshold:** Define whether the failure list includes averages strictly below the threshold or less than/equal to it, and which threshold to use in the runners.
6. **Ties:** Decide how highest/lowest-average ties are handled.
7. **Invalid input:** Decide whether invalid grades, indices, missing files, or malformed files must be handled.
8. **Formatting:** Match numerical results; agree whether exact spacing/decimal places matter.
9. **Class name:** Keep `Class` unless the teacher authorizes a rename.
