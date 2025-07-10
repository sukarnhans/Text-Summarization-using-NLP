# 🧠 Text Summarization using NLP (BART)

A transformer-based approach to **abstractive text summarization** using Amazon product reviews, fine-tuned with the `facebook/bart-large` model. Built as a B.Tech project under the Department of Software Engineering at Delhi Technological University.

![Project Banner](https://github.com/yourusername/yourrepo/assets/banner-image.jpg)

---

## 📌 Problem Statement

With millions of reviews on platforms like Amazon, extracting key information manually is impractical. Our goal: **Automatically generate coherent and concise summaries** from lengthy product reviews without losing context.

---

## 🚀 Project Highlights

| Feature | Description |
|--------|-------------|
| Model | `facebook/bart-large` (Transformer-based Abstractive Summarizer) |
| Library | [SimpleTransformers](https://github.com/ThilinaRajapakse/simpletransformers) |
| Dataset | [Amazon Fine Food Reviews](https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews) |
| Evaluation Metrics | Eval Loss, ROUGE-L, BERTScore |
| Avg. BERTScore F1 | **0.8549** |

---

## 📊 Dataset

- **Name:** Amazon Fine Food Reviews
- **Size:** 254 MB
- **Samples Used:** 125 (100 train + 25 eval)
- **Fields:** `Text` (review body), `Summary` (user-provided headline)

---

## 🛠️ Tech Stack

- **Python** (Data handling & NLP)
- **SimpleTransformers** (Model fine-tuning)
- **PyTorch + CUDA** (GPU acceleration)
- **Matplotlib** (Loss visualization)
- **Pandas**, **Sklearn**

---

## 🧪 Model Architecture

- Pre-trained `facebook/bart-large`
- Fine-tuned using `Seq2SeqModel` from SimpleTransformers
- Early stopping based on eval loss with patience = 3

![Loss Curve](<img width="1080" height="646" alt="image" src="https://github.com/user-attachments/assets/76172f64-cab6-49b3-932c-950e882f86c0" />
) <!-- Replace with actual image if you upload -->

---

## 📈 Results

| Metric | Score |
|--------|-------|
| ROUGE-L F1 | 0.0924 |
| **BERTScore F1** | **0.8549** |

🔍 **Why low ROUGE?** Because summaries are highly abstractive (few word overlaps). BERTScore reflects **semantic accuracy** better.

---

## 📷 Visualizations

### 🔻 Training & Evaluation Loss over Steps

![Loss Graph](https://github.com/yourusername/yourrepo/assets/loss-graph.jpg)

---

## 📚 Sample Prediction

```text
📝 Original Review:
"This is the best granola I've ever had. It's crunchy, sweet, and goes well with milk or yogurt. Highly recommend!"

🤖 Generated Summary:
"Best granola ever!"
