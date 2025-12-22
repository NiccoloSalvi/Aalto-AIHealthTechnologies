# Assignment 3: Medical Image Segmentation (Knee MRI)

This repository contains the implementation for **Assignment 3** of the course **AI in Health Technologies (ELEC-E8739)** at **Aalto University**, Fall 2025.

**Instructor:** Prof. Aleksei Tiulpin, PhD.

## Project Overview

The primary goal of this assignment is to develop and understand deep learning pipelines for the **semantic segmentation of knee tissues** (bones and cartilage) from Magnetic Resonance Imaging (MRI) scans. This task is a fundamental step in the computer-aided diagnosis and longitudinal monitoring of **Osteoarthritis (OA)**.

The project focuses on replicating and implementing methodologies inspired by state-of-the-art research (e.g., Panfilov et al., 2019/2022) to enable fully automatic subregional morphological assessment of knee cartilage.

### Task Description

The implementation involves:

* **Segmentation Pipeline:** Building a "slice-by-slice" segmentation framework to process 3D MRI volumes.
* **Architecture & Design:** Leveraging advanced Pythonic patterns, such as **Inheritance** and **Mixins**, to create modular and reusable training components.
* **Data Handling:** Processing knee MRI data, specifically focused on identifying the femur, tibia, and patella, along with their respective cartilage layers.
* **Model Validation:** Implementing robust evaluation metrics and validation strategies crucial for clinical applications where precision is paramount.

## Important Note on Code Comments

Please note that all instructional comments and structural guidelines within the Jupyter Notebook (`main.ipynb`) were **provided by the course instructor, Prof. Aleksei Tiulpin**. These comments served as the pedagogical framework for the assignment, defining the requirements and the logic to be implemented.

## References

1. Panfilov, E., Tiulpin, A., et al. (2019). *Improving robustness of deep learning based knee mri segmentation: Mixup and adversarial domain adaptation*. IEEE/CVF CVPR Workshops.
2. Panfilov, E., Tiulpin, A., et al. (2022). *Deep learning‐based segmentation of knee MRI for fully automatic subregional morphological assessment of cartilage tissues*. Journal of Orthopaedic Research.

---

*Developed as part of the ELEC-E8739 AI in Health Technologies D course - Aalto University.*