# Lab 12 – Transformers


## Overview

This lab introduces the Transformer, a deep learning architecture that processes sequences of text using
self-attention. Transformers are the foundation of many modern NLP models such as BERT, GPT, and T5, and they
replaced earlier models such as RNNs and LSTMs.

The notebook uses the Hugging Face Transformers library with DistilBERT, a model fine-tuned for positive/negative
sentiment classification. First, the tokenizer and the model are loaded and the number of Transformer layers,
attention heads, and the hidden size are printed. Then a sentence is tokenized into tokens and token IDs (with the
special `[CLS]` and `[SEP]` tokens), each token ID is converted into an embedding vector, and the self-attention
weights of the first layer and the first head are extracted. Finally, the classification head produces two scores
(logits), and softmax converts them into probabilities to give the sentiment prediction and its confidence.

In the task, the pretrained `bert-base-uncased` model is loaded and explored: the number of Transformer layers and
attention heads per layer are printed, the total number of attention heads is calculated, the attention weights of
the third layer and the second head are extracted for the sentence
`"Transformers use self-attention to understand language."` (and shown as a heatmap), and the meaning of the rows
and columns of the attention matrix is explained.


## Dataset

No dataset is needed. The pretrained models (`distilbert-base-uncased-finetuned-sst-2-english` and
`bert-base-uncased`) are downloaded automatically from Hugging Face when the notebook is run.


## Requirements

- Python 3
- PyTorch
- Hugging Face Transformers
- matplotlib
- Internet connection (to download the pretrained models)
- Jupyter Notebook / Google Colab
