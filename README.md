# llm-programming-retention

Anonymised data for the article:

> Gomez, R., Elmalech, A., and Hajaj, C. *Large Language Models in the Classroom: A Controlled Study of Learning and Retention in Programming.* ACM Transactions on Computing Education. DOI: [to be added]

## Study in brief

Master's students in an advanced Python course were allocated to two groups. The LLM group could use ChatGPT during an in-class practice session; the Control group could not. Both groups completed three programming tasks (Week 1), a time-management survey, and one week later an unassisted retention task followed by a perception survey (Week 2).

## Files

| File | Contents |
|---|---|
| `data/coding_scores.csv` | One row per submission: rubric scores per dimension, total score, and binary success (184 submissions from 48 students) |
| `data/survey1_time_management.csv` | One row per student: the five time-management items (Week 1) |
| `data/survey2_perception.csv` | One row per student: the 14 perception items (Week 2) |
| `data/interrater_subset.csv` | The 74 double-scored submissions: primary and second-rater scores per dimension |

## Codebook

**Common columns**

| Column | Values |
|---|---|
| `student_id` | Anonymous code (S01, S02, ...). Codes are consistent across files. |
| `group` | `LLM` or `Control` |

**coding_scores.csv**

| Column | Values |
|---|---|
| `week` | `1` or `2` |
| `exercise` | `1` Knowledge, `2` Skills, `3` Computational Thinking (Week 1); `1` Retention (Week 2, identical to Week 1 Exercise 3) |
| `basic_processing`, `advanced_processing`, `logic`, `output_correctness`, `code_quality` | 0 to 5 |
| `total` | 0 to 25 |
| `success` | `1` Succeeded, `0` Failed |

**Survey files**

Likert responses are reverse-coded for analysis: `1` = Not at all, `5` = To a great extent. Item wording is in the article's appendix.

- survey1: `class_material_search`, `forum_search`, `web_search`, `planning`, `debugging`
- survey2: `q1` to `q14`; constructs: Learning Effectiveness (q1 to q2), Knowledge (q3), Skills (q4 to q6), Attitude (q7 to q10), Long-Term Learning (q11 to q14)

## Anonymisation

Names, student numbers, email addresses and Moodle identifiers were removed and replaced with random codes. Gender, used only to balance group allocation, is not included. No free-text responses or submitted code are shared.

## Ethics

The study was approved by the Institutional Review Board of Bar-Ilan University (Approval No. 17042462).

## Licence

Data are shared under the Creative Commons Attribution 4.0 International licence (CC BY 4.0). Please cite the article above when using the data.
