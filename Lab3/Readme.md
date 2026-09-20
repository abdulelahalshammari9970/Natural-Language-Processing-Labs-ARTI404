# Lab 3 – N-Grams and Language Models


## Overview

This lab introduces N-gram language models. It starts with unigrams, bigrams, and trigrams using NLTK,
including how to calculate word probabilities, and explains padding with start and end symbols (`<s>` and `</s>`).
Then it trains a Maximum Likelihood (MLE) language model, calculates bigram probabilities,
and evaluates models using perplexity.

In the final task, a bigram MLE model is trained on a dataset of tweets to generate new tweets.
The tweets are cleaned first (hashtags, RT, links, mentions, and emojis are removed), then the model is evaluated on a test set.
The lab also shows why MLE gives an infinite perplexity for unseen bigrams and how Laplace (add-one) smoothing fixes it.
Finally, it calculates the probability of the bigram (pakistan is) and the perplexity of the word (pakistan).


## Dataset

The task uses the [Large Random Tweets from Pakistan](https://www.kaggle.com/datasets/adizafar/large-random-tweets-from-pakistan) dataset from Kaggle.
Download the CSV file and place it in the same folder as the notebook before running it.


## Requirements

- Python 3
- pandas
- NLTK
- emoji
- Jupyter Notebook / Google Colab
