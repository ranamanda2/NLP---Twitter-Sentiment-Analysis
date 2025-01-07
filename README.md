# NLP---Twitter-Sentiment-Analysis
 "Analyze Twitter sentiment using NLP with the Sentiment140 dataset."

# Twitter Sentiment Analysis Using NLP

This repository contains an end-to-end implementation of a Twitter sentiment analysis project using the **Sentiment140 dataset**. The goal is to classify tweets into **positive**, **neutral**, or **negative** sentiments based on their content.

---

## Dataset

The dataset used in this project is the **Sentiment140 dataset** available on Kaggle:
- Link: [Sentiment140 Dataset on Kaggle](https://www.kaggle.com/datasets/kazanova/sentiment140)
- File: `training.1600000.processed.noemoticon.csv` (238.8 MB)

### Dataset Details
- **Source**: Extracted using the Twitter API
- **Size**: 1,600,000 tweets
- **Fields**:
  1. `target`: Sentiment polarity (0 = negative, 2 = neutral, 4 = positive)
  2. `ids`: Tweet ID (e.g., 2087)
  3. `date`: Date of the tweet (e.g., Sat May 16 23:58:44 UTC 2009)
  4. `flag`: Query type (e.g., lyx). If no query, this field is `NO_QUERY`.
  5. `user`: Username of the person who tweeted (e.g., robotickilldozr)
  6. `text`: Content of the tweet (e.g., "Lyx is cool")

### Dataset Generation
The dataset was automatically labeled using a unique approach. Positive tweets were identified with emoticons like `:)`, while negative tweets had emoticons like `:(`. The data was collected via the **Twitter Search API** using keyword-based searches.

---

## Project Workflow

1. **Data Collection**:
   - Kaggle dataset: `training.1600000.processed.noemoticon.csv`
   - Alternatively, Twitter API can be used for real-time data collection.

2. **Data Preprocessing**:
   - Remove special characters, URLs, mentions, hashtags, and punctuations.
   - Tokenization and stemming/lemmatization.
   - Stopword removal.

3. **Exploratory Data Analysis (EDA)**:
   - Analyze the distribution of sentiments.
   - Visualize word clouds for positive, neutral, and negative tweets.

4. **Modeling**:
   - Build models using traditional ML algorithms (e.g., Logistic Regression, SVM)
   - Evaluate the model's performance using metrics like accuracy, precision, recall, and F1-score.

5. **Deployment**:
   - Integrate the model into an application for live tweet sentiment classification (Optional).

---

## Installation

### Prerequisites
1. Python 3.x
2. Install required libraries:
   ```bash
   pip install pandas numpy nltk scikit-learn matplotlib seaborn
