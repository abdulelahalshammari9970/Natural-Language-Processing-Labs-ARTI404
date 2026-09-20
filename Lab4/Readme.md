# Lab 4 – Text Classification and Evaluation


## Overview

This lab shows how to build and evaluate a text classification model for sentiment analysis.
Star ratings are converted into three classes (positive, negative, and neutral), the reviews are cleaned,
converted to TF-IDF features, and classified.

The first part is a case study on Disneyland reviews, where a linear SVM classifier is trained and evaluated
using accuracy and a classification report.

The second part is a use case on Amazon reviews of unlocked mobile phones. It covers 5 preprocessing steps
(missing values, lowercasing, noise removal, stop words removal, and lemmatization), a stratified train/test split,
TF-IDF feature extraction, training a Naive Bayes classifier, evaluating it on the test set,
and printing the confusion matrix.


## Datasets

- [Disneyland Reviews](https://www.kaggle.com/datasets/arushchillar/disneyland-reviews) (`DisneylandReviews.csv`)
- [Amazon Reviews: Unlocked Mobile Phones](https://www.kaggle.com/datasets/PromptCloudHQ/amazon-reviews-unlocked-mobile-phones) (`Amazon_Unlocked_Mobile.csv`)

Download the CSV files and place them in the same folder as the notebook before running it.


## Requirements

- Python 3
- pandas
- scikit-learn
- NLTK
- matplotlib
- Jupyter Notebook / Google Colab
