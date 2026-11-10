# Test checklist

Record your evidence in PR descriptions and phase checkpoint Issues. The sample results below are from the original lab documents.

## Phase 1
- [ ] Grade `75.3` → C; `33` → F; `97.1` → A.
- [ ] Grades `[90,85,95.5,77.5,88]`: sum 436.0, count 5, low 77.5, high 95.5.
- [ ] Grades `[10,70,90,92.5,85,95.5,77.5,88,100]`: sum 708.5, count 9, low 10, high 100.
- [ ] Check threshold values 59.9/60/69.9/70/79.9/80/89.9/90 (additional tests).

## Phase 2
- [ ] Billy Bob average 87.2; average minus low 89.625.
- [ ] Sally Sue average approximately 99.66666666666667; minus low 100.0.
- [ ] Class example: highest Sam, lowest Fred, failure list Fred, class average 80.55.
- [ ] Confirm `getStudentAverage` works by both index and name.

## Phase 3
- [ ] Keyboard sample: averages 95.00, 40.50, 72.75, 30.72; class average 59.7425.
- [ ] File sample: highest Sammy Morgan, lowest Marky Mark, class average 83.59375.
- [ ] Both runners use the same `Class`/`Student`/`Grades`/`Grade` logic.
- [ ] Equivalent keyboard/file inputs yield equivalent statistics.

## Clarification-only edge cases
Empty arrays, a student with one grade, ties, invalid indices, invalid scores, duplicate names, and file errors are not fully defined in the source labs. Discuss them with the teacher; do not silently invent grading rules.
