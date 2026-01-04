# 💡 Comparative Analysis of ML Models for Breast Cancer Detection

This repository contains the project report **“Comparative Analysis of Decision Trees and Neural Networks for Breast Cancer Detection in Medical Imaging Data.”**  
The study explores the performance of two machine learning models **Decision Trees (J48)** and **Neural Networks (Multilayer Perceptron)** for classifying medical imaging data related to breast cancer detection.

📄 **[View Full Report (PDF)](Detailed_Research_Report.pdf)**

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

### Hypothesis Testing

Each model was executed 30 times using a 66% training and 34% testing split, with a different random seed for each run to ensure independent accuracy samples.

**Let:**
- **mu₁** = mean accuracy of the Decision Tree (J48)
- **mu₂** = mean accuracy of the Neural Network (ANN)

#### Hypotheses

- **Null Hypothesis (H₀):**  
  mu₁ = mu₂

- **Alternative Hypothesis (Hₐ):**  
  mu₁ ≠ mu₂

A two-sample **t-test assuming equal variances** was conducted using a significance level of **α = 0.05**.

> **Variance Check**  
> An F-test confirmed the assumption of equal variances:
> - F < F₍critical₎ → 1.02 < 1.86  
> - p-value > 0.05 → 0.48 > 0.05  

---

### 📊 Results and Conclusion

| Statistic | Decision Tree (J48) | Neural Network (ANN) |
|---------|------------------|------------------|
| Mean Accuracy | 0.7013745 | 0.652577333 |
| Observations | 30 | 30 |
| t Stat | 4.848177667 | — |
| P(T ≤ t) two-tail | 9.70735e-6 | — |
| t Critical (two-tail) | 2.001717484 | — |

---

### 📈 Visualization of the t-Test Results

![T-Distribution with Test Statistic and Rejection Regions](T_Stat_Distribution.png)



The chart above illustrates the **t-distribution** with the **test statistic** and **rejection regions** for a two-tailed t-test.

- The **purple vertical lines** represent the **t-test statistic**, which is approximately **t = 4.85**.
- The **red vertical lines** indicate the **critical values** for a two-tailed test at a significance level of **α = 0.05**, which are **±2.001**.
- The shaded red areas beyond the critical values correspond to the **rejection regions**.

As shown in the chart, the t-test statistic lies **well beyond the critical values**, placing it firmly within the rejection region. This visual evidence supports the statistical conclusion to **reject the null hypothesis**, confirming a statistically significant difference between the two model accuracies.


### 🔑 Key Findings

- The two-tailed p-value (~9.7e-6) is far below the significance level (α = 0.05).
- The null hypothesis is rejected.
- The t-statistic (~4.85) lies well beyond the critical threshold (±2.001).

---

### ✅ Final Conclusion

There is a **statistically significant difference** in performance between the Decision Tree (J48) and the Neural Network (Multilayer Perceptron).

With a higher mean accuracy (0.701 vs 0.653), the **Decision Tree (J48)** outperformed the **Artificial Neural Network (ANN)** for breast cancer detection in this experimental setting.


## ⏭️ Future Work

A natural next step would be to extend this analysis by comparing the **J48 Decision Tree** with a **Convolutional Neural Network (CNN)** to evaluate performance differences and effectiveness on medical imaging data.

---
