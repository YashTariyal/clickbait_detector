# Clickbait Detector

Through NLP and text classification, this project aims to classify a headline as clickbait or non-clickbait.  

Clickbait refers to an article headline whose purpose is to use sensationalist language to lure in a viewer to click through to a certain webpage. That webpage typically generates ad revenue on the user's clicks or monitizes the user's activity data. The clickbait article itself is not written with journalistic integrity, research or really any deeper or practical meaning - it is simply a vehicle to grab clicks and activity.

With the explosion of social media, smartphones and so many people connected to the internet daily, there is no shortage of ‘information' and online objects vying for our attention, but all are not equal. The ease of sharing and reposting on social media has allowed clutter like clickbait to run wild. And the often profitable nature of publishing and capitalizing on clickbait has also given way to the increase in clickbait.

With clickbait becoming increasingly common and, generally considered as a nuisance, I wanted to see if a headline could be classified using machine learning and what that looks like.

#### Possible Stakeholders:
This could be implemented on a larger scale - on social media/various websites, as a 'clickbait blocker', and clickbait could be flagged or filtered out as such.

## The Dataset
52,000 headlines from clickbait and non-clickbait sources from roughly around 2007 - 2020 .
- 30,000: 2007 - 2016 headlines from https://www.kaggle.com/amananandrai/clickbait-dataset
- 22,000: 2019 - 2020 headlines that I scraped/requested from Twitter, APIs, online publications.

Clickbait sources: Buzzfeed, Upworthy, ViralNova, BoredPanda, Thatscoop, Viralstories, PoliticalInsider, Examiner, TheOdyssey

Non-clickbait sources: NY Times, The Washington Post, The Guaridan, Bloomberg, The Hindu, WikiNews, Reuters

## Process

1. Gather Data.
2. Clean and process data, including feature engineering.
3. Explore data through EDA for initial insights and understanding.
4. Model & Evaluate : train classifiers and evaluate test predictions.  Interpret model performance.

## EDA 

- Visualized word frequency for each class.
- Visualized distribution of engineered features and their relevance on each class.
- Target distribution

![](/images/classes.png)




## Conclusion

I was able to use machine learning algorithms such as Naive Bayes, Logistic regression and SVM to accurately classify clickbait versus non-clickbait headlines. The results were quite good - within the 90-93% range for accuracy scores and 90-93% range for recall scores. I slightly prioritized recall as I figured that it would be more valuable to minimize false negatives (classifying clickbait as non-clickbait).

As machine learning was able to work so well, there is definitely a real world use case for deploying a machine learning solution to filter out / flag clickbait before a reader even has to visualize and discern the headline for themselves!

By analyzing the coefficients of the models that performed the best, I was able to interpret and get some insight into how the models determined if a headline is clickbait or not.

## Next Steps/Future Improvement Ideas

- explore Deep NLP and neural net models to see if they make a stronger classifier
- set up a front end / app using Flask to predict on new headlines in a current day scenario
- analyze topics and themes with LDA
- possibly use LDA topics for modeling
- test model on a new dataset

## Presentation link


## Repository Navigation 

1. Data folder - all relevant csv files
2. Working Notebooks folder - scraping & api requests, cleaning & eda , modeling
3. Final_mvp.ipynb - final notebook showcasing the end to end project.
4. README - end to end project report, reproduction instructions, repository navigation, link to presentation, sources.


## Reproduction Instructions

1. First, start with the cleaning&eda notebook under the 'workingnotebooks' folder - this compiles all relevant csvs (found in the data folder) and sets up the data for the project.  Feature engineering code is located here and processing for EDA is also found here.
2. Second, the modeling notebook (in working notebooks) - the code here can be reproduced to further process the data for modeling and then creating/evaluating your classifiers.
3. Third, the final_mvp notebook gives an overview of my whole process - this notebook can be used for a clear picture of the end to end process but areas like data cleaning are just explained in markdown so utilize the working notebooks for all details. 
