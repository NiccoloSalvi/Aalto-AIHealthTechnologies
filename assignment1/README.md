# Assignment 1: Machine Learning Fundamentals in Healthcare

This repository contains the implementation for **Assignment 1** of the course **AI in Health Technologies (ELEC-E8739)** at **Aalto University**, Fall 2025.

**Instructor:** Prof. Aleksei Tiulpin, PhD.

## Project Overview and Task Description

The objective of this assignment is to apply fundamental machine learning concepts to a clinical prediction problem. The project focuses on predicting treatment response in patients with **Major Depressive Disorder (MDD)** based on clinical data (e.g., age, gender, and Hamilton Rating Scale for Depression scores).

The task involves conducting a scientific numerical experiment to evaluate and compare the performance and stability of different machine learning models under varying hyperparameter settings.

### Implemented Tasks

* **Scientific Experimentation:** Designing a numerical experiment to analyze how hyperparameter selection affects model performance (accuracy) and stability (consistency).
* **Model Comparison:** Implementing and comparing **Decision Trees (DT)** and **Random Forests (RF)** to determine which architecture is better suited for clinical response prediction.
* **Dimensionality Reduction & Visualization:** Using **Principal Component Analysis (PCA)** to visualize the experimental results and observe how models cluster in the hyperparameter space.
* **Statistical Analysis:** Implementing **Permutation Tests** to rigorously compare the mean performance (ROC-AUC) and the variance (stability) between the models, ensuring that the findings are statistically significant.
* **Clinical Relevance:** Interpreting results within the context of predicting "Responders" vs. "Non-responders" to antidepressant treatment.

## Key Findings (Summary)

Based on the implementation, the project demonstrates that **Random Forest** typically outperforms Decision Trees in this clinical setup, showing both higher mean ROC-AUC and significantly better stability (lower variance) across different hyperparameter configurations, as confirmed by the permutation tests.

---

*Developed as part of the ELEC-E8739 AI in Health Technologies D course - Aalto University.*\