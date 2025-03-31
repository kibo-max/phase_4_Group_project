# phase_4_Group_project

![image](https://github.com/user-attachments/assets/b02f53ac-ce0c-4048-8016-e6d22f15134e)

# Summary

## Dataset Overview
The dataset contains information about tweet sentiments that includes classification thereof, trusted judgements, tweet confidence, and other related features. In this regard, we extracted the sentiments which were categorized as negative, positive and neutral.

## Data Preparation
This entailed data cleaning and processing using pandas and NLTK libraries.

(a)  Data cleaning
   The dataset had no missing values therefore no imputation was required.
   Sentiments clustered as not_relevant were dropped.
   Columns that were irrelevant to the analysis were dropped. This included: unit_id', '_golden', '_unit_state', '_trusted_judgments','_last_judgment_at','sentiment:confidence', 'date', 'id','query', 'sentiment_gold'.
   Duplicated tweets were dropped.

(b)  Data pre-processing
Hyperlinks, single-character words, hashtags, symbols amongst others were removed as they are irrelevant to the analysis
Stop words and punctuaion were removed  as they similarly are irrelevant to the analysis.
Lemmatization was applied inorder to convert words to their root form.

 ## Data Vizualization
We used matplotlib to visualize the target sentiment classifications, most common words in the dataset that is the positive and negatives ones.

## Data Modelling and Evaluation

(a) Modelling
We employed the following to model that data-
Scikit-learn model selection to split the dataset into training and testing sets.
Applied TF-IDF Vectorizer to convert the text data into numerical representations
SMOTE and resampling to address class imbalances as one sentiment category comprised more thatn 50% of the dataset.

(b) Evaluation
To assess the model performance we applied the following evaluation metrics-
Accuracy score: To measure the percentage of correct predictions out of those made.
ROC curve and ROC AUC: To represent the performance of the classifier's performance  at different thresholds and to provide an overall summary model's ability between classes

Multinomial naive bayes, Random Forest and XGBoost, machine learning models, were also applied.

## Contents of the repository
This repository contains the following:

data/: Contains the dataset file (Apple-Twitter-Sentiment-DFE.csv).
notebooks/: Contains the Jupyter Notebook (Tweet_Sentiment_Analysis.ipynb) used for the analysis.
scripts/: May contain any Python scripts used for data processing or modeling (if applicable).
models/: May contain saved model files (if applicable).
README.md: This file, providing an overview of the project.
presentation.pdf: Link to presentation (if applicable).
## Model Evaluation and Predictions
The test set obtained from train_test_split(X_test, y_test) was used for model evaluation and to make predictions.
