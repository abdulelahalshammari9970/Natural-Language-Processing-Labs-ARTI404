# Lab 5 – Text Representation


## Overview

This lab shows how to convert text into numerical form so that a machine learning model can process it.
It introduces two text representation techniques: TF-IDF and Word2Vec.

The first part covers TF-IDF, which measures how important a word is in a document compared to a
collection of documents, and cosine similarity, which measures how similar two documents are.
Task 1 computes the cosine similarity between four sentences, and Task 2 applies TF-IDF to three
sentences to find the most important words.

The second part covers Word2Vec with the Skip-gram architecture using gensim. The Simpsons script lines
are cleaned (lowercasing, removing digits and punctuation), tokenized, and used to train a Skip-gram model.
The trained model is then used to find similar words with `most_similar()` (Task 4: "homer", "marge", and "bart")
and to find the odd word out with `doesnt_match()` (Task 5).


## Datasets

- Simpsons Script Lines (`simpsons_script_lines.csv`), included in the `dataset` folder of this lab (used in Tasks 3 to 5)
- [Fake and Real News Dataset](https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset) (`True.csv`), used only in the Word2Vec demonstration cells

Download the CSV files and place them in the same folder as the notebook before running it, or update the file paths in the cells that read them.


## Requirements

- Python 3
- pandas
- numpy
- scikit-learn
- NLTK
- gensim
- Jupyter Notebook / Google Colab
