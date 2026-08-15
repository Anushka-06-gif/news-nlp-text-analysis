# news-nlp-text-analysis

# 📰 News Text Preprocessing and Category Analysis using NLP

A Natural Language Processing (NLP) project for preprocessing and analyzing news articles using Python. The project performs comprehensive text cleaning, tokenization, stopword removal, POS tagging, lemmatization, word-frequency analysis, and category analysis.

## 📌 Project Overview

This project processes news articles from the **News Articles Classification Dataset for NLP & ML** and transforms raw article text into clean, structured text suitable for NLP analysis and machine learning.

The project combines the article's:

* **Headline**
* **Description**
* **Content**

and applies a complete NLP preprocessing pipeline.

## 🎯 Objectives

* Clean and normalize raw news article text
* Tokenize article content into individual words
* Remove unwanted characters and noise
* Remove English stopwords
* Perform Part-of-Speech (POS) tagging
* Apply WordNet lemmatization
* Extract the top 50 frequent words from each article
* Analyze article distribution across categories
* Identify the most frequent words across the complete dataset
* Generate clean datasets for further NLP and machine learning applications

## 📊 Dataset

**News Articles Classification Dataset for NLP & ML**

The dataset contains news articles with the following fields:

| Column        | Description                      |
| ------------- | -------------------------------- |
| `Headlines`   | News article headline            |
| `Description` | Short description of the article |
| `Content`     | Full news article content        |
| `URL`         | Article source URL               |
| `Category`    | News category                    |

The dataset contains **10,000 news articles** covering categories such as:

* Business
* Education
* Entertainment
* Sports
* Technology

### Dataset Source

[News Articles Classification Dataset for NLP & ML — Kaggle](https://www.kaggle.com/datasets/banuprakashv/news-articles-classification-dataset-for-nlp-and-ml?utm_source=chatgpt.com)

The Python program downloads the dataset through the Kaggle API during execution.

## 🔄 NLP Processing Pipeline

```text
Raw News Articles
        ↓
Data Loading
        ↓
Missing Value Handling
        ↓
Duplicate Removal
        ↓
Headline + Description + Content
        ↓
Text Cleaning
        ↓
Lowercase Normalization
        ↓
Tokenization
        ↓
Contraction Expansion
        ↓
Noise Removal
        ↓
Stopword Removal
        ↓
POS Tagging
        ↓
WordNet Lemmatization
        ↓
Processed Text
        ↓
Frequent Word Analysis
        ↓
Category Analysis
```

## 🧹 Text Preprocessing

### 1. Data Cleaning

Handles missing values and removes duplicate records.

### 2. Text Combination

Combines:

```text
Headlines + Description + Content
```

into a single text field.

### 3. Normalization

Converts text to lowercase to maintain consistency.

### 4. Tokenization

Breaks the article into individual tokens using NLTK's `word_tokenize`.

### 5. Noise Removal

Removes:

* URLs
* HTML elements
* Email addresses
* Numbers
* Special characters
* Unnecessary short tokens

### 6. Stopword Removal

Removes common English words that generally provide limited information for text analysis.

### 7. POS Tagging

Identifies grammatical roles such as:

* Nouns
* Verbs
* Adjectives
* Adverbs

### 8. Lemmatization

Converts words into their meaningful base form using **WordNet Lemmatizer**.

For example:

```text
running → run
better → better
cars → car
```

## 📈 Analysis Performed

### Category Analysis

The project calculates the number of articles belonging to each news category.

Example output:

```text
Category          Article_Count
Business          ...
Education         ...
Entertainment     ...
Sports            ...
Technology        ...
```

### Frequent Word Analysis

The project calculates the most frequently occurring words after preprocessing.

Example:

```text
Word        Frequency
---------------------
...
...
...
```

### Top 50 Words per Article

For every article, the project extracts the **50 most frequent words** after preprocessing.

## 📁 Project Structure

```text
News-Text-Preprocessing/
│
├── news_text_preprocessing.py
├── README.md
├── requirements.txt
│
├── data/
│   └── Kaggle dataset
│
└── output/
    ├── processed_news_articles.csv
    ├── category_summary.csv
    └── frequent_words.csv
```

## 📤 Output Files

### `processed_news_articles.csv`

Contains the processed news data including:

* Headlines
* Description
* Category
* Processed text
* Top 50 words

### `category_summary.csv`

Contains the number of articles in each category.

### `frequent_words.csv`

Contains the most frequently occurring words across the dataset and their frequencies.

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **NLTK**
* **spaCy**
* **Regular Expressions**
* **Kaggle API**

## 📦 Main Python Libraries

```text
pandas
numpy
nltk
spacy
kaggle
```

## 💡 Key Features

* 📥 Automatic Kaggle dataset retrieval
* 🧹 Comprehensive text cleaning
* 🔤 Tokenization
* 🚫 Stopword removal
* 🏷️ POS tagging
* 🌱 Lemmatization
* 📊 Category analysis
* 🔎 Frequent-word analysis
* 📝 Top-50 word extraction
* 💾 Structured CSV outputs

## 🚀 Applications

The processed data can be used as a foundation for:

* 📰 News classification
* 🔍 Text similarity
* 📚 Topic analysis
* 🤖 Machine learning classification
* 📈 News category prediction
* 🔤 Text mining
* 🧠 NLP model development

### ⭐ Project

**News Text Preprocessing and Category Analysis using NLP**

A practical NLP project demonstrating the transformation of raw news articles into structured, analysis-ready text using a complete preprocessing pipeline.
