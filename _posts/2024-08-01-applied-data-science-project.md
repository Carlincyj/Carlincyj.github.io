---
layout: post
author: Carlin Chow
title: "Applied Data Science Project Documentation"
categories: ITD214
---
## Project Background
Welcome to my ITD214 Github page! In this space, I would be sharing more about my project titled "British Airways: Improving Customer Experience".

Specifically, my team and I have selected the following dataset from Kaggle which contains customer reviews of British Ariways scrapped from airlinequality from the period 2015 to 2023. There are 19 columns in this dataset (refer to the dataset using this link: https://www.kaggle.com/datasets/chaudharyanshul/airline-reviews
**
Here are the four objectives that we focused on:**
1. To reduce response time by 10% by identifying common complaints through clustering for automation of replies (Yan)
2. To identify areas of customer satisfaction for marketing purposes, to improve business by 10% (Bridget)
3. To analyse review topics for the four different seat types for a more targeted marketing approach, improving business by 10% (Carlin (myself))
4. To reduce negative review sentiments by 10% to improve customer satisfaction and demand (Vivienne)

For my business objective (#3), I aim to make use of Topic Modelling and Sentiment Analysis to analyse common topics of interest for the four different seat types offered on flights by British airways, so that areas of improvement can be addressed / areas done well can be continued. Thereafter, I will present the analyses on which topics are most associated with positive or negative sentiments. 

## Work Accomplished
Document your work done to accomplish the outcome

### Data Preparation
  First, data preparation will be done on this dataset. Prior to my own cleaning, our group has done some data preprocessing on the data. That includes the following:
1. Converting fields into appropriate data types
2. Removal of missing values
3. Conversion to lowercase
4. Removal of punctuation, numbers, stop words and domain stop words
5. N-char less than 3 characters
6. Lemmatization
7. Tokenisation
8. Lemmatization
9. POS Tagging and removal of specific parts of speech

After which, the dataset was cleaned individually. For my Business Objective, the main columns that were essential for the analysis were the following - 'CleanText' (derived from text after cleaning earlier), 'Bigrams', 'Trigrams' and the 'Recommended' columns. Hence, the rest of irrelevant columns were dropped. 

![image](https://github.com/user-attachments/assets/c6137af8-209d-4588-8d5e-91ff57bd712c)


### Modelling
For this business objective, the model of choice was topic modelling. To enhance findings, I had also done an analysis of the bigrams and trigrams related to the topic words churned. 

Topic modelling was done in Jupyter Notebook using LDA. Perplexity scores and coherence scores were calculated to determine the best number of topics to input for the modelling process. Based on the scores, topic_num = 20 was chosen. 


### Evaluation
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce bibendum neque eget nunc mattis eu sollicitudin enim tincidunt. Vestibulum lacus tortor, ultricies id dignissim ac, bibendum in velit. Proin convallis mi ac felis pharetra aliquam. Curabitur dignissim accumsan rutrum. In arcu magna, aliquet vel pretium et, molestie et arcu. Mauris lobortis nulla et felis ullamcorper bibendum. Phasellus et hendrerit mauris. Proin eget nibh a massa vestibulum pretium. Suspendisse eu nisl a ante aliquet bibendum quis a nunc. Praesent varius interdum vehicula. Aenean risus libero, placerat at vestibulum eget, ultricies eu enim. Praesent nulla tortor, malesuada adipiscing adipiscing sollicitudin, adipiscing eget est.

## Recommendation and Analysis
Based on the top 5 topics (specific words) of interest, further evaluation was done through additional analysis of the bigrams and trigrams columns. Some findings from the evaluation for the 4 seat types to improve British Airways service are as follows (examples):

Economy Class: bad customer service, exit row seat, take long time

Premium Economy: one hour delay, last time fly

Business Class: middle seat block

First Class: one hour delay


Based on reviews, customers had following (examples of) positive remarks of some of the following topic words:

Economy Class: leg room (enough, plenty, good)

Premium Economy: food pretty good, seat comfortable good, cabin crew efficient

Business Class: new seat comfortable

First Class: lounge excellent service



## AI Ethics
For this project, one ethical consideration that would be most straightforward would be the annonymisation of customer reviews. During processing of the dataset, the names of customers were removed to ensure privacy. This ensures that confidentiality was maintained for the study,

Finally, transparency of project is made clear, as the ways of conducting the analysis were documented step by step and explained in detail. This would allow the audience to be clear of procedure and variables involved. This enables openness between data manager and the stakeholders, so that recommendations made subsequently are with basis. For the topic modelling portion, topic modelling was done on four separate datasets that was split from the original dataset, thus eliminating any biases or overgeneralisation of issues or areas performed well by the airline. 

## Source Codes and Datasets
Upload your model files and dataset into a GitHub repo and add the link here. 

GitHub repo - https://github.com/Carlincyj/ITD214_project
