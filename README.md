# 💡 Comparative Analysis of ML Models for Breast Cancer Detection

This repository contains the project report **“Comparative Analysis of Decision Trees and Neural Networks for Breast Cancer Detection in Medical Imaging Data.”**  
The study explores the performance of two machine learning models—**Decision Trees (J48)** and **Neural Networks (Multilayer Perceptron)**—for classifying medical imaging data related to breast cancer detection.

---

## 🌟 Project Overview

This study uses the **Weka machine learning platform** and its **breast cancer dataset**, which includes medical imaging data from both cancer-diagnosed patients and healthy individuals.

The primary objective was to determine whether a **statistically significant difference** exists in classification accuracy between:
- **Decision Tree (J48)**
- **Neural Network (Multilayer Perceptron / ANN)**

---

## 🎯 Purpose of the Study

Early detection of breast cancer is critical, as timely intervention significantly improves survival rates. With rapid advancements in **AI and Machine Learning**, automated detection systems have become a promising tool in medical diagnostics.

This project aims to:

- Explore the use of **Decision Trees** and **Neural Networks** for breast cancer detection using medical imaging data.
- Conduct a **comparative analysis** of the classification accuracy of J48 and ANN models.
- Apply **statistical hypothesis testing** to determine whether performance differences between the models are statistically significant.

---

## 🧪 Hypothesis Testing

Each model was executed **30 times** on the same dataset using:
- **66% training / 34% testing split**
- A **different random seed** for each run to ensure independent accuracy samples

Let:
- \( \mu_1 \) = mean accuracy of the Decision Tree (J48)
- \( \mu_2 \) = mean accuracy of the Neural Network (ANN)

### Hypotheses

- **Null Hypothesis (\(H_0\))**:  
  \[
  H_0: \mu_1 = \mu_2
  \]

- **Alternative Hypothesis (\(H_a\))**:  
  \[
  H_a: \mu_1 \neq \mu_2
  \]

A **two-sample t-test assuming equal variances** was conducted using a significance level of \( \alpha = 0.05 \).

> **Variance Check:**  
> An F-test confirmed the assumption of equal variances:  
> - \( F < F_{critical} \) → \( 1.02 < 1.86 \)  
> - p-value \( > 0.05 \) → \( 0.48 > 0.05 \)

---

## 📊 Results and Conclusion

| Statistic | Decision Tree (J48) | Neural Network (ANN) |
|--------|------------------|------------------|
| Mean Accuracy | 0.7013745 | 0.652577333 |
| Observations | 30 | 30 |
| t Stat | 4.848177667 | — |
| P(T ≤ t) two-tail | \( 9.70735 \times 10^{-6} \) | — |
| t Critical (two-tail) | 2.001717484 | — |

### Key Findings

- The **two-tailed p-value** (~\( 9.7 \times 10^{-6} \)) is far below \( \alpha = 0.05 \).
- The **null hypothesis is rejected**.
- The **t-statistic (~4.85)** lies well beyond the critical threshold (\( \pm 2.001 \)).

---

## ✅ Final Conclusion

There is a **statistically significant difference** in performance between the Decision Tree (J48) and the Neural Network (Multilayer Perceptron).

With a higher mean accuracy (**0.701** vs **0.653**), the **Decision Tree (J48)** model **outperformed** the Artificial Neural Network in this breast cancer detection task.

---

## ⏭️ Future Work

A natural next step would be to extend this analysis by comparing the **J48 Decision Tree** with a **Convolutional Neural Network (CNN)** to evaluate performance differences and effectiveness on medical imaging data.

---
