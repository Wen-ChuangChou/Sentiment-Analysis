# Fine-Tuning Llama 3 for Sentiment Analysis

Welcome to the repository for fine-tuning the **Llama 3** model for sentiment analysis. This project enhances **Llama 3.1–8B Instruct**, a state-of-the-art language model, to accurately classify sentiment in short text data.

## Overview

**Sentiment analysis** is a fundamental task in natural language processing (NLP) that involves identifying the emotional tone of a given text. This project fine-tunes **Llama 3.1–8B** to classify text as **positive**, **negative**, or **neutral**.

## Dataset

The dataset used for fine-tuning and evaluation is from the **Massive Text Embedding Benchmark (MTEB)**:

- **Dataset name:** `mteb/tweet_sentiment_extraction` (available on Hugging Face)
- **Training set size:** 27,481 sentence pairs
- **Test set size:** 3,534 sentence pairs
- **Labels:** `positive`, `neutral`, `negative`

##  Evaluation & Results

We first evaluated the performance of **Llama 3.1–8B Instruct** *without* fine-tuning using the following prompt:

> *"Analyze the sentiment of the following text. Respond with exactly one word: either 'positive', 'negative', or 'neutral'."*

- **Zero-shot accuracy:** 63.41%  
- **Post fine-tuning accuracy:** **81.49%**

Fine-tuning led to a substantial improvement in sentiment classification accuracy. In addition to overall performance, the model demonstrated marked gains in **precision**, **recall**, and **F1-score** across all sentiment categories.

The table below summarizes the detailed evaluation metrics on the MTEB tweet sentiment test set, comparing results **before and after fine-tuning**:

| **Metric**             | **Before Fine-Tuning** | **After Fine-Tuning** |
|------------------------|------------------------|------------------------|
| **Accuracy**           | 63.41%                 | **81.49%**             |
|                        |                        |                        |
| **Negative Precision** | 64.14%                 | **79.05%**             |
| **Negative Recall**    | 76.21%                 | **84.42%**             |
| **Negative F1-score**  | 69.66%                 | **81.64%**             |
|                        |                        |                        |
| **Neutral Precision**  | 63.21%                 | **79.42%**             |
| **Neutral Recall**     | 49.22%                 | **76.64%**             |
| **Neutral F1-score**   | 55.34%                 | **78.01%**             |
|                        |                        |                        |
| **Positive Precision** | 65.24%                 | **86.54%**             |
| **Positive Recall**    | 72.78%                 | **85.13%**             |
| **Positive F1-score**  | 68.80%                 | **85.83%**             |


These results highlight the effectiveness of fine-tuning in enabling more nuanced and reliable sentiment predictions, especially for challenging neutral and negative cases.

The radar chart below visualizes the improvements across key performance metrics:

<p align="center">
  <img src="https://github.com/Wen-ChuangChou/sentiment_analysis/blob/main/pic/radarplot.png?raw=true" alt="Radar plot" width="400"/>
</p>
