# 🧠 Customer Support Ticket Classification Model

An end-to-end Machine Learning and NLP-based project designed to automatically classify customer support tickets into predefined categories — **Billing Issue**, **Technical Problem**, **Order Status**, and **General Query** — improving efficiency and consistency in customer service.

---

## 📌 Project Overview

E-commerce platforms handle thousands of customer queries daily. Manual classification of these tickets leads to delays and inconsistencies.  
This project automates that process using **Natural Language Processing (NLP)** and **Machine Learning**, enabling faster and more accurate ticket routing.

---

## 🎯 Objectives

- Automate the classification of customer support tickets.
- Improve accuracy and response time in customer service.
- Build an end-to-end ML pipeline including preprocessing, model training, and deployment.

---

## 📊 Dataset

- **Source:** Synthetic dataset generated with the help of ChatGPT.
- **File:** `flipkart_ticket_dataset_augmented.csv`
- **Records:** 1,750
- **Columns:**
  - `TicketID` – Unique identifier
  - `Description` – Ticket text
  - `Category` – Target class (Billing Issue, Technical Problem, Order Status, General Query)

---

## ⚙️ Preprocessing Steps

- Lowercasing  
- Removing special characters and punctuation  
- Tokenization and Stopword Removal  
- Lemmatization  
- Saving the cleaned dataset as `flipkart_ticket_dataset_cleaned.csv`

---

## 🧩 Feature Engineering

- **Technique:** TF-IDF Vectorization  
- **Parameters:**
  - `ngram_range = (1, 2)`
  - `max_features = 5000`
  - `stop_words = 'english'`

---

## 🤖 Model Training

Models trained and compared:
- Naive Bayes  
- Logistic Regression  
- Linear SVC ✅ (Selected Model)
- XGBoost

**Best Model:** Linear SVC  
**Accuracy:** 97.23%  
**F1-Score:** 0.8974

---

## 🧪 Evaluation

| Model | Accuracy | F1-Score |
|--------|-----------|-----------|
| Naive Bayes | 96.43% | 0.8898 |
| Logistic Regression | 96.84% | 0.8942 |
| **Linear SVC** | **97.23%** | **0.8974** |
| XGBoost | 81.85% | 0.7611 |

---

## 🚀 Deployment

The final model is deployed using **Flask** with a simple **HTML frontend**.

### Steps to run:
1. Load the Dataset
2. Rull all the cells upto Flask App
3. After creation of a folder called " Frontend  " by executing the code cell add index.html file manually.
4. Run the Flask app locally
