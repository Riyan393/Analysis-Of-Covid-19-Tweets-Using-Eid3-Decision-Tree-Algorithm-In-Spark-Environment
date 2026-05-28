# Analysis of COVID-19 Tweets Using EID3 Decision Tree Algorithm in Spark Environment

> Computer Science (Big Data Analytics) 

## Overview

This project classifies COVID-19 tweets by sentiment polarity (positive/negative) using a novel **Enhanced ID3 (EID3)** decision tree algorithm implemented in a distributed **Apache Spark / Hadoop HDFS** environment. The goal was to extract meaningful public health insights from social media big data to support awareness and preventive communication around COVID-19.

The EID3 algorithm improves on the traditional ID3 classifier by integrating a **weighted correlation function** with **information gain**, achieving superior accuracy, faster execution time, and better scalability on massive datasets.

---

## Key Highlights

- 🏆 **EID3 outperformed traditional ID3** across accuracy, execution time, and ability to handle massive datasets
- 📊 Achieved **86.53% accuracy** on Sentiment140 and **88.82% accuracy** on COVID-19_Sentiments datasets
- ⚡ Implemented in a fully **distributed Spark/HDFS environment** for real-time scalability
- 🔬 Conducted a **24-paper literature survey** to inform algorithm design and feature engineering choices
- 📰 Extracted actionable public health insights from positive tweets to support COVID-19 awareness

---

## Tech Stack

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Apache Spark](https://img.shields.io/badge/Apache%20Spark-Big%20Data-red?logo=apachespark)
![Hadoop](https://img.shields.io/badge/Hadoop-HDFS-yellow?logo=apachehadoop)
![NLP](https://img.shields.io/badge/NLP-Sentiment%20Analysis-green)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)

**Languages & Libraries:** Python, Apache Spark (PySpark), Hadoop/HDFS, NLTK, Scikit-learn, NumPy, Pandas

---

## Methodology

### 1. Data Collection
- **Datasets:** Sentiment140 & COVID-19_Sentiments
- Source: Twitter COVID-19 tweet streams

### 2. Data Preprocessing
- Tokenisation, stopword removal, stemming, lemmatisation
- Handling slang, abbreviations, hashtags, URLs, and emoticons
- Reduced classification error rate from ~35% to ~12% through preprocessing alone

### 3. Feature Extraction
Multiple techniques applied and compared:
| Method | Description |
|---|---|
| N-grams / Character-level | Captures sub-word and phrase patterns |
| Bag-of-Words (BoW) | Frequency-based text representation |
| TF-IDF | Term frequency–inverse document frequency weighting |
| Word2Vec | Dense word embeddings |
| GloVe | Pre-trained global word vectors |
| FastText | Subword-level embeddings |

### 4. Feature Selection
Dimensionality reduction using:
- Chi-Square
- Information Gain
- Gain Ratio
- Gini Index

### 5. Classification — EID3 Algorithm
The proposed **EID3 (Enhanced ID3)** algorithm improves on standard ID3 by:
- Computing a **weighted correlation function** for each conditioned feature
- Multiplying it by the **information gain** of that feature
- This dual-weight approach selects more optimal splitting attributes, resulting in a simpler, more accurate decision tree

### 6. Distributed Execution
- Entire pipeline executed in **Apache Spark** on **Hadoop HDFS**
- Enables processing of large-scale tweet datasets in parallel across a cluster

---

## Results

| Dataset | Accuracy |
|---|---|
| Sentiment140 | **86.53%** |
| COVID-19_Sentiments | **88.82%** |

EID3 outperformed all baseline classifiers (KNN, SVM, Logistic Regression, standard ID3, Random Forest) across Recall, Precision, F1-Score, Kappa Statistic, execution time, convergence, stability, and complexity.

---

## Project Structure

```
├── data/                  # Tweet datasets (Sentiment140, COVID-19_Sentiments)
├── preprocessing/         # Cleaning, tokenisation, stemming scripts
├── feature_extraction/    # TF-IDF, Word2Vec, N-gram implementations
├── feature_selection/     # Chi-Square, Information Gain, Gini Index
├── eid3/                  # EID3 algorithm implementation
├── spark_pipeline/        # PySpark distributed pipeline scripts
├── results/               # Accuracy metrics and comparison charts
└── README.md
```

---

## Research Foundation

Built on a 24-paper literature survey covering:
- Sentiment analysis on social media during COVID-19
- ID3 and enhanced decision tree variants
- Big data feature selection in distributed environments (Apache Spark)
- NLP techniques for Twitter text classification

Key reference: Es-Sabery et al. (2021), *"A MapReduce Opinion Mining for COVID-19-Related Tweets Classification Using Enhanced ID3 Decision Tree Classifier"* — IEEE Access. DOI: 10.1109/ACCESS.2021.3073215

---

## Author

**Riyan Ahmed Baig**  
Computer Science (Big Data Analytics)  
[LinkedIn](https://www.linkedin.com/in/riyan393) · [GitHub](https://github.com/Riyan393)

---

*Completed as BEng Final Year Project at Don Bosco Institute of Technology, VTU (2022).*
