# Phase 3 — Keyboard and File Input (original GradeBook 4–5)

**Goal:** Use one shared gradebook model with two independent input mechanisms.

## Partner A: GradeBookRunner (keyboard)
- Inspect and test the supplied, mostly implemented keyboard runner.
- Verify it prompts for class name and number of students.
- For each student, prompt for name, number of grades, and each numeric grade.
- Verify that the runner constructs `Class` and `Student` using the agreed APIs, and fix defects found during testing.
- Display student grades/averages, failure list, highest/lowest average, and class average.
- Sample data from the original lab: freddy (`100,90`), sam (`9,12.5,100`), ben (`55.5,90`), willy (`5,10,15,90,33.6`). Expected averages: `95.00`, `40.50`, `72.75`, `30.72`; class average `59.7425`.

## Partner B: GradeBookFileRunner (file)
- Read `gradebook.dat` using the documented layout: class name, number of students, then each student's name, grade count, and numeric grades.
- Build the same object model as the keyboard runner and produce equivalent reports.
- Original file example: `AP Computer Science AB` with 8 students. Expected highest `Sammy Morgan`, lowest `Marky Mark`, class average `83.59375`.
- Use the teacher-provided `gradebook.dat` if available; `gradebook.dat` in this package is a transcription of the sample data.

## Integration acceptance
1. Agree on shared report formatting so the two runners display the same calculations.
2. Create separate Issues and feature branches; submit and review PRs.
3. Test both runners with equivalent input and compare results.
4. Demonstrate that all prior classes are reused (no duplicated gradebook calculation code in runners).
5. Both partners verify the merged program and post a final test summary in the checkpoint Issue.

**Discussion prompt:** Which code belongs in the runners, and which code belongs in the domain classes?
