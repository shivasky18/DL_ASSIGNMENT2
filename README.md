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
