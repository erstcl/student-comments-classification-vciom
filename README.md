[🇷🇺 Русская версия](README.ru.md) | [🇬🇧 English version](README.md)

---

# Student Sentiment Classification: NLP for Sociological Research

**Hackathon**: "AI & Digital Technologies in Sociological Research" (VCIOM)  
**Team**: aCUtone!  
**Timeline**: November-December 2024  
**Result**: 83% accuracy on multi-class text classification of student opinions

---

## Challenge

VCIOM (Russian Public Opinion Research Center) conducts large-scale research on student opinions for the Ministry of Science and Higher Education. Millions of posts from university social media pages need to be categorized to understand student concerns. The task:

- Classify student posts into 4 thematic categories
- Process thousands of Russian-language social media texts
- Build an automated NLP pipeline to replace manual categorization
- Achieve high accuracy with limited labeled data

**Problem**: Manual categorization of millions of posts is time-consuming, expensive, and inconsistent. An AI solution needed to scale analysis and provide real-time insights into student life.

---

## Solution Overview

We developed a machine learning classification pipeline that automatically categorizes student social media posts into 4 categories with 83% accuracy using traditional NLP and sklearn.

### Categories

**1. Academic & Extracurricular Engagement (471 posts)**
- Teaching quality and professor reviews
- Educational process issues (exams, assignments, deadlines)
- Student activities (clubs, volunteering, sports)

**2. Social & Living Conditions (427 posts)**
- Dormitory issues and campus living
- Food services and cafeterias
- Medical services

**3. Financial Conditions (190 posts)**
- Scholarships and grants
- Tuition fees and financial aid
- Part-time work and student budgets

**4. University Loyalty (320 posts)**
- University reputation and pride
- Recommendation likelihood
- Overall satisfaction with institution

### NLP Pipeline

**1. Data Loading & Preprocessing**
- Merged labeled datasets
- Text cleaning (removed special characters, URLs, mentions)
- Russian stopword removal using NLTK
- Stemming with Snowball Stemmer

**2. Feature Engineering**
- Added category-specific keyword features
- TF-IDF vectorization for text representation
- Train-test split for validation

**3. Model Training**
- Cross-validation for robust evaluation
- Hyperparameter tuning
- Model selection based on accuracy and F1-score

**4. Prediction & Deployment**
- Classified unlabeled posts
- Output predictions with confidence scores

---

## Key Results

**Overall Accuracy** | 83% 
**Posts classified** | 1,408 total 
**Processing speed** | Thousands of posts per second 
**Cost savings** | 70%+ vs manual labor 

### Business Impact

**Speed**: AI processes thousands of posts in seconds vs. hours for human analysts

**Cost**: Neural network operations cost 70%+ less than manual categorization

**Availability**: 24/7 operation without breaks or vacations

**Scalability**: Can be adapted for different data types (texts, reviews, surveys)

---

## My Contribution

- **NLP preprocessing**: implemented text cleaning pipeline (stopword removal, stemming, special character handling for Russian text)
- **Feature engineering**: added category-specific keyword features to improve classification accuracy
- **Model training**: experimented with different sklearn classifiers, performed hyperparameter tuning
- **Evaluation**: conducted cross-validation analysis, calculated accuracy metrics
- **Presentation**: co-developed final presentation showcasing practical applications of the model

---

## Technical Stack

### Libraries & Tools
- **Python**: pandas, numpy (data manipulation)
- **NLP**: NLTK (tokenization, stopwords, stemming)
- **ML**: scikit-learn (classification, vectorization, cross-validation)
- **Presentation**: MS PowerPoint

### Methods & Techniques
- **Text preprocessing**: Russian stopword removal, Snowball stemming
- **Feature extraction**: TF-IDF vectorization
- **Classification**: supervised multi-class classification
- **Validation**: k-fold cross-validation
- **Hyperparameter tuning**: grid search

---

## Use Cases Beyond Academia

### 1. Forum Moderation
Automatically classify forum responses by quality:
- Verified answer
- Good answer
- Incomplete answer
- Spam/irrelevant

### 2. Customer Support
Categorize support tickets by urgency and topic for faster routing

### 3. Social Media Monitoring
Track brand sentiment and categorize customer feedback in real-time

### 4. Survey Analysis
Automatically classify open-ended survey responses by theme

---

## Dataset

- **Source**: University social media pages (VKontakte)
- **Time period**: 2020-2024
- **Size**: ~3,000 labeled posts + thousands unlabeled
- **Language**: Russian
- **Labels**: 4 categories (engagement, living conditions, finances, loyalty)

Dataset provided by VCIOM as part of ongoing research commissioned by the Ministry of Science and Higher Education.

---

## Documentation

- [Team presentation](/презентация_хакатон_ии_вциом.pdf) — solution overview with use cases
- [Labeled dataset](/dataframe_labeled.csv) — training data with categories
- [Full dataset](/dataframe_all.csv) — complete dataset for prediction

---

## About the Competition

**"AI & Digital Technologies in Sociological Research"** is a hackathon organized by VCIOM (Russian Public Opinion Research Center) focusing on applying machine learning to analyze social research data. 

The competition challenged teams to:
- Build NLP models for Russian text classification
- Automate sociological data analysis workflows
- Demonstrate practical business value of AI solutions
- Present findings to VCIOM researchers

This project demonstrates how AI can transform sociological research by automating labor-intensive categorization tasks and enabling real-time analysis of public opinion.

---

## Team

**aCUtone!** — Central University data science team:
- **Timur Nebolsin** — Superfinalist MOS.MSU case championship
- **Mikhail Gavrilov** — T-Bank Math Olympiad prize winner
- **Darya Botyalina** — DANO finalist, interned at KROK
- **Egor Starikov** — Hackathon winner (Central University × T-Bank), Yandex hackathon winner
- **Ivan Kurban** — T-Bank scholarship recipient, Central University Kaggle team member
