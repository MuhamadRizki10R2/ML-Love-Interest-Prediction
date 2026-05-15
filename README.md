# 💬 Love Interest Prediction Using XGBoost

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python">
  <img src="https://img.shields.io/badge/XGBoost-Machine%20Learning-orange?style=for-the-badge">
  <img src="https://img.shields.io/badge/Scikit--Learn-ML-yellow?style=for-the-badge&logo=scikitlearn">
  <img src="https://img.shields.io/badge/Pandas-Data%20Processing-black?style=for-the-badge&logo=pandas">
  <img src="https://img.shields.io/badge/Numpy-Numerical%20Computing-blue?style=for-the-badge&logo=numpy">
</p>

---

# 📌 Description

This project is a Machine Learning system that predicts whether someone is interested in you based on chat conversations.

The model analyzes:
- Response patterns
- Word usage
- Message intensity
- Emoji usage
- Conversation behavior
- Sentiment patterns

Using:
- XGBoost Classifier
- NLP preprocessing
- Feature Engineering

---

# 🧠 Machine Learning Algorithm

## XGBoost Classifier

XGBoost is used because:
- High accuracy
- Fast training
- Good performance for classification tasks
- Handles structured features efficiently

---

# ⚙️ Features

✅ Chat text preprocessing  
✅ Cleaning text using Regex  
✅ Tokenization  
✅ Feature extraction  
✅ TF-IDF Vectorization  
✅ XGBoost model training  
✅ Prediction system  
✅ Accuracy evaluation  
✅ Save & load trained model  

---

# 🛠️ Technologies Used

| Technology | Description |
|---|---|
| Python | Main programming language |
| Pandas | Data processing |
| NumPy | Numerical computation |
| Regex | Text cleaning |
| Scikit-learn | ML tools |
| XGBoost | Machine learning algorithm |
| Joblib | Save/load model |
| Matplotlib | Data visualization |

---

# 📂 Project Structure

```bash
love-interest-prediction/
│
├── dataset/
│   └── chats.csv
│
├── models/
│   └── xgboost_model.pkl
│
├── notebooks/
│   └── training.ipynb
│
├── src/
│   ├── preprocessing.py
│   ├── feature_engineering.py
│   ├── train.py
│   └── predict.py
│
├── outputs/
│   └── results.png
│
├── requirements.txt
└── README.md
```

---

# 🚀 Installation

## 1. Clone Repository

```bash
git clone https://github.com/MuhamadRizki10R2/ML-Love-Interest-Prediction
.git
```

---

## 2. Enter Project Folder

```bash
cd ML-Love-Interest-Prediction
```

---

## 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

# 📦 Requirements

Example `requirements.txt`

```txt
pandas
numpy
scikit-learn
xgboost
matplotlib
joblib
```

---

# 📊 Dataset Format

Example dataset:

| chat | label |
|---|---|
| good morning ❤️ | interested |
| ok | neutral |
| leave me alone | not_interested |

Example CSV:

```csv
chat,label
"good morning ❤️",interested
"where are you?",neutral
"leave me alone",not_interested
```

---

# 🧹 Text Preprocessing

The preprocessing pipeline includes:

- Lowercase conversion
- Remove punctuation
- Remove numbers
- Remove special characters
- Remove extra spaces
- Regex cleaning

Example:

```python
import re

def clean_text(text):
    text = text.lower()
    text = re.sub(r'[^a-zA-Z\s]', '', text)
    return text
```

---

# 🔍 Feature Extraction

Using:

## TF-IDF Vectorizer

```python
from sklearn.feature_extraction.text import TfidfVectorizer

vectorizer = TfidfVectorizer()
X = vectorizer.fit_transform(texts)
```

---

# 🏋️ Model Training

Example training code:

```python
from xgboost import XGBClassifier

model = XGBClassifier()

model.fit(X_train, y_train)
```

---

# 💾 Save Model

```python
import joblib

joblib.dump(model, 'models/xgboost_model.pkl')
```

---

# 📥 Load Model

```python
model = joblib.load('models/xgboost_model.pkl')
```

---

# 🔮 Prediction Example

```python
chat = ["good morning cantik ❤️"]

prediction = model.predict(chat)

print(prediction)
```

Output:

```bash
Interested ❤️
```

---

# 📈 Model Evaluation

Metrics used:
- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

Example:

```python
from sklearn.metrics import accuracy_score

accuracy = accuracy_score(y_test, y_pred)

print(accuracy)
```

---

# 📊 Visualization

Example confusion matrix visualization:

```python
import matplotlib.pyplot as plt
```

---

# 🧪 Example Labels

| Label | Meaning |
|---|---|
| interested | Person likes you |
| neutral | Normal conversation |
| not_interested | Person not interested |

---

# 🔥 Future Improvements

- [ ] Deep Learning Version
- [ ] LSTM Model
- [ ] BERT NLP Model
- [ ] Real-time Chat Prediction
- [ ] Web Application
- [ ] Mobile App
- [ ] Indonesian Slang Detection
- [ ] Voice Message Analysis
- [ ] Emoji Sentiment Analysis

---

# 🤝 Contributing

Contributions are welcome.

Steps:
1. Fork repository
2. Create new branch
3. Commit changes
4. Push branch
5. Open Pull Request

---

# ⭐ Support

If you like this project:

⭐ Star this repository  
🍴 Fork this repository  
📢 Share with others  

---

# 📜 License

This project is licensed under the MIT License.

---

# 👨‍💻 Author

Made with ❤️ by **Muhamad Rizki**

GitHub:
```bash
https://github.com/yourusername
```

---

# 🧠 AI & Machine Learning Project

This repository is part of experimental AI/ML research focused on:
- Human interaction analysis
- Chat pattern recognition
- Behavioral prediction systems
- NLP experimentation

---
