# 🧠 Text Summarization using NLP (BART)

A transformer-based approach to **abstractive text summarization** using Amazon product reviews, built with `facebook/bart-large`. Developed as part of a B.Tech project at Delhi Technological University.

---

## 📌 Problem Statement

With millions of product reviews on platforms like Amazon, manually extracting meaningful information is overwhelming. This project aims to develop an **automated summarizer** that condenses long reviews into short, coherent summaries using modern NLP techniques.

---

## 🚀 Key Highlights

- 🔧 **Model Used**: facebook/bart-large (transformer-based)
- 📚 **Dataset**: Amazon Fine Food Reviews (125 samples)
- 📊 **Metrics**: Eval Loss, ROUGE-L, BERTScore
- 🎯 **BERTScore F1**: `0.8549` – indicating strong semantic similarity

---

## 📁 Dataset Overview

- **Name**: Amazon Fine Food Reviews  
- **Size**: 254MB  
- **Fields Used**:  
  - `Text` – full review  
  - `Summary` – user-provided headline  
- **Sampling**: 100 training + 25 evaluation samples used

---

## 🛠️ Tools & Libraries

- **Python** (Data + Model Training)
- **SimpleTransformers** (wrapper over HuggingFace)
- **PyTorch + CUDA** (GPU acceleration)
- **Pandas**, **Matplotlib**, **Scikit-learn**

---

## 🧪 Methodology

1. **Data Cleaning**:
   - Removed missing and duplicate entries.
   - Renamed columns as `input_text` and `target_text`.

2. **Model Configuration**:
   - Transformer: `facebook/bart-large`
   - Epochs: `20`, Patience: `3`
   - Eval metric: Loss (monitored per step)
   - Training using `Seq2SeqModel`

3. **Evaluation**:
   - Visualized training vs. evaluation loss
   - Used `BERTScore` to validate semantic quality

---

## 📉 Model Training Summary

- **Loss Curves** showed steady decline with early stopping.
- **Summaries** generated were grammatically correct and semantically rich.
- **ROUGE-L F1** was low (`0.0924`) due to high abstraction.
- **BERTScore F1** was strong: `0.8549`
![Training and Evaluation Loss]([https://raw.githubusercontent.com/yourusername/yourrepo/main/assets/loss-curve.png](https://github.com/sukarnhans/Text-Summarization-using-NLP/blob/main/image.png))
---

## ✨ Sample Output

```text
Original Review:
"This is the best granola I've ever had. It's crunchy, sweet, and goes well with milk or yogurt. Highly recommend!"

