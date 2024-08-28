# LDA Topic Modeling and Sentiment Analysis on Project Titan

## Project Overview

This repository contains the analysis of public sentiment surrounding Apple's Project Titan, a self-driving car project. The research primarily focuses on Reddit discussions, exploring how public sentiment evolved before and after the announcement of the project's cancellation.

The analysis employs Latent Dirichlet Allocation (LDA) for topic modeling and VADER for sentiment analysis. The study aims to understand how the anticipation, speculation, and eventual disappointment were reflected in social media sentiment, providing insights into the impact of strategic corporate decisions on consumer expectations.

## Data

### Data Collection

The data used in this analysis was collected from Reddit using the Python Reddit API Wrapper (PRAW) package. The dataset includes comments from posts related to Project Titan across several subreddits, including:

- `/r/Technology`
- `/r/electricvehicles`
- `/r/investing`
- `/r/apple`

The data comprises 500 comments, divided into two phases:
1. 250 comments before the cancellation announcement (up to February 26, 2024).
2. 250 comments from the day of the announcement (February 27, 2024) onward.

### Data Preprocessing

The data underwent a series of preprocessing steps, including:

- **Lowercasing:** All text was converted to lowercase.
- **Punctuation Removal:** Non-essential characters were removed.
- **Tokenization:** Text was broken down into individual words.
- **Stopwords Removal:** Common words with little meaning were filtered out.

This preprocessing enabled the construction of a dictionary and corpus necessary for LDA modeling.

## Analysis

### Topic Modeling with LDA

Latent Dirichlet Allocation (LDA) was used to identify ten distinct topics within the corpus. The model was configured to balance granularity with coherence, yielding a coherence score of 0.44. This score reflects a moderate level of semantic consistency and interpretability among the top words in each topic.

Visualizations such as word clouds were generated to enhance interpretability, with larger font sizes indicating higher term significance.

### Sentiment Analysis with VADER

The sentiment analysis was conducted using the VADER (Valence Aware Dictionary and sEntiment Reasoner) tool. VADER excels at detecting sentiment intensity in text, accounting for nuances like punctuation, word capitalization, and syntactical patterns.

Each comment was assigned a compound sentiment score, with thresholds indicating positive, negative, or neutral sentiment.
