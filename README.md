# DL_ASSIGNMENT2
# 🔤 Latin to Devanagari Transliteration using Seq2Seq (RNN / LSTM / GRU)

This project implements a flexible **sequence-to-sequence model** to transliterate words written in Latin script into Devanagari script using PyTorch. You can choose between RNN, LSTM, or GRU-based encoder-decoder architectures.

---

## 📂 Dataset Format

Input files should be tab-separated `.tsv` files with **no headers** and the following columns:


Example (train.tsv):

> ⚠️ Make sure your files are named correctly and saved as UTF-8.

---

## 📦 Dependencies

Install required libraries (if not already installed):

```bash
pip install torch pandas scikit-learn
train_path = 'train.tsv'
test_path = 'test.tsv'
python transliterate.py
model = Seq2Seq(
    input_dim=len(input_vocab),
    target_dim=len(target_vocab),
    emb_dim=64,
    hidden_dim=128,
    rnn_type='GRU',  # Options: 'RNN', 'LSTM', 'GRU'
    num_layers=1
)
SAMPLE OUTPUT
Epoch 1: Train Loss = 2.4301, Val Loss = 2.1234
...
Epoch 10: Train Loss = 0.5612, Val Loss = 0.4780

Latin: ank → Predicted Devanagari: अंक | Actual: अंक
Latin: ankit → Predicted Devanagari: अंकित | Actual: अंकित
...


# GPT-2 Text Generation on Song Lyrics (Kanye West & Michael Jackson)

This project demonstrates the use of GPT-2, a transformer-based language model, to generate text based on song lyrics of selected artists (Kanye West & Michael Jackson). The script tokenizes the lyrics, preprocesses the data, and fine-tunes the GPT-2 model for text generation.

## 📂 Dataset

The dataset consists of song lyrics from the following artists:

- Kanye West
- Michael Jackson

The lyrics are provided in text files (`.txt`), one file for each artist. The file paths are:


The data is tokenized using the GPT-2 tokenizer and preprocessed for fine-tuning. The model is then trained using the processed data and used to generate text based on an input prompt.

---

## 📦 Dependencies

This project uses the following libraries:

- `tensorflow`
- `transformers`
- `pandas`
- `scikit-learn`

You can install them via pip:

```bash
pip install tensorflow transformers pandas scikit-learn

SAMPLE OUTPUT
true love shouldn't be this complicated
You should be the one I was meant to be
I don't even know you like that
But I don't wanna leave you

