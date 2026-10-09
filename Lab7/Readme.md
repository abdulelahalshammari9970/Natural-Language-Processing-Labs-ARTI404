# Lab 7 – Large Language Models (LLMs)


## Overview

This lab introduces Large Language Models and the three main Transformer model families,
using pre-trained models from Hugging Face through the `transformers` library.

The first part shows a decoder-only model (DistilGPT-2) that generates text by predicting the next token.
The second part shows an encoder–decoder model (FLAN-T5-small) that performs text-to-text tasks such as translation.
The third part shows an encoder-only model (DistilBERT) that classifies the sentiment of a sentence.

In the tasks, the most suitable model family is chosen for five NLP tasks (Task 1),
the sentiment classifier is applied to three sentences and the predicted label and score are printed (Task 2),
and FLAN-T5 is used to summarize a short paragraph (Task 3).
Task 5 is a short reflection on why a decoder-only model is suitable for a chatbot such as ChatGPT.
The optional challenge generates text several times with sampling and explains why the outputs change
even when the prompt is the same.

Note: Task 4 is not included in the original lab file.


## Requirements

- Python 3
- transformers
- sentencepiece
- torch
- Jupyter Notebook / Google Colab
- Internet connection (the first run downloads the pre-trained models from Hugging Face)
