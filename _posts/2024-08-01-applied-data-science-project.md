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
Overall, the steps below have generated insights for bettering the top concerns of passengers who had travelled with British Airways. Specifically, frequent topics from the review ("CleanText") body was extracted using LDA, and picked up to sieve out top bigrams and trigrams for better understanding about reviews on these aspects. 

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

After which, the dataset was cleaned individually. For my Business Objective, the main columns that were essential for the analysis were the following - 'CleanText' (derived from text after cleaning earlier), 'Bigrams', 'Trigrams' and the 'Recommended' columns. Hence, the rest of irrelevant columns were filtered and dropped. 

Tokenization was also done for the TF-IDF process in the later steps.

![image](https://github.com/user-attachments/assets/3dc7797f-a727-4373-b4db-eccde2b12d47)


To provide specific analysis for the four seat types (Economy Class, Premium Economy, Business Class and First Class), the dataset was split into four based on seat type. From there, subsequent steps would be done for each seat type separately.

![image](https://github.com/user-attachments/assets/ee1e1de6-cffd-4048-ac9e-5a0e3a2d276b)


### Modelling
For this business objective, the model of choice was topic modelling. To enhance findings, I had also done an analysis of the bigrams and trigrams related to the topic words churned. 

Topic modelling was done in Jupyter Notebook using LDA. Perplexity scores and coherence scores were calculated to determine the best number of topics to input for the modelling process. Based on the scores, topic_num = 20 was chosen. 

To prepare dataset for topic modelling, TF-IDF was first done.
![image](https://github.com/user-attachments/assets/a64cb410-4154-438a-82f0-75bba90580f6)



Topic Modelling Process

Next, Topic Modelling was done through using LDA function. In this section, I display the LDA done for each of the seat types. 

For Economy Class - 
![image](https://github.com/user-attachments/assets/7bbd2fc5-4661-4a91-905e-3e3dde653a2e)


For Economy Class this was the output obtained

![image](https://github.com/user-attachments/assets/0a64196a-94f7-4622-8f4e-2ce1f54d01ba)

For Premium Economy - 

![image](https://github.com/user-attachments/assets/f0eb14c5-7ccb-4a2d-bfa9-6571a1dc78d8)


For Premium Economy this was the output obtained

![image](https://github.com/user-attachments/assets/d1d0336d-6299-416f-ae08-898f3ab83878)


For Business Class - 
![image](https://github.com/user-attachments/assets/077fffdd-d829-4824-be5b-2aa8595ce9ea)


For Business Class this was the output obtained
![image](https://github.com/user-attachments/assets/14d18817-fc06-4a9d-9b9f-38b9decf89de)


For First Class - 
![image](https://github.com/user-attachments/assets/d902a7b8-02c4-465a-8e3d-e6e44c9ed418)


For First Class this was the output obtained
![image](https://github.com/user-attachments/assets/8d6797ae-1100-4a71-a226-7e5923a2b1f5)

### Evaluation
As topic words may not be sufficient to gain a deeper understanding of these aspects from customer reviews, reference was also done with the top trigrams. In this case, I had filtered trigrams based on the top topic words to identify top trigrams mentioned concerning these aspects. 

For example, 



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
