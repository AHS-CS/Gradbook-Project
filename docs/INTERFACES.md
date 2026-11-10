# Class contracts and starter-code checklist

These signatures have now been verified against the actual starter `.java` files. Keep the original names and return types. The supplied starter code is authoritative.

## Grade — GradeBook 0
```java
private double value;
public Grade(double v);
public double getNumericGrade();
public String getLetterGrade();
public String toString();
```
Letter mapping: `A` for 90 and above, `B` for 80–89.999…, `C` for 70–79.999…, `D` for 60–69.999…, otherwise `F`. The numeric thresholds follow the original lab; no rounding before classification is specified.

## Grades — GradeBook 1
```java
private Grade[] grades;
public Grades(double[] list);
public void setGrade(int pos, double grade);
public double getSum();
public double getLowGrade();
public double getHighGrade();
public int getNumGrades();
public String toString();
```
`Grades` must store `Grade` objects and use their methods when implementing its own behavior.

## Student — GradeBook 2
```java
private String myName;
private Grades myGrades;
public Student(String name, double[] gradeList);
public String getName();
public String toString();
public void setGrade(int spot, double grade);
public int getNumGrades();
public double getSum();
public double getAverage();
public double getAverageMinusLow();
public double getHighGrade();
public double getLowGrade();
```
Use `Grades` methods to implement `Student` behavior. The constructor and `getName()` method are already established by the supplied starter code.

## Class — GradeBook 3
```java
private String name;
private Student[] studentList;
public Class();
public Class(String name, int stuCount);
public void addStudent(int stuNum, Student s);
public String getClassName();
public double getClassAverage();
public double getStudentAverage(int stuNum);
public double getStudentAverage(String stuName);
public String getStudentName(int stuNum);
public String getStudentWithHighestAverage();
public String getStudentWithLowestAverage();
public String getFailureList(double failingGrade);
public String toString();
```
Use `Student` methods rather than reimplementing grade calculations. The constructor signatures and name access are established. Confirm the failure-threshold policy with the teacher.

## Input runners — GradeBook 4–5
- `GradeBookRunner.java`: read class name, student count, student names, grade counts, and scores from keyboard input; print class statistics.
- `GradeBookFileRunner.java`: read the same model from `gradebook.dat` in the repository root; print class statistics.
- The source documents do not prescribe runner method signatures. Both runners should reuse the same underlying classes.

## Interface-first collaboration
Before coding, partners should confirm the public APIs, constructor arguments, and expected `toString()` formats in a GitHub Issue. If an interface changes, discuss it in the PR so the dependent branch can be updated. Do not independently invent incompatible constructors.

## Original runner files included
`GradeRunner.java`, `GradesRunner.java`, `StudentRunner.java`, and `ClassRunner.java` are included as phase-specific sample runners. `GradeBookRunner.java` already implements the keyboard-input flow; students must verify and test it. `GradeBookFileRunner.java` is intentionally incomplete and refers to `theClass` before it is declared; this is a student task, not a packaging error. `Grade.java` contains only a placeholder comment, so the initial repository will not compile until the Phase 1 implementation is added.
