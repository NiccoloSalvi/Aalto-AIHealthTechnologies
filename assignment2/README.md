# Assignment 2: Medical Image Classification (Knee Osteoarthritis)

This repository contains the implementation for **Assignment 2** of the course **AI in Health Technologies (ELEC-E8739)** at **Aalto University**, Fall 2025.

**Instructor:** Prof. Aleksei Tiulpin, PhD.

## Project Overview

The goal of this assignment is to develop a deep learning-based system for the automated diagnosis of **Knee Osteoarthritis (OA)** using plain radiographs. The project focuses on the classification of knee images according to the **Kellgren-Lawrence (KL) grading system**, which is the clinical gold standard for assessing the severity of OA.

The implementation is a simplified version of the deep learning architecture and pipeline proposed in the research paper *Tiulpin et al. (2018)*.

### Task Description

The assignment required the implementation of a professional-grade medical imaging pipeline, specifically:

* **Custom Neural Network Architecture:** Building a Convolutional Neural Network (CNN) from scratch in PyTorch, specifically designed to process knee joint radiographs.
* **Data Pipeline & Augmentation:** Implementing advanced data loading and augmentation strategies using the `solt` library to handle medical imaging data effectively.
* **Robust Evaluation Framework:** * Implementation of **5-fold Stratified Group K-Fold cross-validation**. This ensures that the model is evaluated fairly by preventing data leakage (images from the same patient are never shared between training and validation sets).
* **Performance Metrics:** Analyzing model performance using metrics suitable for clinical settings, such as **Balanced Accuracy** and the **Cohen’s Kappa coefficient** to account for class imbalance in the dataset.

## Important Note on Code Comments

Please note that all instructional comments, pedagogical guidelines, and structural definitions within the provided notebook were **authored by Prof. Aleksei Tiulpin**. These comments were provided to guide the implementation of the assignment according to the course requirements.

## References

1. **Tiulpin, A.**, Thevenot, J., Rahtu, E., Lehenkari, P., & Saarakkala, S. (2018). *Automatic knee osteoarthritis diagnosis from plain radiographs: a deep learning-based approach*. Scientific Reports, 8(1), 1727.

---

*Developed as part of the ELEC-E8739 AI in Health Technologies D course - Aalto University.*