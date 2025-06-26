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

## Evaluation & Results

We first evaluated the performance of **Llama 3.1–8B Instruct** *without* fine-tuning using the following prompt:

> *"Analyze the sentiment of the following text. Respond with exactly one word: either 'positive', 'negative', or 'neutral'."*

- **Zero-shot accuracy:** 63.41%
- **Post fine-tuning accuracy:** **81.49%**

Fine-tuning significantly improved the model’s accuracy. The radar chart below shows performance improvements across multiple evaluation metrics:

<p align="center">
  <img src="https://github.com/Wen-ChuangChou/sentiment_analysis/blob/main/pic/radarplot.png?raw=true" alt="Radar plot" width="400"/>
</p>
