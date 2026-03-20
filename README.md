# 🧠 EEG Mental State Classification using Machine Learning

## 📌 Project Overview

This project is about predicting human mental state using EEG brainwave signals. EEG data is very complex and noisy, so extracting useful information is challenging.

Initially, I started this project with deep learning models like CNN and LSTM because EEG signals look like time-series data. But later I realized that this dataset is not suitable for deep learning due to its structure and size. So I changed my approach to machine learning models, which gave better performance.

---

## 🚀 Idea and Approach (Important Part)

At the beginning, I used **CNN + LSTM** model.

* CNN helps to capture patterns
* LSTM helps to understand sequence behavior

But during implementation, I faced some problems:

* Dataset is not very large
* Data is already in **tabular format (engineered features)**
* No clear temporal sequence like raw signals
* Deep learning models were taking more time and not giving better accuracy

So I understood that:

👉 *Deep learning is not always best for every dataset*

---

## 🔄 Why I Changed to Machine Learning

After observing above issues, I switched to **machine learning models**.

Reasons:

* Data is structured (not raw signal)
* Features already extracted (mean, variance, kurtosis, etc.)
* Tree-based models work better on this type of data
* Faster training and better performance

👉 Then I used:

* MLP (baseline model)
* XGBoost (main model)

---

## 🧠 Models Used

### 🔹 1. CNN + LSTM (Initial Attempt)

* Used for sequence learning
* But not suitable for this dataset
* Lower performance and high complexity

---

### 🔹 2. MLP (Baseline Model)

* Simple neural network
* Used to compare performance
* Accuracy around 96%

---

### 🔹 3. XGBoost (Final Model 🚀)

* Best performing model
* Works well with tabular data
* No need for heavy preprocessing

---

## 📊 Results

| Model                     | Accuracy   |
| ------------------------- | ---------- |
| MLP                       | 96.06%     |
| XGBoost (All Features)    | 97.29%     |
| XGBoost (Top 50 Features) | **97.38%** |

---

## 🔍 Feature Selection (Important Contribution)

Using permutation importance:

* Many features had zero importance
* Selected top 50 features
* Reduced noise and improved performance

---

## 📈 Statistical Validation

To make results more reliable:

* Used paired t-test
* Calculated Cohen’s d

Results:

* p-value ≈ 0.053 (very close to significant)
* Cohen’s d = 1.36 (large effect size)

👉 Shows strong practical improvement of XGBoost

---

## 💡 Conclusion

This project shows an important learning:

> "Choosing the right model based on data is more important than using complex models."

* Deep learning was not suitable here
* Machine learning performed better
* Feature selection improved results

---

## 🔮 Future Work

* Use raw EEG signals instead of processed features
* Improve deep learning model with larger dataset
* Build real-time prediction system
* Create web interface for predictions

---

## 🙋 About Me

I am interested in Data Science and Machine Learning. This project helped me understand how to select models based on data and how to validate results properly using statistics.

---


⭐ If you like this project, feel free to star the repo!
