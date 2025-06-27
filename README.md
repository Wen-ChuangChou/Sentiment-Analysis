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

<div align="center">
  <table>
    <thead>
      <tr>
        <th align="center"><b>Metric</b></th>
        <th align="center"><b>Before Fine-Tuning</b></th>
        <th align="center"><b>After Fine-Tuning</b></th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td align="center"><b>Accuracy</b></td>
        <td align="center">63.41%</td>
        <td align="center"><b>81.49%</b></td>
      </tr>
      <tr>
        <td colspan="3"></td>
      </tr>
      <tr>
        <td align="center"><b>Negative Precision</b></td>
        <td align="center">64.14%</td>
        <td align="center"><b>79.05%</b></td>
      </tr>
      <tr>
        <td align="center"><b>Negative Recall</b></td>
        <td align="center">76.21%</td>
        <td align="center"><b>84.42%</b></td>
      </tr>
      <tr>
        <td align="center"><b>Negative F1-score</b></td>
        <td align="center">69.66%</td>
        <td align="center"><b>81.64%</b></td>
      </tr>
      <tr>
        <td colspan="3"></td>
      </tr>
      <tr>
        <td align="center"><b>Neutral Precision</b></td>
        <td align="center">63.21%</td>
        <td align="center"><b>79.42%</b></td>
      </tr>
      <tr>
        <td align="center"><b>Neutral Recall</b></td>
        <td align="center">49.22%</td>
        <td align="center"><b>76.64%</b></td>
      </tr>
      <tr>
        <td align="center"><b>Neutral F1-score</b></td>
        <td align="center">55.34%</td>
        <td align="center"><b>78.01%</b></td>
      </tr>
      <tr>
        <td colspan="3"></td>
      </tr>
      <tr>
        <td align="center"><b>Positive Precision</b></td>
        <td align="center">65.24%</td>
        <td align="center"><b>86.54%</b></td>
      </tr>
      <tr>
        <td align="center"><b>Positive Recall</b></td>
        <td align="center">72.78%</td>
        <td align="center"><b>85.13%</b></td>
      </tr>
      <tr>
        <td align="center"><b>Positive F1-score</b></td>
        <td align="center">68.80%</td>
        <td align="center"><b>85.83%</b></td>
      </tr>
    </tbody>
  </table>
</div>


These results highlight the effectiveness of fine-tuning in enabling more nuanced and reliable sentiment predictions, especially for challenging neutral and negative cases.

The radar chart below visualizes the improvements across key performance metrics:

<p align="center">
  <img src="https://github.com/Wen-ChuangChou/sentiment_analysis/blob/main/pic/radarplot.png?raw=true" alt="Radar plot" width="400"/>
</p>
