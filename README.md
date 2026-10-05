# llm-programming-retention

Anonymised data for the article:

> Gomez, R., Elmalech, A., and Hajaj, C. *Large Language Models in the Classroom: A Controlled Study of Learning and Retention in Programming.* ACM Transactions on Computing Education. DOI: [to be added]

## Study in brief

Master's students in an advanced Python course were allocated to two groups. The LLM group could use ChatGPT during an in-class practice session; the Control group could not. Both groups completed three programming tasks (Week 1), a time-management survey, and one week later an unassisted retention task followed by a perception survey (Week 2).

## Files

| File | Contents |
|---|---|
| `data/coding_scores.csv` | One row per submission: rubric scores per dimension, total score, and binary success (184 submissions from 48 students) |
| `data/survey1_time_management.csv` | One row per respondent: the five time-management items (42 respondents: 21 LLM, 21 Control) |
| `data/survey2_perception.csv` | One row per respondent: the 14 perception items (31 respondents: 18 LLM, 13 Control) |
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
| `basic_processing`, `advanced_processing`, `logic`, `output_correctness`, `code_quality` | 0 to 5, in steps of 0.5 |
| `total` | 0 to 25 |
| `success` | `1` Succeeded (total above 14), `0` Failed |

Students who did not submit an exercise have no row for it (Week 1: 48 students; Week 2: 40 students).

**survey1_time_management.csv**

Columns: `class_material_search`, `forum_search`, `web_search`, `planning`, `debugging`. Values 1 to 5.

**survey2_perception.csv**

Columns `q1` to `q14` follow the item numbers of the questionnaire. Values 1 to 5. An empty cell is an item the respondent left unanswered.

| Construct | Items |
|---|---|
| Attitude | q1, q4, q6, q9 |
| Knowledge | q2 |
| Learning Effectiveness | q3, q5 |
| Skills | q7, q8, q11 |
| Long-Term Learning | q10, q12, q13, q14 |

**interrater_subset.csv**

| Column | Values |
|---|---|
| `week`, `exercise` | As in `coding_scores.csv` |
| `second_rater` | `R2` or `R3`: anonymous label of the second rater |
| `primary_*`, `second_*` | Rubric scores (0 to 5) per dimension from the primary and second rater, and their sum (`primary_total`, `second_total`) |

Second-rater scores were used only to assess reliability.

**Likert coding**

Likert responses are coded `1` = Not at all, `5` = To a great extent. Item wording is in the article's appendix.

## Anonymisation

Names, student numbers, email addresses and Moodle identifiers were removed and replaced with random codes. Gender, used only to balance group allocation, is not included. No free-text responses or submitted code are shared. A few survey respondents have no coding scores, and a few students with coding rows did not answer a survey.

## Ethics

The study was approved by the Institutional Review Board of Bar-Ilan University (Approval No. 17042462).

## Licence

Data are shared under the Creative Commons Attribution 4.0 International licence (CC BY 4.0). Please cite the article above when using the data.
