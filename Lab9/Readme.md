# Lab 9 – Named Entity Recognition (NER)


## Overview

This lab introduces Named Entity Recognition (NER), which detects named entities in a text and classifies them
into categories such as persons, organizations, locations, dates, and monetary values.

The first part uses spaCy's pre-trained `en_core_web_sm` model to recognize the entities in a sentence and print
their details: the text, label, start and end positions, and the explanation of the label (`spacy.explain`).
It then shows how to annotate custom entities manually with character offsets, check their alignment with
BILUO tags, and visualize the entities with displaCy.

In the tasks, the user enters a sentence and the details of each recognized entity are printed (Task 1).
In a contract paragraph, the entities that spaCy missed or detected incorrectly ("Abc & Co." and "Bcd LLC")
are added as `ORG`, the `PERSON` and `ORG` entities are counted, and the entities are visualized with displaCy (Task 2).
Finally, a custom NER model is trained from a blank English model using `Example.from_dict()` for 20 iterations,
saved to the `custom_ner_model` folder, and loaded again to identify the entities in a sentence (Task 3).


## Notes

- The Visualization cell loads the `custom_ner_model` folder, which is created in Task 3.
  Run the Task 3 cell first, then run all the cells.
- The Task 1 cell asks for a sentence as input when it runs.


## Requirements

- Python 3
- spaCy (with the `en_core_web_sm` model)
- Jupyter Notebook / Google Colab
