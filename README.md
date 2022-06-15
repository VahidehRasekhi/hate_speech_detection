## Project Title 
Offensive Speech Detection on Twitter 


## Description
The increase in online offensive speech is a major issue in modern society, as it can result in crime against people from different races, religions, political affiliations, etc. Therefore, it is crucial for social media to detect and remove offensive language immediately.  

In this study, I focus on detecting offensive language in Twitter using NLP and Machine Learning models. I use a publicly avaialble dataset with labels (offensive and non-offensive). I apply different machine learning models in order to determine which model is the best in classifying tweets as offensive and non-offensive. It is important that the model classifies tweets accurately because inaccurate generalizations would lead to non-offensive tweets to be flagged and removed from Twitter. For instance, the model might classify comments that refer to certain commonly-attacked groups (e.g., gay, Muslim, black, etc.) as offensive while the comment is not offensive at all.


## Motivation
With the advancement of technology and easy access to internet, people all over the world have been using social media such as Twitter, Facebook, YouTube, to express their opinions and share information. Even though these platforms have been useful in quickly spreading information to people in different parts of the world, they have also been exploited as platforms for spreading offensive language, hate speech, racism, intolerance, etc. 

In this project, offensive language referrs to any comment that attacks, ridicules, or intimidates someone based on their culture, ethnicity, race, religion, gender, sexual orientation, and disability. 


## Goals
* The first objective of this study is to determine which machine learning models are the best in offensive language classification.

* The second objective is determining the keywords/phrases the models use for this classification.


## Data
Data for this study comes from:
https://github.com/ManishShettyM/Offensive-Text-Detection


## Data Prepration
* Tweets were cleaned by removing punctuation, stop words, urls, mentions, hashtags, capitalization.

* They were also lemmatized, tokenized, and vectorized. 


## Data Analysis
* Data cleaning and analysis were done in Python.

* There are 31,930 tweets in the training dataset. I split it to train (85%) and development (15%) dataset. 

* Two types of machine learning techniques were applied:

### 1. Unsupervised Learning
#### Topic Modeling 
In order to understand what topics people were tweeting about, I ran topic-modeling, which automatically analyzes text data to determine cluster words for a a set of tweets. The results showed that in general, we have 3 topics: 
* left wing politics, blm 
* Trump, white establishment
* Racisim, Islam

### 2. Supervised Learning:
#### Bag of words/Count vectorizer approach:
    * Naive Bayes
    * Logistic Regression
    * Random Forest 
    * Decision Tress
     
#### Sequential approach:
    * LSTM and CNN

#### Model Performance 
Overall models with bag of words approach performed better. The best models are:

* Bag of words approach: Naive Bayes (F1-score= 88%) and Random Forest(F1-score=87%)
* Sequential approach: CNN (F1-score= 66%)

## Insights
#### Based on Logistic Regression Coefficient, the top 8 words that increase the chance of a tweet being classified as offensive are:
* allahsoil (reference to Islam) 
* racism/racist/race 
* white (reference to white establishment/supremist)
* bigot
* Trump 
* blm 
* women 
* misogyny/misogynist

#### There are two main issues with detecting offensive language: 

  a) Rater inconsistency in data labeling; some tweets are labeled offensive while they are non-offensive. 

  b) Models underperform because:
  * they can’t understand the context and just focus on individual words and phrases 
  * the key words can be misspelled on purpose
  * the key words can also be written as separate letters


## Author
Vahideh Rasekhi

Email: vrasekhi@gmail.com

LinkedIn: https://www.linkedin.com/in/vahideh-rasekhi-phd/


## Acknowledgments
I would like to thank the instructor of the Data Science Bootcamp at Nashville Software School, Michael Holloway, and the teaching assistants, Veronica Ikeshoji-Orlati and Alvin Wendt. 


