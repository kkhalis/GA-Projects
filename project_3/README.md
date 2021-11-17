# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Web APIs & NLP

---

# Problem Statement

An investment company is looking to collate a list of posts on reddit for investment-related trends, which they can recommend the type of investment to a client or user based on their comments. Noting that the comments are mostly from retail investors discussing between stocks and cryptocurrency, they want to classify these comments accordingly. The company has commissioned you to build a classification model based off subreddits specifically from r/CryptoCurrency and r/stocks, to help train and build the model to classify these comments to the correct topic. This would allow the the company to suggest the correct type of investments a client should make based on their comments.

- Scrape sample comments off subreddits r/CryptoCurrency and r/stocks
- To build a classification model that can classify the subreddits with minimal misclassifications

## Contents
Part 1: Web Scraping
Part 2: NLP
* Data Import and Cleaning
* Exploratory Data Analysis
* Modelling
* Evaluation
* Conclusion

## Datasets
2 datasets have been used for this project as shown below:

* [`cryptocurrency.csv`](./datasets/cryptocurrency.csv): scraped subreddit data from r/CryptoCurrency
* [`stocks.csv`](./datasets/stocks.csv): scraped subreddit data from r/stocks

## Data Dictionary

Provided below is a data dictionary of the dataset. Do note that we will only use 4 features from the datasets.

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**subreddit**|*object*|cryptocurrency.csv/stocks.csv|Subreddit category of post|
|**selftext**|*object*|cryptocurrency.csv/stocks.csv|Details of post in subreddit|
|**title**|*object*|cryptocurrency.csv/stocks.csv|Title of post in subreddit|
|**author**|*object*|cryptocurrency.csv/stocks.csv|Author of post in subreddit|

---

## Evaluation

### Evaluation of Chosen Model vs Random Forest

We can see the results of our models' performance on the test data below. For the purposes of this project, I will focus on comparing between our top model of choice and Random Forest Classifier, based on the ROC AUC score, followed by their Sensitivity and their Specificity. This is because we'd want our models to have less false positive and false negatives, so that we do not wrongly provide wrong news and trends to our client.

Any errorneous classifications would most likely result the wrong recommendation of investment to a client, regardless for CryptoCurrency or stocks purposes. We can see that our Random Forest model results in a high false positive rate, but has a lower false negative rate as compared to our Naive Bayes model.

Although the Naive Bayes model may have good scores, our Random Forest model shows a high amount of specificity, which shows that it classified most of the subreddits related to stocks pretty well. Our Random Forest model also has a high ROC AUC score, which indicates it is able to distinguish between CryptoCurrency and stocks.

### Misclassification Analysis

Collecting the commonly misclassified subreddits, we see that some posts are filled with repeated texts to meet the word count limit in a post. We also see a post with text written as `geslner as voldemort`, which is likely representative of Gary Gensler, the Chairman of the U.S Securities and Exchange Commission and his comments on the recent stock shorting of Gamestop by retail investors. However, it is not indicative of which classification this subreddit should belong to. This suggests that some subreddit posts are fueled by events, which don't usually describe much with relation to the classification.

There are also subreddits describing about their mining rig builds, which are more of computer hardware specifications in nature, but no keywords related to cryptocurrency. It is possibly conclusive that the word `mining` can refer to various meanings, notably one subreddit related to the mining industry, particularly in copper, being heavily impacted due to the pandemic, which would be stock-related instead.

Some subreddits also have no keywords or indication with relation to our subreddits. For example, the quoted subreddit below carry hints of frustration for the imposing of tax-reporting requirements for cryptocurrency brokers at the upcoming infrastructure bill to be passed in the U.S.<sup>1</sup><sup>2</sup>

>Here is a quick article on democrats that are opposed to the infrastructure bill, pay attention. If these are you representatives call them, let them know they WILL receive your votes to keep them in office. And those for the bill, that they will NOT be staying in office. It's time to take the power back guys: 
"Republicans have publicly indicated they'll back the bipartisan bill:Â Reps. Brian Fitzpatrick (Pa.), the co-chair of the bipartisan Problem Solvers Caucus, as well as Adam Kinzinger (Ill.), Tom Reed (N.Y.) andÂ Fred UptonÂ (Mich.)"<sup>3</sup>


There are also investing jargons that are frequently and interchangeable used between both subreddits. We see occurences of `ath` (all time highest), `dyor` (do your own research). Some subreddits in stocks that mention about cryptocurrency as a form of investment, which might be confusing in terms of classification for our models. We also see common phrases that are more used for positivity towards a particular stock or cryptocurrency, such as `this is the way`, which usually doesn't contribute much to our classification needs and introduces noise instead.

On reviewing of the the results mentioned above, the recommended model to use would be the TfidfVectorizer Naive Bayes model. The scores of its sensitivity, specificity and misclassification rate would minimise future similar datasets for classification, as compared to the Random Forest, which might incur more false positives in the long run.



**Citations**
<br>
<sup>1</sup> https://apnews.com/article/technology-joe-biden-business-bills-cryptocurrency-92628a41124230448f65fdeb89ffad7d
<br>
<sup>2</sup> https://www.cnbc.com/2021/08/11/crypto-lawmakers-fought-over-the-infrastructure-bill-heres-whats-next.html
<br>
<sup>3</sup> https://thehill.com/homenews/house/573409-whip-list-how-house-democrats-say-theyll-vote-on-infrastructure-bill

---


## Conclusion and Learnings
Setting random seeds to provide an apple-to-apple comparison between models can affect model performance and metric scores. Prior to setting random seeds for comparison, I noted ExtraTrees performing excessively well. However, the accuracy dropped by 10% on adding random_state=42. This would signify that the model is not robust and may not generalise with new unseen data in the future.

Visibly, it is also noticeable that majority of the top features are related to cryptocurrency, instead of having a balance of features from both subreddits. While our baseline score is based on the equal rows of data from each subreddit, the textual content in each subreddit post has a heavier weightage in terms of providing better feature scores for a more accurate classification model. Although having more data would suggest that the model will improve, having more data also introduces additional noise in the model.

This would also have an added effect on the choice of vectorizers, since CountVectorizer scores features with the highest occurences. This would skew the scores of the features over time, if the text within the subreddits are not of good feature quality.

In terms of classification, scikit-learn also recommends Naive Bayes for classification of text data with less than 100,000 samples.

**Link to slides can be found [*here*](https://docs.google.com/presentation/d/1HepNmKZzzpxKoILoady0c6Q9341WQLLWRjBC98eKhlw/edit?usp=sharing).**