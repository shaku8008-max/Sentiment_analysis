````markdown
# SDG 12 Twitter Analysis: Responsible Consumption and Production

## Project Overview

This project analyzes public discourse on Twitter related to Sustainable Development Goal 12 (SDG 12): Responsible Consumption and Production, covering the period from October 2024 to May 2025.

The goal of this project is to understand how people discuss sustainability topics such as food waste, carbon footprint reduction, circular economy, ethical sourcing, and supply chain responsibility. The project uses Natural Language Processing (NLP), sentiment analysis, topic modeling, clustering, and machine learning techniques to identify public opinion patterns, key discussion themes, and engagement behavior.

---

## Research Objectives

The project aims to answer the following questions:

- What are the dominant discussion themes within SDG 12 conversations?
- How do people feel about responsible consumption topics?
- Which sustainability topics generate the strongest positive or negative sentiment?
- What causes spikes in Twitter engagement?
- What hidden discussion groups exist within SDG 12 conversations?
- Which factors influence tweet sentiment the most?

---

## Dataset

### Source

Twitter data collected for SDG 12 related discussions.

### Timeframe

October 2024 – May 2025

### Key Fields Used

- Tweet text
- Created_At
- Retweet Count
- Favorite Count
- Reply Count
- Quote Count
- Hashtags
- User information
- Sentiment score

---

## Data Preprocessing

Before analysis, the dataset was cleaned using the following steps:

- Removed stop words
- Removed punctuation
- Removed URLs and mentions
- Removed unnecessary symbols
- Converted timestamps into day and week fields
- Created text length feature
- Converted text into machine-readable format for NLP models

This improved the quality of topic modeling, clustering, and sentiment analysis.

---

## Methodology

### 1. Bigram and Trigram Analysis

Used to identify the most frequent word combinations in SDG 12 discussions.

### Key Findings

Top bigrams:

- carbon footprint
- circular economy
- food waste

Top trigrams:

- reduce carbon footprint
- supply chain traceability
- extended producer responsibility

This showed that Twitter users strongly associate responsible consumption with carbon reduction, ethical sourcing, and sustainable production systems.

---

### 2. Sentiment Analysis

Two sentiment analysis approaches were used:

### TextBlob

Used to calculate polarity scores:

- Positive
- Neutral
- Negative

### Hugging Face Model

Model used:

```python
cardiffnlp/twitter-roberta-base-sentiment-latest
````

This transformer-based model provided stronger Twitter-specific sentiment classification.

### Key Findings

Food waste dataset sentiment results:

* Neutral: 259
* Positive: 162
* Negative: 102

Most tweets were neutral to positive, showing that discussions were mainly informative and supportive rather than highly critical.

Negative sentiment was mostly linked to:

* wasteful behavior
* environmental risks
* poor food management
* greenwashing concerns

---

### 3. LDA Topic Modeling

LDA (Latent Dirichlet Allocation) was used to discover hidden topics within the tweet corpus.

This grouped commonly occurring words into meaningful sustainability themes.

### Main Topics Identified

* biodegradable packaging
* food waste reduction
* circular economy
* carbon footprint
* supply chain sustainability
* sustainability policy discussions

This helped identify what people were discussing without manually reading thousands of tweets.

---

### 4. K-Means Clustering

Used TF-IDF vectorization to convert tweets into numerical features.

Applied K-Means clustering to identify hidden discussion groups.

### Cluster Groups

Cluster 1:
Sustainability and green practices

Cluster 2:
Critical policy discourse and greenwashing concerns

Cluster 3:
Waste management and circular economy

Cluster 4:
Carbon accountability and environmental responsibility

### Key Findings

Cluster 2 showed the strongest negative sentiment, while Clusters 1 and 3 were more positive and solution-focused.

This revealed that constructive and critical voices coexist in SDG 12 discourse.

---

### 5. Sentiment by Cluster

Cross-tab analysis was used to compare sentiment across clusters.

### Findings

* Most clusters were dominated by neutral and positive sentiment
* Cluster 2 contained stronger negative sentiment
* Cluster 1 and 3 focused more on practical sustainability solutions

This showed how emotional tone changes depending on the discussion topic.

---

### 6. Weekly Spike Detection

Weekly tweet volume was analyzed to identify major engagement spikes.

### Key Finding

A major spike occurred in April 2025, where tweet volume exceeded 1200+ tweets.

### Likely Reasons

* Earth Day (April 22, 2025)
* Earth Month campaigns
* corporate ESG announcements
* sustainability policy discussions
* food waste action plans

This demonstrated that public engagement is highly event-driven rather than consistently sustained.

---

### 7. Random Forest for Sentiment Prediction

A Random Forest classifier was used to predict sentiment using:

* text length
* retweet count
* favorite count
* reply count
* quote count

### Goal

To identify which features most strongly influence public sentiment.

### Key Findings

Feature importance showed:

1. Text Length (strongest predictor)
2. Favorite Count
3. Retweet Count
4. Reply Count
5. Quote Count

This suggests that longer and more engaging tweets tend to carry stronger emotional sentiment.

---

## Major Insights

### Public Discussion is Event-Driven

Twitter engagement around SDG 12 rises sharply during major sustainability events but often declines afterward.

This suggests the need for stronger long-term communication strategies.

---

### Carbon Footprint Dominates the Conversation

Reducing carbon footprint was the strongest recurring theme.

This indicates that climate responsibility remains the central concern within responsible consumption discussions.

---

### Supply Chain Accountability Matters

Users strongly connect SDG 12 with:

* ethical sourcing
* producer responsibility
* supply chain transparency

This shows increasing demand for corporate sustainability accountability.

---

### Public Sentiment is Cautiously Optimistic

Most users support sustainability initiatives, but criticism appears when discussing:

* policy failures
* greenwashing
* poor waste management
* lack of corporate responsibility

---

## Technologies Used

### Python Libraries

* pandas
* matplotlib
* seaborn
* scikit-learn
* TextBlob
* transformers
* gensim
* pyLDAvis
* nltk

### Machine Learning Models

* Hugging Face RoBERTa Sentiment Model
* LDA Topic Modeling
* K-Means Clustering
* Random Forest Classifier

---

## Final Conclusion

Twitter reflects strong public awareness of SDG 12, but engagement remains fragile and highly dependent on major events.

People care deeply about responsible consumption, especially around carbon footprints, food waste, and supply chain accountability. However, public trust is heavily influenced by how organizations communicate sustainability efforts.

Future sustainability campaigns should focus on:

* sustained engagement
* supply chain transparency
* reducing greenwashing skepticism
* stronger corporate accountability

This project demonstrates how NLP and machine learning can provide meaningful insights into public sustainability discourse at scale.

---

## Author

Project developed for SDG 12 Twitter Analysis using NLP and Machine Learning methods.

```
```
