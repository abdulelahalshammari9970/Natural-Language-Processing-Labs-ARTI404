# Deep Learning for NLP — Lab 6: Yelp Review Sentiment Classification

This lab classifies Yelp restaurant reviews as **Negative (0)** or **Positive (1)** using a neural network built with PyTorch. Two ways of turning text into numbers are compared: TF-IDF (given in the lab) and Word2Vec (Tasks 1 and 2).

## Files

| File | Description |
|---|---|
| `Lab6_deep_learning_for_nlp-3.ipynb` | Completed lab notebook with all outputs visible |
| `dataset/07-yelp-dataset.txt` | Yelp reviews dataset (tab-separated: review, label) |

## Dataset

- 1,000 restaurant reviews, each with a sentiment label.
- Balanced classes: 500 positive and 500 negative.
- Split: 80% training (800 reviews) and 20% testing (200 reviews), `random_state=42`.

## What was implemented

| Part | Description |
|---|---|
| Baseline | TF-IDF (1,000 features) → network 1000 → 64 → 32 → 1, Adam (lr = 0.01), 10 epochs |
| Task 1 | Word2Vec representation: reviews are tokenized, Word2Vec is trained on the training reviews only (`vector_size=200`, `window=5`, `min_count=1`, `sg=1`), and each review is converted into one vector by averaging its word vectors, then into PyTorch tensors |
| Task 2 | New network on the Word2Vec vectors: 200 → 128 → 64 → 32 → 1 with ReLU activations, `BCEWithLogitsLoss`, Adam (lr = 0.001), 15 epochs |

## Results

| Model | Input features | Test accuracy |
|---|---|---|
| Baseline network | TF-IDF (1,000 features) | 0.745 |
| Task 2 network | Word2Vec (200-dimensional average vectors) | 0.480 |

Baseline classification report (TF-IDF): precision, recall and F1 are between 0.71 and 0.78 for both classes.

## Key takeaways

- TF-IDF gave a much better result than Word2Vec in this lab (0.745 vs 0.480).
- The Word2Vec network barely learned: its loss stayed close to 0.693 (about `ln 2`, the loss of random guessing for two classes), so its test accuracy is at chance level.
- The most likely reason is the very small dataset: Word2Vec was trained on only 800 short reviews with the default number of training epochs, so the averaged word vectors carry little useful information about sentiment.
- In extra tests outside the notebook, training Word2Vec for more epochs and using mini-batches improved the accuracy, but the settings required by the lab were kept in the submitted notebook.

## How to run

1. Put the notebook and the `dataset` folder in the same folder, so that the path `07-yelp-dataset.txt` used in the notebook is found (or keep the file next to the notebook).
2. Install the requirements: `pip install pandas scikit-learn torch gensim jupyter`
3. Open the notebook and run all cells from top to bottom (Kernel → Restart & Run All).

## Notes

- The notebook reads the dataset with `pd.read_csv("07-yelp-dataset.txt", sep="\t", ...)`, so the dataset file must be in the same folder as the notebook when running it.
- Word2Vec is trained only on the training reviews to avoid using test data during training.
- A review with no known words is converted to a zero vector.
