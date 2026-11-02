# Lab 10 – Introduction to Machine Translation


## Overview

This lab introduces Machine Translation (MT), the task of automatically translating text from one language
to another, together with its main challenges (ambiguity, idiomatic expressions, and low-resource languages)
and its applications.

The first part shows Neural Machine Translation with a small English–French example. The sentences are tokenized
with the Keras `Tokenizer`, converted to sequences of word indices, and padded to the same length. Then an
encoder–decoder LSTM model (Embedding, encoder LSTM, `RepeatVector`, decoder LSTM, and a `TimeDistributed`
softmax layer) is trained and used to translate a new sentence.

In the tasks, the role of each model layer is explained: the Embedding layer, the encoder LSTM, the decoder LSTM,
and the softmax output layer (Task 1). In the use case, an e-commerce company needs to translate its English content
into French. The English–French dataset is cleaned, short sentences are selected, and a random sample of 20,000
sentence pairs is tokenized and padded. The encoder–decoder LSTM model is then trained for 20 epochs, evaluated
on the test set, and used to translate test sentences and short shopping sentences (Task 2).


## Dataset

- [Language Translation (English–French)](https://www.kaggle.com/datasets/devicharith/language-translation-englishfrench) (`eng_-french.csv`)

Download the CSV file and place it in the same folder as the notebook before running Task 2.


## Requirements

- Python 3
- TensorFlow / Keras
- NumPy
- pandas
- scikit-learn
- Jupyter Notebook / Google Colab
