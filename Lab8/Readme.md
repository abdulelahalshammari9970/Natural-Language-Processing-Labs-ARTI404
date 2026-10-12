# Lab 8 – Part-of-Speech (POS) Tagging


## Overview

This lab introduces Part-of-Speech (POS) tagging, which assigns each word in a text a grammatical category
(such as noun, verb, or adjective) based on its definition and its context in the sentence.

The first part uses NLTK's `pos_tag` method to tag the words of a sentence with the Penn Treebank tags,
and ends with an example that extracts the adjectives (`JJ`) from a set of phone reviews.

The second part uses spaCy to show coarse-grained tags (`token.pos_`), fine-grained tags (`token.tag_`),
and their descriptions (`spacy.explain`). It also shows how spaCy uses the context to choose the correct tense
of an ambiguous word such as "read", and how to visualize the tags and dependencies with displaCy.

In the tasks, the coarse-grained tag, fine-grained tag, and tag explanation of the word "play" are printed,
followed by the tags of every word in the sentence (Task 1). The words "google" and "table" are compared in
different sentences, showing that the same word can be a proper noun, a noun, or a verb depending on its
context (Task 2). Finally, the part of speech of each word in a sentence is visualized with displaCy (Task 3).


## Requirements

- Python 3
- NLTK (with the `averaged_perceptron_tagger_eng` and `punkt_tab` data packages)
- spaCy (with the `en_core_web_sm` model)
- Jupyter Notebook / Google Colab
