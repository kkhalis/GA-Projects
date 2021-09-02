# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Test Analysis

## Problem Statement
The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university. Does the SAT need to focus on increasing participation rates? Are students choosing a particular test to get better results to enter their college of choice?


---

## Executive Summary
Datasets from both the ACT and SAT for 2017 and 2018 were used in this analysis. Each dataset, consisting of average scores and participation rates in every state. This  would allow for a year-on-year comparison of test scores and participation rates, and also a comparison to measure the performance the tests against each other.


---

### Datasets

4 datasets have been chosen for this project as shown below:

* [`act_2017.csv`](./data/act_2017.csv): 2017 ACT Scores by State
* [`act_2018.csv`](./data/act_2018.csv): 2018 ACT Scores by State
* [`sat_2017.csv`](./data/sat_2017.csv): 2017 SAT Scores by State
* [`sat_2018.csv`](./data/sat_2018.csv): 2018 SAT Scores by State

---

### Data Dictionary
Provided below is a data dictionary of the dataset

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**state**|*object*|act_2017.csv|State of ACT Participation and Results|
|**act_2017_participation**|*float*|act_2017.csv|Participation % of ACT in the related State in 2017|
|**act_2017_english**|*float*|act_2017.csv|Average results for English in the related State|
|**act_2017_math**|*float*|act_2017.csv|Average results for Math in the related State|
|**act_2017_reading**|*float*|act_2017.csv|Average results for Reading in the related State|
|**act_2017_science**|*float*|act_2017.csv|Average results for Science in the related State|
|**act_2017_composite**|*float*|act_2017.csv|Average of English, Math, Reading and Science scores in 2017, rounded to the nearest whole number|
|**act_2018_participation**|*float*|act_2018.csv|Participation % of ACT in the related State in 2018|
|**act_2018_composite**|*float*|act_2018.csv|Average of English, Math, Reading and Science scores in 2018, rounded to the nearest whole number|
**sat_2017_participation**|*float*|sat_2017.csv|Participation % of SAT in the related State in 2017|
**sat_2017_ebrw**|*int64*|sat_2017.csv|Average Evidence-Based Reading and Writing SAT score for the related State in 2017|
**sat_2017_math**|*int64*|sat_2017.csv|Average Math SAT score for the related State in 2017|
**sat_2017_total**|*int64*|sat_2017.csv|Average Total SAT score for the related State in 2017|
**sat_2018_participation**|*float64*|sat_2018.csv|Participation % of SAT in the related State in 2018|
**sat_2018_ebrw**|*int64*|sat_2018.csv|Average Evidence-Based Reading and Writing SAT score for the related State in 2018|
**sat_2018_math**|*int64*|sat_2018.csv|Average Math SAT score for the related State in 2018|
**sat_2018_total**|*int64*|sat_2018.csv|Average Total SAT score for the related State in 2018|
**composite_diff**|*float64*||Difference in Average Composite ACT scores between 2017 and 2018|
**total_diff**|*int64*||Difference in Average Total SAT scores between 2017 and 2018|
**act_participation_diff**|*float64*||Difference in participation % for ACT between 2017 and 2018|
**sat_participation_diff**|*float64*||Difference in participation % for SAT between 2017 and 2018|

---

### Conclusions & Recommendations
The SAT tests only have 2 sections, Evidence-Based Reading and Writing (EBRW) and Math, whereas the ACT has 4 sections, English, Math, Reading and Science. Although the SAT has portions in the EBRW which contains elements of Science topics, the test doesn't necessarily target the topic directly as compared to the ACT. For example, students who have a preference towards the science section might prefer to take the ACT instead, as there is a section entirely focused to science, while the SAT might put a science question occasionally in either the EBRW or math section. 

Additionally, because the SAT has one paper focused on math, students who are weaker in math might find their overall total score to be affected if they don't score well in the math section, since it has a higher weightage for the total score as compared to the ACT. Test takers would likely choose the ACT as it is more straightforward with its 4 sections of testing targeted at the various topics directly. However, students who are more proficient at math and EBRW would fare better if they took the SAT instead of the ACT.

The redesigned SAT testing also removed penalties for guessing. Test takers prior to the redesigned SAT would most likely have an adverse preference towards the SAT at that point, as test takers would need to put in more time to learn how to take the test<sup>1</sup>.

Students in various states might not have the chance to choose whether to take the ACT or SAT, as different states require different tests<sup>6</sup>. The scores for a student in a particular state which requires the SAT, might not be indicative of their true potential if they are weak in math. -- to insert chart here? --

The SAT should focus on targeting how to test an individual's problem solving skills, core thinking techniques and preparation for college, instead of increasing participation rates. Contracts with the College Board to push higher participation of SAT wouldn't help students if they were not prepared to handle the sections offered, as compared to the ACT.

There are still good initiatives, such as tying up with Khan Academy to prepare students ahead for the SAT.

---


**Citations**
<br>
<sup>1</sup>https://www.washingtonpost.com/news/grade-point/wp/2016/03/03/as-sat-enters-a-new-era-this-week-students-say-the-exam-has-improved/
<br>
<sup>2</sup> https://www.edweek.org/teaching-learning/in-race-for-test-takers-act-outscores-sat-for-now/2017/05
<br>
<sup>3</sup> https://www.washingtonpost.com/education/2018/10/23/sat-reclaims-title-most-widely-used-college-admission-test/
<br>
<sup>4</sup>https://www.edweek.org/teaching-learning/sat-scores-rise-as-number-of-test-takers-tops-2-million/2018/10
<br>
<sup>5</sup>https://dailynorthwestern.com/2018/11/12/campus/college-board-sat-overtakes-act-for-highest-number-of-test-takers/
<br>
<sup>6</sup>https://blog.prepscholar.com/act-vs-sat
<br>
<sup>7</sup>https://www.newamerica.org/education-policy/edcentral/how-college-boards-aggressive-campaign-to-save-the-sat-may-kill-it/

---
