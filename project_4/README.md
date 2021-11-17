<<<<<<< HEAD
# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) West Nile Virus Prediction across the city of Chicago

## Problem Statement

Due to the recent epidemic of West Nile Virus in the Windy City, the Department of Public Health set up a surveillance and control system to help collect data on mosquito numbers, West Nile Virus appearance, and weather events.

As part of the Disease And Treatment Agency, division of Societal Cures In Epidemiology and New Creative Engineering (DATA-SCIENCE), we have been tasked to assess the viability of the current spray model, as well as to try and predict occurrence of West Nile Virus in Chicago by training classifier models. This will further refine the current pest management model.

<a href = 'https://www.preventivepestcontrol.com/weather-affect-mosquito-activity/'> Mosquitoes enjoy wet and warm climates and are most active in temperatures above 80 degrees</a>. Conversely, when temperatures go below 50 degrees, mosquitoes go dormant.  

Mosquito lifecycles for Culex Pipiens, the most common mosquito caught in Chicago, <a href='https://www.in.gov/health/erc/zoonotic-and-vectorborne-epidemiology-entomology/pests/culex-species-mosquitoes/'>typically range from 2-4 weeks, and even less than a week in the heat of summer</a>.

Our project will seek to:

1. Determine the effectiveness of sprays on the mosquito population
2. Predict the occcurence of West Nile Virus
3. Help provide guidelines by which to apply future sprays
4. Conduct a cost benefit analysis on the use of the pesticides in response to the epidemic

After training on the classifier models, the selection of the best model will be guided by the Precision, Recall, ROC-AUC and PR score on the validation set.

## Contents
* Data import, helper functions, cleaning and imputation of missing values
* EDA: Previewing Data and Highlighting Outliers
* Modelling
* Applying our selected model on the Kaggle test set
* Cost-Benefit Analysis and Conclusion

## Executive Summary
This project aims to find try and predict the presence of West Nile Virus within mosquitoes using various classification models, to assess the viability and effectiveness of the spray model employed in 2011 and 2013, and thereafter conduct a cost-benefit analysis on the use of sprays. 

Initial analysis showed some columns with completely missing, or mostly trace data, such as `water1`, `depth` and `snowfall`. As number of mosquitoes per row were capped at 50, the records were summed up to get the total number of mosquitoes into 1 record. Imputation of missing values were done by adding the mean difference between both stations, to the station with available values.

Presence of West Nile Virus were mostly found in Culex Pipiens and Culex Restuans species. There were notably higher numbers of mosquitoes caught when relating with certain weather phenomena, such as mist, drizzle or rain. Temperature correlating with specific times of the year were also found to promote the number mosquitoes caught. This suggests that the pooling of stagnant water sources after such weather conditions, in addition to temperatures during specific seasons of the year, contributed to increased breeding and growth of mosquitoes. 

The spray data provided, however, did not prove to be very effective as the sprays were always conducted <b>after</b> the mosquitoes were caught. Although the traps are scattered and collected every week only from Monday through Wednesday, sprays, which are only effective on the day sprayed, were mostly conducted on Thursdays. Hence, they did not provide most correlation to the mosquito population post-spray.

A few features were engineered additionally, such as the lag of days, ranking of traps based on mosquitoes caught, to improve predictive power for our classification models. The dataset is severely imbalanced due to only a small set of being present with West Nile Virus. We utilised SMOTE, a statisical technique which helps to increase the number of samples in a balanced way. Ultimately, the logistic regression classification model was found to have the best PR-AUC score, with a kaggle result of 0.71124.

With regards to cost-benefit analysis and conclusions, please refer to their individual sections below.

=======
# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Kaggle Competition - Starter

## Introduction

Welcome to your first week of work at the Disease And Treatment Agency, division of Societal Cures In Epidemiology and New Creative Engineering (DATA-SCIENCE). Time to get to work!

Due to the recent epidemic of West Nile Virus in the Windy City, we've had the Department of Public Health set up a surveillance and control system. We're hoping it will let us learn something from the mosquito population as we collect data over time. Pesticides are a necessary evil in the fight for public health and safety, not to mention expensive! We need to derive an effective plan to deploy pesticides throughout the city, and that is **exactly** where you come in!
>>>>>>> 10756d444d50c74526dcaa9a1e84d338bdaff6a4

## Dataset

The dataset, along with description, can be found here: [https://www.kaggle.com/c/predict-west-nile-virus/](https://www.kaggle.com/c/predict-west-nile-virus/).

<<<<<<< HEAD

* [`train.csv`](./assets/train.csv): Training set consists of data from 2007, 2009, 2011, and 2013.
* [`test.csv`](./assets/test.csv): Test set consists of data required to predict results for 2008, 2010, 2012, and 2014.
* [`weather.csv`](./assets/weather.csv): Weather data from 2007 to 2014 of 2 stations
* [`spray.csv`](./assets/spray.csv): GIS data of spraying efforts in 2011 and 2013

### Data Dictionary
You can access the data dictionary, split into markdown format [*here*](https://github.com/kkhalis/project_4/blob/master/DataDictionary.md).

You can also access the detailed description of weather info in the Data Dictionary [*here*](https://github.com/kkhalis/project_4/blob/master/assets/noaa_weather_qclcd_documentation.pdf)

## Project Planning
Project Plan Documentation can be found [*here*](https://docs.google.com/spreadsheets/d/1_o3eWrHmSxif5hHflbAwt84u0uXwgWTV/edit#gid=540275792).

## Cost-Benefit Analysis

In effective pest management, one should consider the use of different spray types and effectiveness, as well as factors influencing the lifecycle of the pest.

When considering only fogging, the typical spray used in residential areas for combating mosquitos, timing of the spray should be strongly considered in reducing a mosquito population due to its time-constrained effectiveness:
1. Timing of rainfall
* Rainfall can have a large impact on the population of mosquitos, with stagnant, trapped water providing fertile breeding ground. In built-up cities such as Chicago, it can be difficult to get rid of all water traps and to completely eliminate sources of stagnant water. Use of fogging 8-10 days after a heavy downpour can be a timely way to eliminate mosquito populations for the day, as they are hatching, and accurately target the spray to its window of maximum effectiveness.

* Spray use should also be avoided when the timing coincides with predictions of rainfall on the day itself. For maximum effectiveness, sprays would have to remain in the air and interact with the mosquito population. Any precipitation during the course of the day would reduce the effectiveness of the spray by taking it out of the air and preventing maximum exposure.

2. Degree Days
* Mosquitos have shown to be most active around a specific temperature band, above 65F, often measured in degree days. When judging appropriate spray effectiveness, degree days can be used to help judge the use and timing of sprays. More days consistently above the 65F band would lead to a faster lifecycle, and a more active population, requiring a more consistent use of spraying. In contrast, we may avoid spraying on cooler days due to the limited effectivness of spraying, particularly when the mosquito population is small. Targeted use specifically in areas that have historically had the West Nile Virus presence can be considered instead.
* In examining our spray data set, sprays have largely been applied in September. This might be one big area of improvement for future spray applications, to shift them towards the summer months, when mosquitos are most active.

3. Wind Speed and Drift
* Wind speed should also be considered on the day of application. Wind speed can cause pesticide drift, removing the pesticide fog from its most effective location. Wind speed of the day should be considered during pesticide application. This is especially important in Chicago, which follows a grid layout, allowing buildings to form wind corridors and exacerbating wind effects.
* Conversely, days with no wind speed can be difficult for spray operators, at speeds below 3km/h, spray can evaporate before arriving at the desired destination of application. A light breeze will provide the operator with the knowledge of the pesticide drift.

4. Sprayer Type
* Sprayer machinery can play an important role in the application of pesticides. A fine nozzle sprayer will help to provide a fine dispersion of the pesticide mist, however, hot days and lower humidity can lead to a faster evaporation of smaller droplets. Conversely, larger particle sizes (>200 microns) may survive the heat and be less affected by wind size, but may not be as effective at delivering the pesticide to pests.

5. Pesticide
* The assumption made is that the spray used is the most commonly use spray for fogging the air and targeting adult mosquitoes. However, standing pesticides can also be used in conjunction with air pesticides, targeting difficult to reach or difficult to clear areas with standing water to eliminate mosquito larvae. This would be a far more long-reaching solution, although constant re-application would be required through each rainfall. Therefore, consideration would have to be given according to the frequency of rainfall and the difficulty of application.

### Model 1

#### Costs

1. Spraying

- [Time of spray](https://www.chicago.gov/city/en/depts/cdph/provdrs/healthy_communities/news/2020/august/city-to-spray-insecticide-thursday-to-kill-mosquitoes.html): Weather permitting, the spraying will begin at dusk on August 13th and continue through the night until approximately 1:00 am, with licensed mosquito abatement technicians in trucks dispensing an ultra-low-volume spray. The material being used to control the adult mosquitoes, Zenivex.


- [Spray rate of Zerivex](https://chicago.cbslocal.com/2017/08/30/spray-mosquitoes-far-south-side-west-nile-prevention/): The chemical used is Zenivex, applied at a rate of 1.5 fluid ounces per acre. That measure is approved by the U.S. EPA to control mosquitoes in outdoor residential and recreational areas.


- [Zerivex cost per acre](https://www.centralmosquitocontrol.com/-/media/files/centralmosquitocontrol-na/us/resources-lit%20files/zenivex%20cost%20comparison%20fact%20sheet.pdf): USD0.67 per acre

- Area of Chicago City: estimated to be 145,300 acres based on Google Search

Based on the above, we assume the cost of spray to be USD 0.67 per acre multiplied by the area of Chicago city, which would be at USD $97,351. This accounts for 1 spraying exercise.

If we assume the most aggressive spray strategy and spray every week during the summer months of July, August and September based on our spray effectiveness analysis, then the total cost can be calculated to be USD 1,168,212.

For this scenario, we would need to set aside a budget of about USD 1.17 million to conduct the spraying exercises on an annual basis.

2. Medical Health Costs

- Patients who were hospitalized with acute flaccid paralysis, a partial- to whole-body paralysis caused by WNV infection, had the largest initial and long-term medical costs ([median USD 25,000 and USD 22,000 respectively](https://www.sciencedaily.com/releases/2014/02/140210184713.htm)).


- Number of [human WNV cases](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7241786/) in Chicago region (refer to Table 2): 24 in 2011 and 66 in 2013


- The [CDC site](https://www.cdc.gov/westnile/index.html) shares that while there are no vaccines to prevent or medications to treat WNV in people, about 1 in 5 people who are infected develop a fever and other symptoms and about 1 out of 150 infected people develop a serious, sometimes fatal, illness.  


#### Benefits

In a maximum benefit scenario, we assume that due to our aggressive spraying policy, no one contracted the virus.

Conversely, in a scenario where the spray had not been used, we will use the following costs:

Medical Health Costs - USD 60

  - Number of [human WNV cases](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7241786/) in Chicago region will be taken as the average of cases from 2007-2014 (same as our dataset), without the years of 2011 and 2013, to determine maximal benefit against a programme with no spraying

  - The [CDC estimates](https://www.sciencedaily.com/releases/2014/02/140210184713.htm):
     - Roughly 4 out of 5 people are asymptomatic
     - 1 in 5 people who are infected develop a fever, with a median medical cost of USD 7,500
     - 1 in 150 infected people develop a serious, sometimes fatal, illness incurring long-term median medical costs of a total of USD 47,000.

The medical costs for symptomatically mild to moderate cases are 60/5 * 7500 = USD 90000.0.
The medical costs for symptomatically severe cases, rounding up, are USD 47000.

The total medical costs are USD 137,000

Productivity Loss

Based on [NCBI(National Centre for Biotechnology Information)'s study in determining productivity loss of an individual](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3322011/) , we assume productivity loss to be (referenced from Table 3 in the link):

For the symptomatically mild and moderate cases:
- USD 955 for each individual, for a total of USD 11460


For the hospitalised individual:
- USD 10800, if the individual is under the age of 60

Total productivity loss: USD 22260
The economic loss to WNV can be calculated as USD 159,260.

### Model 2

In our second model, we look to target specific areas of the city, highly affected by the mosquitos, along with the following factors:

- Spray Area: Spray Area imputed from the spray area of the 2011 spray block, an area roughly measuring 12.857 km^2, or 3177 acres.

- Spray Times: Following the EDA done on the weather data set, alongside the features that were deemed to be of the highest importance in the logistic regression, we can see that spraying can be targeted to hit the life cycle of mosquitos immediately after periods that are:
    1. At least 10 days after a light rain or mist event
    2. On days where the degree day value is 7 or higher
    
Assuming this happens 3 times a month (Every 10 days of uninterupted sunshine following a rain event), and only in the months correlated with the highest number of cases (August, September), we can lower spray frequency to 6 times a year.

Further, from our EDA, only 18 of the 64 blocks in the train set had WNV counts above 10 for the last 4 years, more than 2.5 cases per year per block.

Therefore, we would restrict our spraying to only the regions that would benefit the most.

At a rate of:
* 6 sprays a year
* For 18 blocks * 3177 acres * USD 0.67 per acre

The total cost of Model 2 would be USD 229887.72

At USD 230,000, this spray plan is remains higher than the loss estimated of USD 159,260.

## Recommendations

In conclusion, while a model that included indiscriminate spraying through Chicago did not show material benefit when compared to the cost, a model that was calculated based on initial features discovered during EDA and examined after modeling did product a spray plan that was more expensive than the economic loss estimated.

This model was however based on a worst case scenario of 6 sprays. When adjusted by the weather for the year, it will likely reduce the reliance of such a high spray count. Further streamlining of the model could be done by looking at the month of June as a lead up, to help determine the severity of the mosquito population for the year.

That said, the [best and most economical way](https://www.cdc.gov/westnile/prevention/index.html) to prevent West Nile disease or any other mosquito-borne illness is likely education of the populace, to reduce the number of mosquitoes. Precautions recommended by the CDC include:

- When outdoors, apply insect repellent that contains DEET, picaridin, oil of lemon eucalyptus or IR 3535, according to label instructions.
- Wear long-sleeved shirts and long pants when going out
- Make sure doors and windows have tight-fitting screens. Repair or replace screens that have tears or other openings. Try to keep doors and windows shut, especially at night.
- Eliminate sources of water-holding containers that can support mosquito breeding such as tires, buckets, planters, toys, pools, birdbaths, flowerpots, or trash containers
- In communities where there are organized mosquito control programs, contact your municipal government to report areas of stagnant water in roadside ditches, flooded yards and similar locations that may produce mosquitoes.

## Conclusion
Some things to consider in a follow-up model or test sets, would include data on the following:
- Use models with class weights. This will penalise the misclassifications made by the minority class by setting a higher class weight , and at the same time, reducing weight for the majority class. Penalising mistakes will put more emphasis on the misclassifed class.
- Consider other approaches in dealing with imbalanced classification, such as ADASYN
- Collect more data to balance classes within the dataset.


Presentation slides can be found [*here*](https://docs.google.com/presentation/d/1mcq-PWQ7iOgGA75zJQiJCC4yx7CGViAl/edit?usp=sharing).
=======
**This is also where you will be submitting your code for evaluation**. The public leaderboard uses roughly 30% of the dataset to score an AUC (Area Under Curve) metric.

> If you do not already have a Kaggle account, you will need to sign up on the website.  Also note that you will be submitting a "Late Submission" on Kaggle because the official competition has ended.  You can use the leaderboard to see how your results compare against roughly 1300 other data science teams!

You can submit predictions as many times as you want to Kaggle, but there is a limit of 5 submissions per day.  Be intentional with your submissions!


#### Navigating Group Work

This project will be executed as a group.  To make your team as effective and efficient as possible you should do the create a shared GitHub repo and project planning document as described in the deliverables section below.

## Deliverables

**GitHub Repo**

1. Create a GitHub repository for the group. Each member should be added as a contributor.
2. Retrieve the dataset and upload it into a directory named `assets`.
3. Generate a .py or .ipynb file that imports the available data.

**Project Planning**

1. Define your deliverable - what is the end result?
2. Break that deliverable up into its components, and then go further down the rabbit hole until you have actionable items. Document these using a project managment tool to track things getting done.  The tool you use is up to you; it could be Trello, a spreadsheet, GitHub issues, etc.
3. Begin deciding priorities for each task. These are subject to change, but it's good to get an initial consensus. Order these priorities however you would like.
4. You planning documentation (or a link to it) should be included in your GitHub repo.

**EDA**

1. Describe the data. What does it represent? What types are present? What does each data points' distribution look like? Discuss these questions, and your own, with your partners. Document your conclusions.
2. What kind of cleaning is needed? Document any potential issues that will need to be resolved.

**Note:** As you know, EDA is the single most important part of data science. This is where you should be spending most of your time. Knowing your data, and understanding the status of its integrity, is what makes or breaks a project.

**Modeling**

1. The goal is of course to build a model and make predictions that the city of Chicago can use when it decides where to spray pesticides! Your team should have a clean Jupyter Notebook that shows your EDA process, your modeling and predictions.
2. Conduct a cost-benefit analysis. This should include annual cost projections for various levels of pesticide coverage (cost) and the effect of these various levels of pesticide coverage (benefit). *(Hint: How would we quantify the benefit of pesticide spraying? To get "maximum benefit," what does that look like and how much does that cost? What if we cover less and therefore get a lower level of benefit?)*
3. Your final submission CSV should be in your GitHub repo.

**Presentation**
* Audience: You are presenting to members of the CDC. Some members of the audience will be biostatisticians and epidemiologists who will understand your models and metrics and will want more information. Others will be decision-makers, focusing almost exclusively on your cost-benefit analysis. Your job is to convince both groups of the best course of action in the same meeting and be able to answer questions that either group may ask.
* The length of your presentation should be about 10 minutes (a rough guideline: 1 minute intro, 5 minutes on model, 2 minutes on cost-benefit analysis, 2 minute recommendations/conclusion).  Touch base with your local instructor... er, manager... for specific logistic requirements!

---

**Your project is due at 13 Aug 2021 09:00AM.**

---

### Project Feedback + Evaluation

For all projects, students will be evaluated on a simple 4 point scale (0-3 inclusive). Instructors will use this rubric when scoring student performance on each of the core project requirements:

Score | Expectations
----- | ------------
**0** | _Does not meet expectations. Try again._
**1** | _Approaching expectations. Getting there..._
**2** | _Meets expectations. Great job._
**3** | _Surpasses expectations. Brilliant!_

### Rubric

Your final assessment ("grade" if you will) will be calculated based on a topical rubric (see below).  For each category, you will receive a score of 0-3.  From the rubric you can see descriptions of each score and what is needed to attain those scores.

For Project 3 the evaluation categories are as follows:
- [Organization](#organization)
- [Data Structures](#data-structures)
- [Python Syntax and Control Flow](#python-syntax-and-control-flow)
- [Probability and Statistics](#probability-and-statistics)
- [Modeling](#modeling)
- [Presentation](#presentation)

#### Organization

Clearly commented, annotated and sectioned Jupyter notebook or Python script.  Comments and annotations add clarity, explanation and intent to the work.  Notebook is well-structured with title, author and sections. Assumptions are stated and justified.


| Score | Status                     | Examples                                                                                                                                                                                                                                         |
|-------|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Does not Meet Expectations | 1. Comments and annotations are **absent** <br> 2. There is no clear notebook structure <br> 3. Assumptions are not stated                                                                                                                                       |
| 1     | Approaching Expectations   | 1. Comments are present but generally unclear or uninformative (e.g., comments do not clarify, explain or interpret the code) <br> 2. There are some structural components like section/subsection headings <br> 3. Assumptions are stated but not justified |
| 2     | Meets Expectations         | 1. Comments and annotations are clear and informative <br> 2. There is a clear structure to the notebook with title and appropriate sectioning <br> 3. Assumptions are both stated and justified                                                             |
| 3     | Exceeds Expectations       | 1. Comments and annotations are clear, informative and insightful <br> 2. There is a helpful and cogent structure to the notebook that clarifies the analysis flow <br> 3. Assumptions are stated, justified and backed by evidence or insight               |

#### Data Structures

Python data structures including lists, dictionaries and imported structures (e.g. DataFrames), are created and used correctly.  The appropriate data structures are used in context.  Data structures are created and accessed using appropriate mechanisms such as comprehensions, slices, filters and copies.

| Score | Status | Examples |
|-------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 | Does not Meet Expectations | 1. Appropriate data structures are not identified or implemented <br> 2. Data structures are not created appropriately <br> 3. Data structures are not accessed or used effectively |
| 1 | Approaching Expectations | 1. Contextually appropriate data structures are identified in some but not all instances <br> 2. Data structures are created successfully but lacked efficiency or generality (e.g., structures were hard-coded with values that limits generalization; brute-force vs automatic creation/population of data) <br> 3. Data structures are accessed or used but best practices are not adopted |
| 2 | Meets Expectations | 1. Contextually appropriate data structures are identified and implemented given the context of the problem <br> 2. Data structures are created in an effective manner <br> 3. Data structures are accessed and used following general programming and Pythonic best practices |
| 3 | Exceeds Expectations | 1. Use or creation of data structures is clever and insightful <br> 2. Data structures are created in a way that reveals significant Pythonic understanding <br> 3. Data structures are used or applied in clever or insightful ways |


#### Python Syntax and Control Flow

Python code is written correctly and follows standard style guidelines and best practices.  There are no runtime errors.  The code is expressive while being reasonably concise.

| Score | Status | Examples |
|-------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 | Does not Meet Expectations | 1. Code has systemic syntactical issues <br> 2. Code generates incorrect results <br> 3. Code is disorganized and needlessly difficult |
| 1 | Approaching Expectations | 1. Code is generally correct with some runtime errors <br> 2. Code logic is generally correct but does not produce the desired outcome <br> 3. Code is somewhat organized and follows some stylistic conventions |
| 2 | Meets Expectations | 1. Code is syntactically correct (no runtime errors) <br> 2. Code generates desired results (logically correct) <br> 3. Code follows general best practices and style guidelines |
| 3 | Exceeds Expectations | 1. Code adopts clever or advanced syntax <br> 2. Code generates desired results in an easily consumable manner (e.g., results are written to screen, file, pipeline, etc, as appropriate within the flow of the analysis) <br> 3. Code is exceptionally expressive, well formed and organized |


#### Probability and Statistics

Descriptive and inferential statistics are calculated and applied where appropriate.  Probabilistic reasoning is demonstrated.  There is a clear understanding of how probability and statistics affects the analysis being performed.

| Score | Status | Examples |
|-------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 | Does not Meet Expectations | 1. Descriptive statistical calculations are absent <br> 2. Inferential statistical calculations are absent <br> 3. Probabilities or statistics are not relevant given the context of the analysis |
| 1 | Approaching Expectations | 1. Descriptive statistics are present in some cases <br> 2. Inferential statistics are present in some cases <br> 3. Probabilities or statistics are somewhat relevant to the analysis context |
| 2 | Meets Expectations | 1. Descriptive statistics are calculated in all relevant situations <br> 2. Inferential statistics are calculated in all relevant situations <br> 3. Probabilities or statistics are relevant to the analysis |
| 3 | Exceeds Expectations | 1. Descriptive statistics are calculated, interpreted and visualized (where appropriate) <br> 2. Inferential statistics are calculated, interpreted and visualized (where appropriate) <br> 3. Probabilities or statistics are leveraged to draw meaningful or insightful conclusions |

#### Modeling

Data is appropriately prepared for modeling.  Model choice matches the context of the data and the analysis.  Model hyperparameters are optimized.  Model evaluation is robust.  Model results are extracted and explained either visually, numerically or narratively.

| Score | Status | Examples |
|-------|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 | Does not Meet Expectations | 1. Data is not prepared for modeling.<br>2. Models are not implemented or not implemented fully.<br>3. Model hyperparameters are not considered.<br>4. Model evaluation is not performed.<br>5. Model results are unavailable or not extracted. |
| 1 | Approaching Expectations | 1. Data has some null values, inappropriate types and/or improper handling of categorical labels.<br>2. Model choice is questionable given the objective of the analysis.<br>3. Model hyperparameters are insufficiently or not optimized.<br>4. Model evaluation is performed but the evaluation is not generalizable.<br>5. Model results are extracted but not explained or interpreted. |
| 2 | Meets Expectations | 1. Data is free from nulls and correctly typed for the given model.<br>2. Model choice is appropriate to the analysis.<br>3. Model hyperparameters are optimally selected.<br>4. Model evaluation reflects generalizeable performance.<br>5. Model results are extracted and explained either visually, numerically or naratively. |
| 3 | Exceeds Expectations | 1. Data is pristinely prepared with creative or useful feature engineering.<br>2. Model selection is justified and demonstrates an awareness of tradeoffs.<br>3. Model hyperparameters are optimized and the optimization is demonstrated/justified.<br>4. Model evaluation reflects generalizable performance and is interpreted in the context of the analysis.<br>5. Model results are explained, interpreted and related to the overarching analysis goals. |


#### Presentation

The goal, methodology and results of your work are presented in a clear, concise and thorough manner.  The presentation is appropriate for the specified audience, and includes relevant and enlightening visual aides as appropriate.

| Score | Status | Examples |
|-------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 | Does not Meet Expectations | 1. The problem was not well explained or ambiguous. <br> 2. The level of technicality was far above or below the target audience. <br> 3. The presentation went substantially over or under time. <br> 4. The speaker's voice was difficult to hear of unclear. <br> 5. The presentation visuals did not seem to support the talk. |
| 1 | Approaching Expectations | 1. The problem was stated but was not 100% clear. <br> 2. The level of technicality was was good at times, but too low or too high at other times given the target audience. <br> 3. The presentation was given went slightly over or under time. <br> 4. The speaker's voice was at times difficult to understand. <br> 5. The presentation visuals were generally helpful, but some of them were either too complex or disconnected from the narrative. |
| 2 | Meets Expectations | 1. The problem was framed appropriately for the audience. <br> 2. The level of technicality was appropriate to the target audience. <br> 3. The presentation was given within the allocated timeframe. <br> 4. The speaker's voice had volume and clarity. <br> 5. The presentation visuals were helpful and supportive. |
| 3 | Exceeds Expectations | 1. The problem was expertly stated and compelling. <br> 2. The level of technicality was perfect for the target audience. <br> 3. The presentation was given within the allocated timeframe and paced evenly throughout. <br> 4. The speaker's voice was clear, understandable and consistent. <br> 5. The presentation visuals provided distinct insight, supported the speaker from the background, and were not distracting. |
>>>>>>> 10756d444d50c74526dcaa9a1e84d338bdaff6a4
