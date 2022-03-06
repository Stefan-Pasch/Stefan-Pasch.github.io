---
layout: page
title: Blogs
---

## Stonkbert: Can Language Models Predict Medium-Run Stock Price Movements?
![Stonkbert](assets/img/stocknlp/stonkbert_cracked.jpg)

Article written by Daniel Ehnes and Stefan Pasch. Find the full paper [here](https://arxiv.org/abs/2202.02268)[1].

Recent years have seen one of the biggest advancements in AI research in the field of Natural Language Processing (NLP). By shifting away from rule-based attempts to analyze language towards large neural networks, modern transformer models are able to capture a general understanding of language. Most notably, in 2018 Google has published its **transformer-based neural network BERT** (Bidirectional Encoder Representations from Transformers)[2]. With this and similar transformer-based language models new high scores could be set in various NLP tasks and applications, such as question-answering, fact-checking or hate-speech detection.

Unsurprisingly, such language models have since been applied to predict stock prices based on company-related text data, such as tweets and corporate disclosures (For example, see the excellent articles of Babbe[3] and Aktan[4]). However, this work has mostly focused on the stock movements just a few days after the corresponding documents have been published. Yet, many investors do not engage in day-trading and are interested in stock performance over a longer time. Moreover, most language models that tried to predict stock prices analyzed a single source of text data, e.g., only company reports. However, some types of company-related text data may be more informative than others.

Therefore, with StonkBERT, we focus on the following main questions:

- 1. Can Language-Models predict the performance of a stock **one year** after the publication of related text data?
- 2. If yes, is it dependent on the type of document that is used in the analysis? (We investigate three types of documents that are commonly used for this purpose: **News articles, blogs, and annual company reports)**

#### Getting Stock-Related Text Data and Stock Prices

**Stock-Related Text Data**: We scrutinize three types of company-related text data: We use a dataset on historical financial news from Gennadiyi[5]. The dataset covers company-specific news articles (henceforth “news”) and stock market opinion pieces (which we label as “blogs”). Further, we retrieved annual reports as filed with the Securities and Exchange Commission (SEC), the so-called Form-10K filings.

We cover articles from 2012 to 2019 and consider the 250 companies with the most articles in the dataset of historical financial news.

**Stock Prices**: For these companies, we gathered daily stock price data from Yahoo Finance. To distinguish individual price movements from general market trends, we look at the abnormal price in- or decreases for each stock, that is, a stock’s price change compared to the average price change of the market. These abnormal one-year return data were then split into tertiles, dividing stocks into three equally large groups, of over-, under-, and average-performers. Hence, from a random classifier, we would expect an accuracy of 33%.
