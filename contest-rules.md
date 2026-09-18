# Contest Rules for ICAIC 2026

**Updated: 18 September 2026.**

These rules cover the Individual Contest and Team Contest of the International Collegiate Artificial Intelligence Contest (ICAIC). They may be updated before the event to address omissions, inconsistencies, or new information, without substantial changes to the format.

Each university designates a **Team Leader (TL)** as its non-competing representative, separate from the three contestants. The TL handles administrative matters and appeals and is responsible for ensuring that the contestants understand and comply with the rules. The TL does not participate in solving contest tasks or assist contestants during either contest.

## 1. General Requirements

### 1.1. Code of Conduct

- **Respect:** Show respect and consideration, welcome diversity, and support mutual understanding.
- **Integrity:** Play fairly, avoid deception, and maintain honest competition.
- **Confidentiality:** Safeguard sensitive information, especially problem statements and solutions.
- **Professionalism:** Interact with appropriate formality and decorum, respecting fellow competitors and officials.
- **Safety and welfare:** Do not endanger anyone's emotional or physical well-being.
- **Compliance:** Understand and follow the rules, including contest structure, submission deadlines, and event conduct.
- **Reporting misconduct:** Promptly report unethical behavior or rule violations.
- **Enforcement:** Infractions may result in sanctions, including disqualification and exclusion from future participation.

### 1.2. Eligibility Criteria

Each university may enter **one team of three contestants**. All three contestants must be undergraduate students enrolled in that university.

Enrollment eligibility is assessed on the date of the first ICAIC contest.

## 2. Individual Contest and Shared Procedures

Contestants use organizer-provided computers, must not communicate during the contest, and are scored individually. Medal allocations are based only on Individual Contest results. Tasks follow the [ICAIC Syllabus](syllabus.md).

Sections 2.2–2.11 also apply to the Team Contest, with the team acting as one participant for submissions, feedback, final submission selection, and limits. Team-specific scoring and permitted communication within the team are described in section 3. Technical assistance, extensions, conduct, and appeal procedures are shared by both contests.

### 2.1. Contest Schedule

| Session | Format |
| --- | --- |
| Practice session | Held before the Individual Contest to familiarize contestants with the hall and contest system. It does not affect scores or medals. |
| Individual Contest | 3 tasks in 6 hours. |
| Team Contest | 2–3 tasks in 6 hours, solved jointly by the three contestants. |

### 2.2. Contest Environment

- The programming language is Python, with development in a Jupyter Notebook environment.
- PyTorch and scikit-learn are the core AI/ML libraries. TensorFlow and Keras are unavailable. Additional packages cannot be downloaded during the contest.
- Contestants receive identical local machines, subject to minor technical differences, and identical GPU resources.
- Tasks may involve writing code, fitting models on training data, and running inference on test data.
- Each task may require submission of code, trained models, model predictions, or a combination of these.
- Contestant laptops, training environments, and the grading system have no internet access during the contest. Only internal contest services are accessible. Approved models, datasets, and documentation are provided within the contest environment. External downloads and APIs are prohibited.
- No LLM assistant is provided. LLM-based chat assistants, copilots, browser assistants, and AI coding agents are prohibited.
- Available packages, hardware, approved pretrained models, editors, and offline resources are specified in the [Technical Appendix](technical-appendix.md).
- Screen activity may be monitored live and recorded.
- Requests for additional editors or offline documentation may be sent to [sc@icaic.sg](mailto:sc@icaic.sg) up to four weeks before ICAIC starts.

### 2.3. Scoring

Each task receives a final score from **0 to 100**. If a task has subtasks, their contributions are combined into one task metric as specified in the task statement. Normalization is applied once to the task score, not separately to subtasks.

#### Metric direction

The task statement defines the raw metric and whether higher or lower values are better. Convert it to a higher-is-better score before normalization:

```text
Submission_Score = Raw_Metric       if higher is better
Submission_Score = -Raw_Metric      if lower is better
```

For example, an RMSE of 2 becomes a score of -2 and ranks above an RMSE of 5, which becomes -5. Apply the same conversion to baseline and Scientific Committee metrics. Leaderboard A uses these higher-is-better scores.

#### Normalization

The baseline earns **0 points**. The target for **100 points** is whichever is higher: 90% of the Scientific Committee's improvement over the baseline, added to the baseline, or the best contestant submission. Scores between the baseline and target scale linearly.

```text
Reference_Score = Min_Score + 0.9 × (SC_Solution - Min_Score)
Max_Score = max(Reference_Score, Max_Submission)
Norm_Score = 100 × (Submission_Score - Min_Score) / (Max_Score - Min_Score)
```

Clamp `Norm_Score` to 0–100: values below 0 become 0, and values above 100 become 100.

| Term | Definition |
| --- | --- |
| `Min_Score` | The baseline solution's higher-is-better score. |
| `SC_Solution` | The Scientific Committee solution's higher-is-better score. |
| `Max_Submission` | The highest valid higher-is-better score across all contestants' submissions evaluated on the relevant dataset, including the contestant's own submissions. For final scoring, this includes only submissions selected for test evaluation. |
| `Reference_Score` | The baseline score plus 90% of the improvement from the baseline to the Scientific Committee solution. |
| `Max_Score` | The target for 100 points: the greater of `Reference_Score` and `Max_Submission`. If there are no valid evaluated submissions, use `Reference_Score`. |
| `Norm_Score` | The task score after normalization and clamping to the range 0–100. |

The Scientific Committee guarantees finite baseline and reference scores with **`SC_Solution > Min_Score` on both validation and test data**. This ensures that the denominator is positive, even if no contestant beats the baseline.

Validation scores and their reference values are computed on validation data. Final test scores, including the baseline, Scientific Committee score, and highest selected submission score used for normalization, are computed on test data. Validation scores are never used as test normalization references.

For example, with submission accuracy 85%, baseline accuracy 60%, Scientific Committee accuracy 95%, and highest contestant accuracy 90% on the same dataset:

```text
Reference_Score = 60% + 0.9 × (95% - 60%) = 91.5%
Max_Score = max(91.5%, 90%) = 91.5%
Norm_Score = 100 × (85% - 60%) / (91.5% - 60%)
           = 79.365079…
Displayed score = 79.3651
```

For a lower-is-better metric, baseline RMSE 5 and committee RMSE 2 become scores -5 and -2. The reference score is `-5 + 0.9 × (-2 - (-5)) = -2.3`, corresponding to RMSE 2.3. This requires 90% of the committee's improvement over the baseline, consistently with higher-is-better metrics.

All raw metrics, conversions, normalization, and summation use IEEE 754 double precision with no intermediate rounding. Reports, scoreboards, and certificates display four decimal places. Rankings, submission-selection comparisons, and medal boundaries use full-precision values.

A submission that times out, exceeds memory limits, crashes, produces malformed output, or yields a non-finite metric receives **0 points**, without applying metric conversion or normalization. A task with no submission receives 0 points. Platform-side failures are corrected and the affected evaluations rerun; they do not count against the submission limit.

A contestant's final task score is the **higher normalized test score of their two selected submissions**. If only one submission is available, its test score counts; if neither produces a valid result, the task score is 0.

### 2.4. Feedback and Final Submission Selection

Unless a task statement specifies a different training or validation arrangement, Individual and Team Contest tasks use the following datasets. The entire test dataset remains hidden in all cases.

| Dataset | Access during the contest | Purpose |
| --- | --- | --- |
| Training | Data and labels | Train models. |
| Validation | Data, without labels | Evaluate submissions during the contest and provide feedback for hyperparameter adjustment and model selection. Results form **Leaderboard A (Validation)**. |
| Test | Neither inputs nor labels | Evaluate selected submissions after the contest. Results form **Leaderboard B (Test)** and determine official rankings, medals, and awards. |

Contestants cannot inspect, train on, or generate predictions locally for the hidden test dataset. After the contest, the grading system runs the selected submissions on test inputs and scores their outputs against hidden labels.

During the contest, contestants see their own Leaderboard A scores per task, the baseline score (`Min_Score`), and the anonymous highest higher-is-better submission score across all contestants (`Max_Submission`), including their own submissions. They cannot see other contestants' individual scores or rankings.

#### Selecting submissions for final scoring

Each individual contestant, or each team in the Team Contest, may bookmark or select **up to two distinct submissions per task** before their contest deadline.

| Explicitly selected submissions | Submissions evaluated on the hidden test dataset |
| --- | --- |
| Two | Both selected submissions. |
| One | The selected submission and the highest-scoring remaining submission on Leaderboard A. |
| None | The two highest-scoring submissions on Leaderboard A. |

Automatic selection considers submissions with valid Leaderboard A scores. Ties are broken in favor of the submission received later by the contest system. A selected submission is not chosen again for the second slot. If fewer than two submissions are available, only the available submissions are evaluated.

Submissions received before the deadline continue to run even if they are queued or still executing when the contest ends. Automatic selection takes place after their validation evaluations finish. Explicit selections cannot be changed after the contestant's deadline.

#### Results after the contest

1. All contestants leave the hall.
2. TLs may enter to inspect their team's laptops and submissions.
3. TLs are shown the best selected submission score on Leaderboard B for each task, for each of their contestants in the Individual Contest or for their team in the Team Contest, both before and after normalization, without rankings.
4. TLs share these scores with their contestants to prepare appeals, while keeping them confidential from other teams until the closing ceremony.
5. Official rankings are withheld until the closing ceremony. Afterward, both leaderboards are published for everyone.

### 2.5. Supplies

**Provided:** Blank paper, writing tools, Clarification Request Forms, snacks, and water.

**Allowed:** Writing utensils, small mascots, non-electronic earplugs, ID badges, snacks, and water. Contestants may request permission from the Scientific Committee during practice to use their own keyboard or mouse; approval is not guaranteed. External monitors are prohibited.

**Prohibited:** Personal electronic devices, including computers, phones, earphones, calculators, communication or Bluetooth-enabled items; books; manuals; data storage media; and other items that can store or transmit data.

**Medical and special needs:** Medical items, such as tablets and glucometers, require Scientific Committee approval before entry. Requests may be made during practice. If a medical device needs a Bluetooth connection to a phone, the phone must be held by a volunteer in the hall who has been briefed on how to respond to abnormal situations. Other situations should be reported to the Scientific Committee before practice.

### 2.6. Starting the Contest

Contestants must be seated at least 10 minutes before the start. They must not touch workstations or tools until instructed by the organizers.

### 2.7. Clarification Requests

Questions about task details, rules, or grading may be submitted to the Scientific Committee through the contest system or written forms. Responses may be:

- Yes or no.
- A reference to a section of the task statement, contest rules, or appendix.
- A request to consult the dataset and baseline first when the task description is unclear.
- A statement that the Python environment cannot be changed during the contest.
- A request to rephrase the question in yes/no format.

The Scientific Committee may decline ambiguous or unclear questions, or questions about knowledge contestants are expected to have. Non-trivial, substantial answers are broadcast to all contestants.

### 2.8. Technical Assistance Requests

For computer, network, or other technical problems, raise the colored card as instructed by the organizers. Assistance staff address technical issues but do not answer task questions.

### 2.9. Ending the Contest

Warnings are given 15, 5, and 1 minute before the end. When the contest ends, contestants must stop immediately and wait for instructions to leave their desks.

Substantial technical problems may justify extra time, decided case by case. Contestants must report an issue immediately through a clarification request or, if their computer or network is unavailable, by raising the colored card and notifying assistance staff.

The Scientific Committee may grant an extension before or after the scheduled end, including for incidents reported immediately before the deadline. Contestants must stop at their current deadline and wait for instructions. If an extension is granted, organizers specify when work resumes and the revised deadline. The revised deadline applies to submissions and final-submission selections.

### 2.10. Cheating and Violations

Cheating is prohibited, including:

- Tampering with the contest system or attempting to breach the scoring system.
- Direct or indirect communication with other contestants or people outside the hall during the Individual Contest.
- Bringing prohibited items into the hall.
- Attempting unauthorized access to test data.

### 2.11. Appeal Process

All appeals must be submitted by Team Leaders. A TL may appeal for an individual contestant or for the entire team in the Team Contest.

Appeals may be submitted immediately after each contest ends. The closing deadline will be announced in the event schedule. Submission instructions and required information will be announced separately.

The Scientific Committee reviews all appeals. If it needs more information, it contacts the TL using the contact details supplied with the appeal; the TL must reply as quickly as possible. The committee may arrange a face-to-face meeting with the TL and possibly the affected contestant. Organizers announce the meeting details and timing. Final decisions are shared with the General Assembly at its first meeting after those decisions.

## 3. Team Contest

The Team Contest is an official, creative, AI-oriented contest for university teams.

- Team members sit together and may communicate and cooperate.
- Each team shares **one organizer-provided computer or laptop** and receives the same software environment, GPU allocation, and evaluation limits as one individual contestant, as specified in the Technical Appendix. Internet access is not available.
- Teams must not communicate with other teams or with people outside the contest hall.
- The allowed and prohibited items are the same as for the Individual Contest, including the approval requirements for personal peripherals and medical items.
- Scoring is task-specific and described in the task statements.
- The highest-performing teams receive Team Contest trophies at the closing ceremony. No Team Contest medals are awarded.

The duration and task count are listed in section 2.1. Submission limits and final selection slots apply to the whole team, not separately to each member.

## 4. Medals, Awards, Trophies and Certificates

### 4.1. Individual Contest

Medals are awarded solely on total Individual Contest scores. The planned allocation is **4 gold, 4 silver, and 4 bronze medals**.

If contestants tie at a medal boundary, all contestants with that full-precision total score receive the same higher medal. Medal counts may therefore exceed the planned allocation; no contestant receives more than one medal.

### 4.2. Team Contest

The top teams by Team Contest score receive **Team Contest trophies**. No medals are awarded for the Team Contest. Teams tied at an award boundary all receive the same award.

The event trophy remains with the organizer for use in future editions. Further award arrangements will be announced later.

### 4.3. Certificates

#### 4.3.1. Participation Certificate

Participation certificates are awarded to everyone officially involved, including contestants, team leaders, guests, volunteers, Scientific Committee and board members, host scientific, technical, and organizing committee members, and sponsors.

Each certificate includes the participant's name, role, and country. It is signed by ICAIC's Executive Director, with additional signatures at ICAIC's discretion.

#### 4.3.2. Achievement Certificate

Achievement certificates are awarded to contestants or teams winning official medals, awards, or trophies. Each includes the contestant's or team's name, country, and precise achievement, such as a medal, award, trophy, or honourable mention. Certificates are signed by ICAIC's Executive Director and the Chair of the Scientific Committee.

### 4.4. Hall of Fame

Results, scoreboards, medals, and awards are published on the official ICAIC website. Questions or suggestions about contest rules should be sent to [sc@icaic.sg](mailto:sc@icaic.sg).
