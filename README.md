# 📰 Fake News Detection 

## 📌 Overview
The spread of **fake news** on social media platforms poses a serious threat to public trust, democracy, and information integrity.  
Our project leverages **Machine Learning** to detect fake news **directly from the text content** of news articles, providing a smarter alternative to outdated blacklists of fake news sources.

Instead of rigidly checking articles against pre-labeled fake news lists, we train a **text classification model** that can **predict whether a news source is likely to produce fake news** based on multiple articles from that source.

> 🎯 **Goal:** Help social media platforms reduce the visibility of potentially fake content by assigning **visibility weights** to articles.

---

## 🚀 Problem Definition
Traditional fake news detection methods (checking against static lists) are **inflexible** and **easy to bypass**.  
Our ML-driven approach:

- Trains on a **corpus of labeled news articles** (real and fake).
- Classifies the likelihood of a **news source** being fake based on multiple articles.
- Reduces **misclassification errors** by focusing on **source-level detection**.
- Outputs predictions that can be integrated into **social media ranking algorithms**.

---

## 🛠 Tech Stack

**Frontend**  
- HTML, CSS (Templates: `index.html`, `prediction.html`)

**Backend**  
- Python (Flask)
- Pandas, NumPy
- Scikit-learn (ML Models)
- Pickle (`finalized_model.pkl`, `vectorizer.pkl`)



---

## 📂 Project Structure
```plaintext
📦 Fake News Detection
├── static/
│   └── image.svg — UI logo/icon
├── templates/
│   ├── index.html — Homepage UI
│   └── prediction.html — Prediction result page
├── app.py — Flask backend application
├── news.csv — Dataset (real & fake news)
├── finalized_model.pkl — Trained ML model
├── vectorizer.pkl — Text vectorizer
├── requirements.txt — Dependencies
├── Procfile — Deployment config
└── README.md — Documentation
```

---

## 📊 How It Works

1. **Data Collection**  
   - A labeled dataset (`news.csv`) containing both real and fake news articles is used.

2. **Data Preprocessing**  
   - Tokenization, stopword removal, and vectorization using **TF-IDF**.

3. **Model Training**  
   - ML algorithm (e.g., Logistic Regression / Naive Bayes) trained on the dataset.
   - Model saved as `finalized_model.pkl` and vectorizer as `vectorizer.pkl`.

4. **Prediction Pipeline**  
   - Flask backend loads model & vectorizer.
   - User submits article text.
   - Model predicts if the news is **Real** or **Fake**.


---

## 📸 Screenshots

### 🏠 Homepage
![home page.png](https://github.com/lokeshkolapati/Fake_News_Detection/blob/main/home%20page.png)

### 📌 Prediction Page
![prediction page](https://github.com/lokeshkolapati/Fake_News_Detection/blob/main/prediction%20page.png)


---

## 📦 Installation & Usage

### 1️⃣ Clone the repository
```bash
git clone https://github.com/yourusername/fake-news-detection.git
cd fake-news-detection
```
### 2️⃣ Install dependencies
```bash
pip install -r requirements.txt
```
### 3️⃣ Run locally
```bash
python app.py
```
- Visit: http://127.0.0.1:5000

## 🔮 Future Enhancements
- Use deep learning models (LSTMs, Transformers).
- Include image analysis for detecting manipulated visuals.
- Multi-language fake news detection.
- Real-time API for social media platforms.
## 💡 "In a world full of information, truth is our most powerful weapon."
