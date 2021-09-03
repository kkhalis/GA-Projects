# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Test Analysis

## Problem Statement
The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university. Does the SAT need to focus on increasing participation rates? How would participating in one of test affect a student in terms of scoring? 

### Contents:
- [Executive Summary](#Executive-Summary)
- [Outside Research](#Outside-Research)
- [Datasets](#Datasets)
- [Data Dictionary](#Data-Dictionary)
- [Conclusions and Recommendations](#Conclusions-and-Recommendations)

---

### Executive Summary
Datasets from both the ACT and SAT for 2017 and 2018 were used in this analysis. Each dataset, consisting of average scores and participation rates in every state. This  would allow for a year-on-year comparison of test scores and participation rates, and also a comparison to measure the tests against each other.

---

### Outside Research
Averaging ACT or SAT scores by state helps colleges to set standards for admission, likely towards public universities with automatic admissions for in-state students <sup>1</sup>. Thus, it does carry a slight benefit for students looking to enter universities via such automatic admissions from their in-state colleges. There are other factors too, such as tuition fees and discounts for in-state students versus out-of-state students.

Although the ACT has been the reigning test since 2012, we can see a shift towards the SAT after its redesign in 2016, which removed the penalty on deducting scores for getting the wrong answer. However, there are other push factors on seeing the increase in acceptance for SAT in some states. The College Board pushes for statewide testing contracts, which can swing a state's staple test such as the ACT, to the SAT <sup>2,3</sup>. The College Board has also partnered with Khan Academy for free SAT preparation. This in turn would promote higher participation rates to the SAT.

The SAT tests only have 2 sections, Evidence-Based Reading and Writing (EBRW) and Math, whereas the ACT has 4 sections, English, Math, Reading and Science. Although the SAT has portions in the EBRW which contains elements of Science topics, the test doesn't necessarily target the topic directly as compared to the ACT. Additionally, because the SAT has one paper focused on math, students who are weaker in math might find their overall total score to be affected due to a higher weightage for the total score as compared to the ACT. Test takers would likely choose the ACT as it is more straightforward with its 4 sections of testing targeted at the various topics directly. However, students who are more proficient at math and EBRW would fare better if they took the SAT instead of the ACT.

Students in various states might not have the chance to choose whether to take the ACT or SAT, as different states require different tests. The scores for a student in a particular state which requires the SAT, might not be indicative of their true potential if they are weak in math, or even poor English speakers, who might not be able to quickly understand and solve problems <sup>4</sup>.

**Citations**
<br>
<sup>1</sup> https://magoosh.com/hs/sat/average-sat-scores-by-state-how-does-your-state-stack-up/
<br>
<sup>2</sup> https://www.edweek.org/teaching-learning/illinois-chooses-sat-over-act-for-statewide-college-readiness-testing/2015/12
<br>
<sup>3</sup> https://www.newamerica.org/education-policy/edcentral/how-college-boards-aggressive-campaign-to-save-the-sat-may-kill-it/
<br>
<sup>4</sup> https://www.reuters.com/investigates/special-report/college-sat-redesign

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

### Conclusions and Recommendations
From the findings above, we can see that the ACT and SAT average composite and total scores are inversely correlated with their participation rates in the respective states. This is likely due to selection bias, where we see test takers participating in low participation states tend to score better, and states with higher participation have a diluted average of scores due to the higher amount of participants.

The focus should be shifted to providing better test preparation resources, instead of increasing participation rates. Contracts with the College Board to push higher participation of SAT wouldn't help students if they were not prepared to handle the sections offered, as compared to the ACT.

---

### Slides
Link to slides can be found [*here*](https://docs.google.com/presentation/d/18xNWBXwIvc-aRzeFb72Xt-L-ftPIY-zVLYRrdMF4oqU/edit?usp=sharing).