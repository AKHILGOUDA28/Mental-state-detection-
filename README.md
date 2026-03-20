# 🧠 EEG Mental State Classification using CNN, LSTM & Machine Learning

## 📌 Project Overview

This project is about predicting human mental state using EEG brainwave signals. EEG data is very complex and noisy, so understanding patterns is not easy. In this work, I tried different approaches starting from deep learning (CNN + LSTM) and then moving to machine learning models like XGBoost and MLP.

Main goal is to build a system which can correctly classify mental states and also understand which features are important.

---

## 🚀 Idea and Innovation

First I started with **CNN + LSTM model** because EEG signals are like time-series data.

* CNN is used to capture **spatial patterns** from signals
* LSTM is used to capture **temporal dependencies (sequence behavior)**

So combining both helps to understand:

> "what pattern is present" + "how pattern changes over time"

But after experimenting, I realized that deep learning is not always best for this dataset. So I moved to machine learning models and did feature engineering and selection.

👉 Main innovation in this project:

* Compared **Deep Learning vs Machine Learning**
* Used **Permutation Feature Importance**
* Reduced features from hundreds → top 50 features
* Applied **Statistical Testing (t-test, Cohen’s d)** to prove results

---

## 🧠 Models Used

### 🔹 1. CNN + LSTM (Deep Learning Approach)

* Handles time-series EEG data
* Captures both spatial and temporal patterns
* Good conceptually but requires more data and tuning

---

### 🔹 2. MLP (Neural Network)

* Simple feedforward network
* Used as baseline deep learning model
* Faster than CNN-LSTM but slightly lower performance

---

### 🔹 3. XGBoost (Best Model 🚀)

* Tree-based ensemble model
* Handles tabular data very efficiently
* No need of heavy preprocessing

👉 This model gave best results in this project

---

## 📊 Results

| Model                     | Accuracy   |
| ------------------------- | ---------- |
| MLP                       | 96.06%     |
| XGBoost (All Features)    | 97.29%     |
| XGBoost (Top 50 Features) | **97.38%** |

---

## 🔍 Key Findings

* Feature selection improved performance
* Many EEG features are redundant
* Only small subset of features is enough
* XGBoost outperformed neural networks

---

## 📈 Statistical Validation

To make results strong, I used:

* **Paired t-test**
* **Cohen’s d (Effect Size)**

Results:

* p-value ≈ 0.053 (very close to significant)
* Cohen’s d = 1.36 → very large effect

👉 This means XGBoost is practically much better than MLP

---

## 📊 Evaluation Metrics

* Accuracy: ~97%
* F1 Score: 0.96
* Balanced performance across all classes
* Confusion matrix shows very low misclassification

---

## 🛠️ Tech Stack

* Python
* Pandas, NumPy
* Scikit-learn
* XGBoost
* TensorFlow / Keras
* Matplotlib, Seaborn

---

## 📁 Dataset

EEG Brainwave Dataset (Mental State Classification)
Available on Kaggle.

---

## 💡 Conclusion

This project shows that:

* Deep learning is powerful but not always best choice
* Feature engineering and model selection is very important
* Simpler models like XGBoost can outperform complex models

Also reducing features helps to:

* Improve speed
* Reduce complexity
* Maintain accuracy

---

## 🔮 Future Work

* Improve CNN + LSTM model with better tuning
* Real-time EEG prediction system
* Build web interface for live prediction
* Try more advanced models like Transformers

---

## 🙋 About Me

I am interested in Data Science and Machine Learning. I like working with real-world data and finding useful insights. This project helped me understand how to compare models properly and validate results using statistics.

---

⭐ If you like this project, feel free to star the repo!
