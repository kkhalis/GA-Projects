# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Test Analysis

## Problem Statement
The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university.

The SAT has two sections of the test: Evidence-Based Reading and Writing and Math ([*source*](https://www.princetonreview.com/college/sat-sections)). The ACT has 4 sections: English, Mathematics, Reading, and Science, with an additional optional writing section ([*source*](https://www.act.org/content/act/en/products-and-services/the-act/scores/understanding-your-scores.html)). They have different score ranges, which you can briefly read the summary of their scoring differences ([*here](https://blog.prepscholar.com/act-vs-sat)) :
* [SAT](https://collegereadiness.collegeboard.org/sat)
* [ACT](https://www.act.org/content/act/en.html)

Standardized tests have long been a controversial topic for students, administrators, and legislators. Since the 1940's, an increasing number of colleges have been using scores from sudents' performances on tests like the SAT and the ACT as a measure for college readiness and aptitude ([*source*](https://www.minotdailynews.com/news/local-news/2017/04/a-brief-history-of-the-sat-and-act/)). Supporters of these tests argue that these scores can be used as an objective measure to determine college admittance. Opponents of these tests claim that these tests are not accurate measures of students potential or ability and serve as an inequitable barrier to entry. Lately, more and more schools are opting to drop the SAT/ACT requirement for their Fall 2021 applications ([*read more about this here*](https://www.cnn.com/2020/04/14/us/coronavirus-colleges-sat-act-test-trnd/index.html)).



**To-Do:** *Fill out this cell (or edit the above cell) with any other background or information that is necessary for your problem statement.*

Are students choosing a particular test to get better results to enter their college of choice?

### Choose your Data

There are 10 datasets included in the [`data`](./data/) folder for this project. You are required to pick **at least two** of these to complete your analysis. Feel free to use more than two if you would like, or add other relevant datasets you find online.

* [`act_2017.csv`](./data/act_2017.csv): 2017 ACT Scores by State
* [`act_2018.csv`](./data/act_2018.csv): 2018 ACT Scores by State
* [`sat_2017.csv`](./data/sat_2017.csv): 2017 SAT Scores by State
* [`sat_2018.csv`](./data/sat_2018.csv): 2018 SAT Scores by State

---

### Outside Research
Based on your problem statement and your chosen datasets, spend some time doing outside research on state policies or additional information that might be relevant. Summarize your findings below. If you bring in any outside tables or charts, make sure you are explicit about having borrowed them. If you quote any text, make sure that it renders as being quoted. **Make sure that you cite your sources.**

**To-Do:** *Fill out this cell with outside research or any additional background information that will support your analysis.*

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
The SAT tests only have 2 sections, Evidence-Based Reading and Writing(EBRW) and Math, whereas the ACT has 4 sections, English, Math, Reading and Science. Although the SAT has portions in the EBRW which contains elements of Science, the test doesn't necessarily target the topic directly as compared to the ACT.

Given that the weightage in the SAT for the 2 tests could heavily affect the total score if one paper is not done well, test takers would likely choose the ACT as it is more straightforward with it's 4 sections of testing targeted at the various topics directly.