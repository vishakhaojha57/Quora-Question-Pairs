# Quora Question Pair Similarity Detection

## Project Overview

This project aims to determine whether two questions asked on Quora are duplicates of each other. Duplicate question detection is an important Natural Language Processing (NLP) task that helps reduce redundant content and improves the user experience on question-answering platforms.

The model analyzes a pair of questions, extracts meaningful features, converts text into numerical representations using Bag of Words (BoW), and predicts whether the questions have the same meaning.

---

## Problem Statement

Given two questions, the objective is to classify them into one of the following categories:

* Duplicate Questions (1)
* Non-Duplicate Questions (0)

Example:

Question 1:

```
What is the capital of India?
```

Question 2:

```
Which city serves as the capital of India?
```

Output:

```
Duplicate (1)
```

---

## Dataset

The project uses the Quora Question Pairs Dataset.

Dataset Link:

https://www.kaggle.com/competitions/quora-question-pairs/data

Dataset contains:

* id
* qid1
* qid2
* question1
* question2
* is_duplicate

---

## Technologies Used

* Python
* NumPy
* Pandas
* NLTK
* Scikit-Learn
* FuzzyWuzzy
* XGBoost
* Jupyter Notebook

---

## Project Workflow

### 1. Data Collection

The Quora Question Pairs dataset is loaded and analyzed for duplicate and non-duplicate question pairs.

### 2. Data Preprocessing

Text preprocessing includes:

* Converting text to lowercase
* Removing special characters
* Removing HTML tags
* Handling missing values
* Text normalization

### 3. Feature Engineering

Several handcrafted features are created, including:

#### Basic Features

* Question length
* Word count
* Common word count
* Total word count
* Shared word ratio

#### Fuzzy Features

* QRatio
* Partial Ratio
* Token Sort Ratio
* Token Set Ratio

These features help capture textual similarity between question pairs.

### 4. Text Vectorization

Bag of Words (BoW) is used to convert textual data into numerical feature vectors.

CountVectorizer is used to generate word frequency-based representations of the questions.

### 5. Feature Combination

The following features are combined:

* Handcrafted features
* Fuzzy matching features
* Bag of Words vectors

This creates the final feature matrix used for model training.

### 6. Model Training

The following machine learning models are trained and evaluated:

#### Random Forest Classifier

Random Forest is an ensemble learning algorithm that combines multiple decision trees to improve prediction performance.

#### XGBoost Classifier

XGBoost is a gradient boosting algorithm that efficiently handles large datasets and complex feature interactions.

### 7. Prediction

The trained model predicts whether a pair of questions is duplicate or non-duplicate.

## Installation

Clone the repository:

```bash
git clone <repository-url>
```

Move into the project directory:

```bash
cd Quora-Question-Pair
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Required Libraries

```bash
pip install numpy pandas scikit-learn nltk fuzzywuzzy python-Levenshtein xgboost
```


## Author

Vishakha Ojha

GitHub: https://github.com/vishakhaojha57

