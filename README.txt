Synthetic school data for Databricks Lakeflow Designer testing
- trying different joins within Designer to see which pop up errors + which get blocked by setting up the guardrail operator

Files:
- students.csv: 30 students with grade level and homeroom.
- classes.csv: 6 classes with subjects and teachers.
- enrollments.csv: student-to-class mapping, 4 classes per student.
- test_scores.csv: clean assessment-level test scores.
- student_scores_flat.csv: denormalized version containing names, grades, classes, and scores.
- test_scores_messy.csv: intentionally contains data-quality issues for validation testing.

Intentional issues in test_scores_messy.csv:
1. One exact duplicate score row.
2. student_id S999 does not exist in students.csv.
3. class_id C999 does not exist in classes.csv.
4. One row has a missing score.
5. One score is greater than max_score.
6. One score is negative.
7. One letter_grade intentionally disagrees with percentage.
