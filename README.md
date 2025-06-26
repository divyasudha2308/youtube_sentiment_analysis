# 📽️ Sentiment-Based Model for Recommender Systems

This project integrates **sentiment analysis** and **deep learning** into a recommender system to improve video recommendations using user comments. It is designed to address the **cold-start** and **data sparsity** problems in traditional recommendation systems by predicting sentiment from text using **VADER** and a custom **CNN model**.

## 🔍 Problem Statement

Conventional recommender systems rely heavily on user ratings. However, when new content or users are added (cold-start), or when very few ratings are available (data sparsity), these systems perform poorly. Our approach uses **user-generated comments** to predict sentiment ratings, enabling more robust and personalized recommendations.

---

## 🎯 Objectives

- Extract sentiment scores from YouTube comments using **VADER**
- Train a **Convolutional Neural Network (CNN)** to classify sentiment ratings (1–5)
- Generate video recommendations based on predicted sentiment
- Visualize sentiment distribution with pie charts and graphs

---

## 🧠 Tech Stack

| Area          | Technology                  |
|---------------|-----------------------------|
| Frontend      | HTML                        |
| Backend       | Python, Django              |
| NLP Tool      | VADER                       |
| Deep Learning | TensorFlow, Keras           |
| Data Handling | Pandas                      |
| Visualization | Matplotlib                  |

---

## 📁 Dataset

- **Source**: YouTube video comments and ratings
- **Split**: 80% training / 20% testing
- **Format**: CSV file containing comment text and ground truth ratings

---

## 🛠️ Modules Implemented

1. **Sentiment Extraction** using VADER
2. **CNN Model** for classifying comments into rating categories (1–5)
3. **Recommendation Engine** using predicted sentiment
4. **Bulk Prediction** from CSV files
5. **Graphical Visualization** of sentiment ratings

---

## 🧪 Testing and Evaluation

- **Metric Used**: RMSE (Root Mean Square Error)
- **Validation Strategy**:
  - `ModelCheckpoint` to save best CNN model weights
  - `EarlyStopping` to prevent overfitting
- **Output Testing**:
  - Individual comment prediction
  - Batch comment prediction with pie chart output

---

## 🚀 How to Run

```bash
# 1. Clone the repository
git clone https://github.com/yourusername/sentiment-recommender.git
cd sentiment-recommender

# 2. Create a virtual environment and activate
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run the Django server
python manage.py runserver
