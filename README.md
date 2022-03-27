
# Analyzing the Sentiment Distribution of Tweets about the War in Ukraine
Using Natural Language Processing and Sentiment Analysis, tweet data on the War in Ukraine was analyzed.

## Background

### Social Media Analytics (SMA)
Social Media Analytics is used to collect data from various social media websites and evaluate the data effectively, in order to make business as well as logical decisions, based on the data received from end users. Social media is a great platform to understand the end user's sentiments, opinions and choices. SMA is used to analyze the customer's opinions on an emotional level to better understand the public opinion and analyze the polarity in events and issues of concern.

### What is Sentiment Analysis?
Sentiment Analysis, also known as Opinion Mining, is a popular data mining approach used to study the inclination of people's views, sentiments, evaluations, opinions and emotions towards any products, global issues, events, services and organizations to name a few. These opinions are measured through Natural Language Processing(NLP), text analysis, Machine learning and other computational linguistics. Sentiment distribution is widely used to analyze the reaction of people and reveal the contextual polarity of the information used.

### Why Sentiment Analysis?
Sentiment Analysis is an important way to understand the audience and hence make business or corporate decisions based on the analysis performed on people's opinions. Understanding the people's thought process and needs can help companies and organizations understand what to expect in terms of business and upcoming trends. Based on the results, one can get a direction on how to understand their potential market. Sentiment Analysis provides real time analysis to keep organizations updated all the time. Identifying positive, neutral and negative comments help in audience engagement and better understanding of emotional as well as business aspects of audience in general. 

![twitter sentiment analysis dia1](https://user-images.githubusercontent.com/23488019/158078675-df77b237-3077-451d-888d-acaf958fda8a.png)

### Setbacks of Sentiment Analysis
Sentiment Analysis is a popular way, companies can get information regarding public opinion and their inclination towards or against issues. However, it is not perfect, since there can be discrepancies in the data accumulated and this can lead to minor to major changes in the final result analysis. Few of the major hurdles in performing sentiment analysis are discussed below:
1. Tone of people's voice - The tone of people's voice can sadly not be identified 100% of the times. Sarcasm and irony can be misinterpreted and misevaluated and end up getting categorized incorrectly. This problem can be difficult for humans to decipher in day-to-day lives, let alone any algorithm. 
2. Emojis - Wrong use of emojis for sentiment expression can end up in getting skewed results. Sometimes, people can get confused with what emotion an emoji actually represents and hence alter the sentiment altogether. 


## Overview
The main goal of the present project was to identify the sentiments Twitter users have about the war in Ukraine.

On February 24, 2022, Russia invaded Ukraine demanding an assurance that Ukraine will never join NATO. Over a dozen cities and towns were attacked, including the capital city, Kyiv (Source: [NYTimes](https://www.nytimes.com/interactive/2022/world/europe/ukraine-maps.html?searchResultPosition=3))

Since then, there have been tensions between countries, in particular with the United States and European Union supporting Ukraine, and Russia counting with Venezuela and Syria as allies (Source: [NYTimes](https://www.nytimes.com/2022/03/05/world/americas/venezuela-russia-usa.html?searchResultPosition=1)). These tensions, according to media channels and specialists, can potentially escalate the Ukrainian war to a third world war.

Besides the threat of worldwide conflict, other impacts of the Russian invasion on Ukraine has already been observed. The most prominent impact is Ukrainians’ migration to neighboring countries, such as Poland, Hungary and Slovakia. Specialists have been calling it a major refugee crisis, as of March 11 over two and a half million Ukrainians have fled their homes (Source: [The UN Refugee Agency](https://data2.unhcr.org/en/situations/ukraine#_ga=2.200929772.353981607.1646674903-2007428328.1646674903)).

Given the direct or indirect impact of the war in Ukraine to people’s lives, it is worthwhile to assess the sentiments people have about this event. Sentiments were identified through text data, consisting of over one million tweets downloaded from February 26 to March 10, 2022. Data was sourced from [Kaggle](https://www.kaggle.com/bwandowando/ukraine-russian-crisis-twitter-dataset-1-2-m-rows/discussion/310030). The dataset administrator used three processes to collect data:

- Process 1 hashtags: "#SlavaUkraini OR #Russia OR #RussiaUkraineWar OR #Putin OR #RussiaUkraine OR #RussianWar OR #ww3 OR #moscow OR #RussianConflict"
- Process 2 hashtags: "#ukraineunderattack OR #Ukriane OR #Ukraine OR #RussianUkrainianWar OR #UkraineRussia OR #UkraineConflict OR #UkraineWar OR #Kharkiv OR #StopPutinNow"
- Process 3: Geolocation UKRAINE country.

Through the examination of tweet data, the following questions will be answered:

1. **What are the most common words mentioned on twitter about the Ukrainian war**?
2. **What is the sentiment breakdown for Ukraine war tweets**?
3. **How sentiment polarity changes over time**?
4. **Do sentiment distributions change according to country**?
5. **Is polarity related to the number of casualties in the war**?
6. **How accurate are Machine Learning models in predicting polarity based on tweet text**?

### Description of the communication protocols
The group has created a GitHub repository with 4 different branches for each member to work on their own branch. The 4 branches that have been created are as follows:

1. week_2_deliverables_AD : Branch for Ana Duchini
2. week_2_deliverables_AS : Branch for Aakriti Sharma
3. week_2_deliverables_FM : Branch for Flora Matos
4. week_2_deliverables_rk : Branch for Ruchika Kulkarni

Each group member has worked in a specific project task and the whole group has been communicating through slack and meeting every two days via zoom.

## Technologies Used
### A.  Data Cleaning and Analysis
Pandas in Python will be used to clean the data and perform an exploratory analysis. Further analysis will be completed using Python. A number of different libraries that were used for our project are described below:

#### 1. Sentiment Analysis using Vader
The VADER (Valence Aware Dictionary for sEntiment Reasoning) sentiment analysis model, relies on a dictionary that maps words and other lexical features common to microblogs. F1 scores have been calculated to approach 0.95 ([see research paper](https://www.researchgate.net/publication/275828927_VADER_A_Parsimonious_Rule-based_Model_for_Sentiment_Analysis_of_Social_Media_Text)). It provides positive, neutral, and negative scores, which are ratios for proportions of text that fall in each category (so they add up to 1), as well as a compound score normalized between -1 and 1. 
The Heuristics of VADER are:
1. Punctuation
2. Capitalization
3. Degree modifiers (also called booster words) 
4. Polarity shift due to Conjunctions
5. Catching Polarity Negation

#### 2. Sentiment Analysis using TextBlob
It is a Python library for text processing. It is used in performing Natural Language Processing tasks such as sentiment analysis, classification, translation, parts of speech tagging and phrase extraction. 

Anaconda prompt will be used to install all the Python libraries. 

### B.  Database Storage
The final data is exported to SQLite for later access. [Current zipped version can be found here](resources/data set/tweets_data.sqlite.zip). The [schema used can be found here](resources/schema.sql)

### C.  Machine Learning
SciKitLearn is the Machine Learning library we'll be using to create a classifier. Our training and testing setup is 

### D. Data Visualization
Tableau will be used to graphically depict our results and chart the visualizations. 

### E.  Dashboard
In addition to using a Flask template, we will also integrate D3.js for a fully functioning and interactive dashboard. HTML, Bootstrap CSS will be used to create a webpage where we will have the dashboard for all our findings and sentiment analysis. 

### Preprocessing Data

The raw data file contains more than 1.2 million rows and 18 columns of twitter data from all over the world, in 64 different languages. For the purpose of this project, only English tweets were extracted from the data set for the analysis. The number of English tweets are further divided into smaller data sets on the basis of the location of the tweets i.e. data sets from different countries.

The first step in cleaning the data, is to identify the most relevant data, extract it and clean it. As far as sentiment analysis is concerned, the most relevant data in the entire data set is the tweeted text in the 'text' column. For cleaning, the tweets were extracted into a dataframe. To evaluate sentiments, tweets need to contain pure text in lower case. The numbers, hashtags, emojis, hyperlinks are removed with the help of regex (regular expressions) and pandas functions. Once free of all the noise, the data are stored in the form of a csv file for further analysis. The details of cleaning operations can be viewed in the Sentiment_Analysis_Data_Cleaning.ipynb


## Results

### Natural Language Processing (Exploratory Data Analysis)
- Extract preprocessed data from database
- Use NLP to turn unstructured text into machine-usable code by:
	- Tokenization
	- Lemmatization and Stemming?
	- Removing stop words
	- Can use bag-of-words or tf-idf to get word frequency [*still left to decide best approach*]
Pipeline steps to follow (could use separate notebooks for each step):
1. Raw Text: Start with the raw data, then clean it up.
2. Tokenization: Separate the words from paragraphs or sentences, into individual words.
3. Stop Words Filtering: Remove common words like "a" and "the" that add no real value to what we are looking to analyze.
4. Term Frequency-Inverse Document Frequency (TF-IDF): Statistically rank the words by importance compared to the rest of the words in the text. This is also when the words are converted from text to numbers.
5. Machine Learning: Put everything together and run through the machine learning model to produce an output.
*** NLP packages: NLTK, SpaCy, Gensim, Scikit-Learn
*** Key areas of NLP: LDA, TF-IDF, embedding techniques (i.e. word2vec, doc2vec), neural architectures (i.e. CNN, RNN, attention, Seq2Seq)


## Project Pipeline :

![project pipeline](https://user-images.githubusercontent.com/23488019/158079683-59057a33-11ee-42c4-bcac-af917b35b83d.PNG)
 
 
## Summary
 The steps for the analysis are as follows:
 1. **Collecting Data**: From [Kaggle dataset](https://www.kaggle.com/datasets/bwandowando/ukraine-russian-crisis-twitter-dataset-1-2-m-rows)
 2. **Preprocessing Data**: (data cleaning, filter by English language, and selected countries) [Twitter_Vader_Sentiment_Analysis_Data_Cleaning.ipynb](Twitter_Vader_Sentiment_Analysis_Data_Cleaning.ipynb). Due to the size of each dataset collected by ranges of dates, each file was processes separately, and later consolidated for analysis.
 3. **Sentiment Analysis**: Using [VADER](Twitter_Vader_Sentiment_Analysis_Data_Cleaning.ipynb). A compound score is calculated. This is converted into overall 'positive','negative' or 'neutral' values, and aggregated to each tweet data.
 4. **Machine Learning Model**:
  Evaluated various models in [Machine_Learning](Machine_Learning.ipynb), where a function was created to compare the accuracy of 4 models: Random Forest, Naive Bayes, Logistic Regression, and Linear SVC.
 7. **Data Visualizations**: A working presentation has been added to [Google docs](https://docs.google.com/presentation/d/1uzYRtAgBxeyVoteSkImERVQHtRtEBiBFCAVat05HdC0/edit?usp=sharing)
 8. **Database**: The data has been loaded to a SQLite database using [this notebook](SQL_database.ipynb). A copy of the output can be found in [Google Drive](https://drive.google.com/file/d/152mxp0DtOWYw0seek4LncegdKDTBk65C/view?usp=sharing) using the following [schema](resources/schema.sql), as laid out below:
 ![screenshot of schema](resources/images/schema.png)
 9. **Deploying the model and visualizations at the web app** (in progress). Working [Tableau file can be found here](Ukraine_analysis.twb). It uses the SQLite data referenced above. 

![Diagram of the process steps](resources/images/flowchart.png)
*Diagram of the steps followed and the files involved*


