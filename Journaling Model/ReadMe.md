Made by: Muhammad Nur Irfan\
ID: MC128D5Y0235\
Path: Fundamental Deep Learning\
Google Colab Link: https://colab.research.google.com/drive/1SrE_QpuHNVkQQbpPtv_dAHHJKY_6uq9J?usp=sharing

# Model Overview
This model is an emotion classification designed for a journaling website, which helps users track and reflect on their emotional states.

## 🧠 1. Business Understanding

The goal is to build a machine learning model that classifies user-written journal entries into emotional categories:

- Marah (Angry)
- Senang (Happy)
- Stress (Stressed)
- Bersyukur (Grateful)
- Sedih (Sad)

This will empower users to be more mindful of their emotional health.

---

## 📊 2. Data Understanding

### Dataset Overview:
- **Total entries**: 559
- **Columns**: 
  - `teks`: journal text (type: object, non-null)
  - `label`: emotion class (type: object, non-null)

### Emotion Label Distribution:
- Marah: 112
- Senang: 112
- Stress: 112
- Bersyukur: 112
- Sedih: 111

### Data Quality:
- ✅ No missing values
- ✅ No duplicate entries (`df.duplicated().sum() == 0`)

---

## 🧹 3. Data Preparation

- Text cleaning: punctuation removal, case folding, stopword removal
- Tokenization using BERT tokenizer
- Label encoding for classification
- Train-test split (80% training / 20% testing)
- Ready for modeling with IndoBERT or other transformers

---

## 🤖 4. Modeling

- Model: Fine-tuning IndoBERT for text classification
- Evaluation metrics: Accuracy, Loss

---

## ✅ 5. Evaluation

- Model evaluated using classification report
- Model accuracy and loss graphs
- Confusion matrix to check per-label performance


---

## 🚀 6. Deployment

- Saving model
- Convert model into tfjs
- Inferencing model to insight implementating model into website 

---
## 🛠 Technologies Used
- Python 
- Pandas
- Numpy 
- Scikit-learn
- Transformer
- Matplotlib
- Seaborn
- Tensorflowjs
- Torch
---
## Environment Build
**Google Colab** Runtime GPU T4


## Output
`journal_tfjs_model` is Tensorflow Javascript Model that contains fine-tuned model and model.json to load model


