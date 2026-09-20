---
layout: default
title: Contest Rules
nav_order: 3
---

# Contest Rules

**Updated: 20 September 2026.**

These rules cover the Individual Contest and Team Contest of the International Collegiate Artificial Intelligence Contest (ICAIC). They may be updated before the event to address omissions, inconsistencies, or new information, without substantial changes to the format.

The **Scientific Committee (SC)** has final authority to interpret these rules, adjudicate unforeseen situations, determine results, and decide appeals.

Each university designates a **Team Leader (TL)** as its non-competing representative, separate from the three contestants. The TL handles administrative matters and appeals, and ensures that the contestants understand and follow the rules. The TL does not participate in solving contest tasks or assist contestants during either contest.

## 1. General Requirements

### 1.1. Code of Conduct

- **Respect:** Treat everyone with respect and consideration, and welcome diversity.
- **Integrity:** Compete fairly and honestly.
- **Confidentiality:** Keep sensitive information confidential, especially task statements and solutions.
- **Professionalism:** Be courteous to fellow contestants and officials.
- **Safety and welfare:** Do not endanger anyone's emotional or physical well-being.
- **Compliance:** Understand and follow the rules, including contest procedures, submission deadlines, and event conduct.
- **Reporting misconduct:** Report rule violations or unethical behavior promptly.
- **Enforcement:** Violations may lead to sanctions, including disqualification and exclusion from future participation.

### 1.2. Eligibility Criteria

Each university may enter **one team of three contestants**. All three contestants must be undergraduate students enrolled in that university.

For ICAIC 2026, each contestant must also meet at least one of the following conditions:

- First began post-secondary studies in **2022 or later**.
- Was born in **2003 or later**.

Eligibility is assessed on the date of the first ICAIC contest.

For interrupted or extended studies, the TL may request an eligibility extension from the SC at least three weeks before the first ICAIC contest. The request must explain the circumstances and show that the extension would not give an unfair advantage. Approval is normally granted if the contestant meets all other eligibility requirements and has completed no more than the equivalent of eight semesters of full-time STEM study by the eligibility assessment date.

At on-site registration, contestants must present photo identification and proof of enrollment covering that date. A letter in English signed by a university official is sufficient proof of enrollment.

### 1.3. Team Rosters and Attendance

The three contestants on the university's accepted roster must remain the same for both contests. Reserves and substitutions are not permitted after the roster is accepted. If a contestant cannot or will not participate, the TL must promptly notify the SC. The SC decides the consequences for participation in either contest, including whether the remaining contestants may compete individually.

Contestants must attend all events designated as required in the event schedule. Absence may result in disqualification and forfeiture of awards. TLs must be available during registration, practice, both contests, and the awards ceremony. Contestants and TLs must follow organizers' instructions.

## 2. Contest Format and Procedures

Tasks follow the [ICAIC Syllabus](syllabus.md).

The procedures below apply to both contests, with each team acting as one participant for submissions, scoring, feedback, final submission selection, and limits in the Team Contest.

In these rules, “data” includes datasets, problem instances, and task environments.

### 2.1. Contest Format and Schedule

| Session | Format |
| --- | --- |
| Practice session | Held before the Individual Contest to familiarize contestants with the hall and contest system. It does not affect scores or medals. |
| Individual Contest | 3 tasks in 6 hours. |
| Team Contest | 2–3 tasks in 6 hours, solved jointly by the three contestants. |

#### Individual Contest

Contestants use organizer-provided laptops and are scored individually. During the contest, they may communicate only with authorized contest personnel through the procedures in Sections 2.5 and 2.6.

#### Team Contest

- Team members sit together and may communicate and cooperate.
- Each team receives **exactly one** organizer-provided laptop, shared by all three contestants. The team receives the same software environment, GPU allocation, and evaluation limits as one individual contestant, as specified in the [Technical Appendix](technical-appendix.md).
- During the contest, contestants may communicate only with their teammates and authorized contest personnel through the procedures in Sections 2.5 and 2.6.

### 2.2. Contest Environment

- The programming language is Python, with development in a Jupyter Notebook environment. The Python environment cannot be changed during the contest.
- Every contestant or team receives the same compute resources for solution development and evaluation.
- Each task may require submission of code, model artifacts, task outputs, or a combination of these, as specified in the task statement.
- Contestant laptops, development environments, and the grading system have no internet access during the contest. Only internal contest services are accessible. External downloads and APIs are prohibited.
- Messaging, collaboration, and file-sharing services are prohibited. Attempts to bypass platform restrictions are prohibited.
- LLM-based assistance is prohibited, including chat assistants, copilots, browser assistants, and AI coding agents, whether running locally or remotely. If the organizers provide an LLM as part of a task, contestants may use that model for assistance with any task in the same contest.
- Available packages, hardware, approved pretrained models, editors, and offline resources are specified in the [Technical Appendix](technical-appendix.md).
- Computer activity may be monitored and recorded.
- Requests concerning the contest environment may be sent to [sc@icaic.sg](mailto:sc@icaic.sg) no later than four weeks before ICAIC starts.

### 2.3. Supplies

**Provided:** Blank paper, writing tools, Clarification Request Forms, snacks, and water.

**Allowed:** Writing utensils, small non-electronic mascots, non-electronic earplugs, ID badges, snacks, and water.

**Prohibited:** Personal electronic devices, including computers, phones, smartwatches, smart glasses, earphones, calculators, external monitors, wireless communication devices, and electronic storage devices; books, manuals, notes, and other written reference materials. Keyboards, mice, medical devices, and supporting phones approved under the procedures below are exceptions.

Requests for personal keyboards, mice, or medical and special arrangements must be submitted through registration by the announced deadline before practice.

**Personal keyboards and mice:** Requests must include the device's make and model. Devices must be wired, have no wireless capability even when used wired, have no built-in macro or programmable-key functionality, and have no modifications affecting electronic functionality. The SC confirms before practice whether a device may be brought for inspection. Final approval follows inspection and testing during practice. The SC may reject a device even if it meets these requirements.

**Medical and special needs:** Personal medication is allowed. Electronic medical devices, supporting phones, and other special arrangements require SC approval before entry. Arrangements are agreed with the contestant before practice and checked during practice. Needs arising later must be reported as soon as possible. If a medical device requires a phone connection, the SC agrees on how the phone will be held and used; this may include a briefed volunteer holding the phone in the hall.

### 2.4. Starting the Contest

Contestants must be seated at least 10 minutes before the start. They must not touch laptops or tools until instructed by the organizers.

### 2.5. Clarification Requests

Task statements are in English. During the contest, contestants must use English when communicating with contest officials, and officials will respond in English.

Questions about task details, rules, or grading may be submitted to the Scientific Committee through the contest system or written forms. Responses may be:

- Yes or no.
- A reference to a section of the task statement, contest rules, or appendix.
- A request to consult the data and baseline first when the task description is unclear.
- A statement that the Python environment cannot be changed during the contest.
- A request to rephrase the question in yes/no format.

The Scientific Committee may decline ambiguous or unclear questions, or questions about knowledge contestants are expected to have. Substantial answers are broadcast to all contestants.

### 2.6. Technical Assistance Requests

For laptop, network, or other technical problems, raise the colored card as instructed by the organizers. Assistance staff address technical issues but do not answer task questions.

### 2.7. Evaluation, Feedback and Final Submission Selection

Tasks use the following data for development and evaluation. Task statements may specify different development or validation arrangements.

| Stage | Access during the contest | Purpose |
| --- | --- | --- |
| Development | Provided data, including labels where applicable. | Build and improve solutions. |
| Validation | Data access as specified in the task statement; reference answers remain hidden. | Evaluate submissions and provide feedback for solution improvement and selection. Results form the **Validation Leaderboard**. |
| Test | Test data and reference answers remain hidden from contestants. | Evaluate selected submissions after the contest. Results form the **Test Leaderboard** and determine official rankings, medals, and awards. |

After the contest, the grading system evaluates the selected submissions on hidden test data using the task's evaluation procedure.

The Validation Leaderboard is public, showing contestant or team identities, their best normalized validation score per task, and overall rankings by the sum of those scores.

It updates live until one hour before the scheduled end of each contest, then stays frozen until after the closing ceremony. During the freeze, private submission feedback shows evaluation status and raw validation metrics only. Updated normalized scores and normalization targets are withheld until the leaderboard is unfrozen.

#### Selecting submissions for final scoring

Each participant may select **up to two distinct submissions per task** before their contest deadline, including submissions still queued or running.

| Explicitly selected submissions | Submissions evaluated on the hidden test dataset |
| --- | --- |
| Two | Both selected submissions. |
| One | The selected submission and the remaining submission with the highest validation score. |
| None | The two submissions with the highest validation scores. |

Automatic selection uses valid higher-is-better validation scores before normalization. Ties are broken in favor of the submission received later by the contest system. A selected submission is not chosen again for the second slot. If fewer than two submissions are available, only the available submissions are evaluated.

Submissions received before the deadline continue to be evaluated after the contest. Once all validation results are available, the system fills any unselected slots according to the table above.

If a selected submission fails validation after the deadline, the TL must appeal under Section 2.11 to request a rerun or replacement. If the SC approves a replacement, it uses the remaining unselected submission with the highest validation score, following the automatic selection rule above.

### 2.8. Scoring and Ranking

Each task receives a final score from **0 to 100**. If a task has subtasks, their contributions are combined into one task metric as specified in the task statement. Normalization is applied once to the task score, not separately to subtasks.

#### Metric direction

The task statement defines the raw metric and whether higher or lower values are better. Convert it to a higher-is-better score before normalization:

```text
Submission_Score = Raw_Metric       if higher is better
Submission_Score = -Raw_Metric      if lower is better
```

Apply the same conversion to baseline and Scientific Committee metrics before normalization.

#### Normalization

Scores scale linearly from **0 points** at the baseline to **100 points** at the target defined below.

```text
Reference_Score = Min_Score + 0.9 × (SC_Score - Min_Score)
Max_Score = max(Reference_Score, Max_Submission)
Norm_Score = 100 × (Submission_Score - Min_Score) / (Max_Score - Min_Score)
```

The 0.9 factor allows a margin below the committee’s improvement over the baseline, making full marks more attainable. A higher contestant score raises the target.

Clamp `Norm_Score` to 0–100.

| Term | Definition |
| --- | --- |
| `Min_Score` | The baseline solution's higher-is-better score. |
| `SC_Score` | The Scientific Committee solution's higher-is-better score. |
| `Max_Submission` | For validation, the highest valid higher-is-better validation score across all participants' evaluated submissions. For test normalization, the highest valid higher-is-better test score across only the submissions selected for test evaluation under Section 2.7, including automatic selections. |
| `Reference_Score` | The committee-derived reference target. |
| `Max_Score` | The target for 100 points. If there are no valid evaluated submissions, use `Reference_Score`. |
| `Norm_Score` | The normalized task score. |

The Scientific Committee guarantees finite baseline and reference scores with **`SC_Score > Min_Score` on both validation and test data**.

Validation scores and their reference values are computed on validation data. Final test scores, including the baseline, Scientific Committee score, and highest selected submission score used for normalization, are computed on test data.

**Higher is better (accuracy).** With submission accuracy 85%, baseline accuracy 60%, Scientific Committee accuracy 95%, and best contestant accuracy 90% on the same dataset:

```text
Submission_Score = 0.85
Min_Score = 0.60
SC_Score = 0.95
Max_Submission = 0.90
Reference_Score = 0.60 + 0.9 × (0.95 - 0.60) = 0.915
Max_Score = max(0.915, 0.90) = 0.915
Norm_Score = 100 × (0.85 - 0.60) / (0.915 - 0.60)
           = 79.365079…
Displayed score = 79.3651
```

**Lower is better (RMSE).** With submission RMSE 3, baseline RMSE 5, Scientific Committee RMSE 2, and best contestant RMSE 2.5 on the same dataset:

```text
Submission_Score = -3
Min_Score = -5
SC_Score = -2
Max_Submission = -2.5
Reference_Score = -5 + 0.9 × (-2 - (-5)) = -2.3
Max_Score = max(-2.3, -2.5) = -2.3
Norm_Score = 100 × (-3 - (-5)) / (-2.3 - (-5))
           = 74.074074…
Displayed score = 74.0741
```

All raw metrics, conversions, normalization, and summation use IEEE 754 double precision with no intermediate rounding. Reports, scoreboards, and certificates display four decimal places. Rankings, submission-selection comparisons, and medal boundaries use full-precision values.

A submission that times out, exceeds memory limits, crashes, produces malformed output, or yields a non-finite metric receives **0 points**, without applying metric conversion or normalization. A task with no submission receives **0 points**.

All submissions count against the submission limit, including failed submissions. Platform-side failures are corrected and the affected evaluations rerun without consuming additional attempts. Alternatively, the SC may ignore an affected submission, excluding it from scoring and final submission selection and restoring one attempt.

If a contestant or team is disqualified from a contest, their submissions are excluded from that contest's normalization. The grading system recalculates the affected validation and test normalization targets, all affected scores and totals, rankings, and medal allocations using the remaining eligible participants. Published results are corrected accordingly.

A contestant's final task score is the **higher normalized test score of their two selected submissions**. If only one submission is available, its test score counts; if neither produces a valid result, the task score is 0.

#### Final ranking and ties

Participants are ranked by higher full-precision total test score, then lower total submission time. Remaining ties share a rank.

For each task where a selected submission beats the test baseline, count the time from contest start until the selected submission earning the final task score is received by the contest system. If both earn that score, use the submission received earlier. Sum these times across tasks. Other tasks contribute no time, and failed submissions incur no time penalty.

### 2.9. Ending the Contest

Warnings are given 15, 5, and 1 minute before the end. When the contest ends, contestants must stop immediately and wait for instructions to leave their desks.

Substantial technical problems may justify extra time, decided case by case. Contestants must report technical issues immediately as described in Section 2.6.

The Scientific Committee may grant an extension before or after the scheduled end, including for incidents reported immediately before the deadline. Contestants must stop at their current deadline and wait for instructions. If an extension is granted, organizers specify when work resumes and the revised deadline. The revised deadline applies to submissions and final-submission selections.

### 2.10. Cheating and Violations

Cheating is prohibited, including:

- Tampering with the contest system or attempting to breach the scoring system.
- Communicating with unauthorized people during the contest.
- Bringing prohibited items (see Section 2.3) into the contest hall.
- Attempting unauthorized access to test data.

### 2.11. Results and Appeals

#### Results after the contest

1. All contestants leave the hall.
2. Once all validation evaluations are complete and submissions selected under Section 2.7, the selected submissions are evaluated on hidden test data.
3. TLs and their contestants may enter for supervised inspection of their own laptops and submissions to prepare appeals.
4. Contestants are shown their best selected submission score on the Test Leaderboard for each task, both before and after normalization, without rankings. TLs receive these scores for all three contestants in the Individual Contest or for their team in the Team Contest.
5. TLs and contestants must keep these scores confidential from other teams until the closing ceremony.
6. Official test rankings are withheld until the closing ceremony. Afterward, the Validation Leaderboard is unfrozen and both final leaderboards are published for everyone.

#### Appeal process

All appeals must be submitted by Team Leaders. A TL may appeal for an individual contestant or for the entire team in the Team Contest.

Appeals may be submitted immediately after each contest ends. The closing deadline will be announced in the event schedule. Submission instructions and required information will be announced separately.

The Scientific Committee reviews all appeals. If it needs more information, it contacts the TL, who must reply promptly. The committee may meet the TL, and possibly the affected contestant, in person. The SC's decisions on appeals are final. They are shared with the General Assembly at its first meeting after those decisions for information, not further approval or review.

## 3. Medals, Trophy and Certificates

### 3.1. Medals

The Individual Contest and Team Contest each have a planned allocation of **4 gold, 4 silver, and 4 bronze medals**, awarded to contestants and teams, respectively, based on the final ranking in the corresponding contest.

In either contest, contestants or teams still tied at a medal boundary after the submission-time tiebreaker receive the same higher medal. Medal counts may therefore exceed the planned allocation. Each contestant may receive at most one Individual Contest medal, and each team at most one Team Contest medal.

### 3.2. Team Champion Trophy

The Team Champion Trophy will be awarded to the highest-ranked team in the Team Contest. The trophy will be retained by the contest organisation and carried forward as a challenge trophy for the subsequent edition of ICAIC. The name of the winning team will be engraved on the trophy.

### 3.3. Certificates

#### 3.3.1. Participation Certificate

Participation certificates are awarded to everyone officially involved, including contestants, team leaders, guests, volunteers, Scientific Committee and board members, host scientific, technical, and organizing committee members, and sponsors.

Each certificate includes the participant's name, role, and country. It is signed by ICAIC's Executive Director, with additional signatures at ICAIC's discretion.

#### 3.3.2. Achievement Certificate

Achievement certificates are awarded to contestants or teams winning official medals or awards. Each includes the contestant's or team's name, country, and achievement, such as a medal, award, or honorable mention. Certificates are signed by ICAIC's Executive Director and the Chair of the Scientific Committee.

### 3.4. Publication of Results

Results, scoreboards, medals, and awards are published on the official ICAIC website. Questions or suggestions about contest rules should be sent to [sc@icaic.sg](mailto:sc@icaic.sg).
