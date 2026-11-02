# Lab 11 – Attention with RNN


## Overview

This lab introduces the attention mechanism, which allows a neural network to focus more on the relevant
words of the input when making a prediction.

A small question-answering dataset is used, where each question belongs to one of 12 answer groups.
The questions are lowercased, tokenized with the Keras `Tokenizer`, padded to the same length, and converted
to PyTorch tensors. Then an RNN model with attention is built in PyTorch: an Embedding layer turns word indices
into vectors, an RNN layer reads the words in sequence, an attention layer gives each word a weight using softmax,
and a final linear layer chooses one answer. The model is trained for 50 epochs, and the attention weights of a
question are visualized as a bar chart.

In the tasks, the attention weights of three different questions are visualized and the word with the highest
attention in each question is identified, followed by a discussion of whether these words are important for
understanding the question (Task 1). Two questions with a similar meaning but different wording are then compared
to see whether the model focuses on similar words, and what this suggests about how attention works (Task 2).


## Dataset

- `Lab_11_QnA_Dataset.csv`, included in the `dataset` folder of this lab (168 questions, 12 answer groups)

The notebook was written for Google Colab: upload the CSV file to Colab and name it
`Lab_11_QnA_Dataset_Download.csv` (the path used in the notebook), or update the file path in the cell that reads it.


## Requirements

- Python 3
- PyTorch
- TensorFlow / Keras (for the `Tokenizer` and `pad_sequences`)
- pandas
- matplotlib
- Google Colab
