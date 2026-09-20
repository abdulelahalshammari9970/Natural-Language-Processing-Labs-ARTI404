# Lab 2 – Text Pre-processing and Regular Expressions


## Overview

This lab introduces the essential techniques for preparing and cleaning text data in NLP.
It starts with regular expressions in Python (`search`, `match`, `findall`, `sub`, `compile`, and `split`),
then covers the main text pre-processing steps: tokenization, lower casing, stemming (Porter and Snowball),
lemmatization, and stop words removal using both NLTK and spaCy.
The lab ends with a small example that uses regular expressions to extract hashtags from an Apple tweets dataset
and finds the total number of hashtags and the top 10 most used ones.




## Requirements

- Python 3
- pandas
- NLTK (with the `punkt`, `wordnet`, and `stopwords` data packages)
- spaCy (with the `en_core_web_sm` model)
- Jupyter Notebook / Google Colab
