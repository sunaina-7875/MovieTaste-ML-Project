# MovieTaste-ML-Project
“A machine learning project that predicts if a user will like a movie.”
# 🎬 MovieTaste - Machine Learning Project

## 📌 Project Overview
MovieTaste is a Machine Learning project that predicts whether a user will like a movie or not.  
The model is trained on a synthetic dataset of 2500 movies and uses a Random Forest Classifier.

---

## 📊 Dataset
- **Total Movies**: 2500 (synthetic dataset generated for practice).
- **Features (Inputs)**:
  - **Genre**: Action, Comedy, Drama, Sci-Fi, Romance
  - **Rating**: IMDb-style score (1–5)
  - **Popularity**: Number of viewers (100–10,000)
  - **Length**: Movie duration (80–180 minutes)
- **Target (Output)**:
  - **Like = 1** → User will like the movie
  - **Like = 0** → User will not like the movie

---

## 🎭 Genre Encoding
Genres are converted into numeric codes for ML processing:
- Action = 1  
- Comedy = 2  
- Drama = 3  
- Sci-Fi = 4  
- Romance = 5  

---

## 🧩 Training and Testing
- Dataset is split into **80% training** and **20% testing**.
- Training data teaches the model.
- Testing data checks if the model can predict correctly on new movies.

---

## 🌳 Model
- **Algorithm**: Random Forest Classifier (120 decision trees).
- Decision Trees are simple “if–else” rules.
- Random Forest combines many trees to improve accuracy.

---

## 📈 Results

### Accuracy
Model accuracy:1.0
👉 The model achieved 100% accuracy on the synthetic dataset.

### Confusion Matrix
A heatmap graph shows correct vs wrong predictions.  
In this case, all predictions are correct (perfect matrix).

### Classification Report
precision=1.0
recall=1.0
f-1 score=1.0
👉 Every prediction is perfect because the dataset rules are simple.

### Feature Importance
A bar chart shows which features matter most:
- **Rating** and **Popularity** are the most important.
- Length and Genre have less impact.

---

## 🔢 Custom Predictions
You can test your own inputs using the function:

python
print(predict_like(1,4.2,8000,120))
# Output
User will LIKE this movie 🎬
# Example prediction
print(predict_like(1,4.2,8000,120))   # Action movie, high rating
print(predict_like(3,2.5,1500,170))   # Drama movie, low rating
# Output
User will LIKE this movie 🎬
User will NOT like this movie 💔
# conclusion
MovieTaste predicts if a user will enjoy a movie based on its features.
Accuracy is 1.0 because the dataset is synthetic and rules are simple.
With real IMDb data, accuracy would be lower but more realistic.
