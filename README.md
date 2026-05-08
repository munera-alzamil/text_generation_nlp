# Arabic Text Generation (NLP Zero to Hero: Arabic NLP Implementation)

An assignment for CS365 — Natural Language Processing at IMSIU. This notebook follows the "NLP Zero to Hero" video series and implements all six parts on real Arabic news data from the SANAD dataset.

---

## What This Project Covers

| Part | Topic |
|---|---|
| Part 1 | Tokenization — normalizing and tokenizing Arabic text |
| Part 2 | Sequencing — converting tokens to padded integer sequences |
| Part 3 | Simple Classification Model — Embedding + Dense baseline |
| Part 4 | RNN Model — SimpleRNN classifier |
| Part 5 | LSTM Model — Bidirectional stacked LSTM classifier |
| Part 6 | Text Generation — LSTM next-word prediction for Arabic text |

---

## Dataset

The **SANAD** dataset is used — a collection of Arabic news articles organized by source and category. Up to 3,000 articles per category are loaded to keep training time manageable.

The dataset is not included in this repo. Download it and place the ZIP file in your Google Drive at `MyDrive/NLP Assignment2/SANAD.zip` before running the notebook.

---

## Models

### Classification Models

| Model | Architecture |
|---|---|
| Simple | Embedding + GlobalAveragePooling + Dense |
| RNN | Embedding + SimpleRNN + Dense |
| BiLSTM | Embedding + Bidirectional LSTM x2 + Dense |

All three models are trained for 5 epochs and compared by validation accuracy.

### Text Generation Model
An LSTM with 128 units trained on 20-token sliding windows from the full corpus. Uses temperature sampling (0.8) to generate Arabic text continuations from a user-provided seed sentence.

---

## Dependencies
tensorflow
scikit-learn
numpy
pandas
matplotlib

CS365 — Natural Language Processing | Assignment 2 | Dr. Fahman Saeed and Dr. Amal AlSaif | IMSIU

