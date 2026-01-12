# AI in Health Technologies (ELEC-E8739): Final Project 
**Knee cartilage Segmentation via soft label regression**

* **Professor:** Prof. Aleksei Tiulpin, PhD
* **Term:** Fall 2025

---

## 1. Project Overview 
The final project for this course challenges you to synthesize and extend concepts beyond what is readily available. The core task is to adapt uncertainty-aware segmentation methods from the SAUNA papers [1, 2] to the cartilage segmentation problem from Assignment 3.

**Key Requirements:**
* **Reframing Segmentation:** Instead of treating segmentation as a binary classification problem (0 or 1), you will reframe it as a regression problem.
* **Soft Labels:** You must create "soft" ground truth labels that encode spatial uncertainty.
* **Implicit Neural Networks:** Train your network to predict these continuous values.
* **Collaboration:** This project is completed in groups of three.



## 2. Core Technical Challenge 

### 2.1 Ground Truth Transformation 
Assignment 3 uses "hard" masks (0, 1, 2...). You must implement a transformation to convert these into "soft" regression targets that capture uncertainty.

* **Signed Distance Fields (SDFs):** This is a robust and highly recommended approach.
* **Mechanism:** An SDF maps each coordinate $(x, y)$ to its distance to the nearest boundary.
* **Signs:** The sign indicates if the coordinate is inside (negative) or outside (positive) the object.
* **Geometric Information:** This provides a continuous label rich in geometric information that encodes the boundary, the primary source of uncertainty.


### 2.2 Model and Loss 
For simplicity, all analysis can be performed in 2D.

* **Model Output:** The implicit neural field (INR) must be adapted so its final layer outputs a single continuous value (predicted distance) instead of a binary logit.
* **Loss Function:** Replace classification losses (like BCE or Dice) with a regression loss.
* **Recommended Losses:** A simple L1 loss $(|y_{true}-y_{pred}|)$ is a strong starting point. You are encouraged to explore L2 (MSE) or Focal-L1 loss.
---

## 3. Deliverables 
Your group should submit a single ZIP file containing:
1. **Google Colab Notebook:** A single, runnable `.ipynb` file that is well-commented and executes from start to finish.
2. **README File:** Instructions on how to run the notebook and arrange data.
3. **Project Report:** A 4-page, 2-column report in the IEEE template style.

---

## 4. Grading Criteria 
| Criterion | Weight | Requirement |
| :--- | :--- | :--- |
| **Code Correctness & Quality** | **30%** | Code runs on Colab without errors and is logically structured. |
| **Report Quality** | **30%** | Must include insights and plots of training/validation loss curves. |
| **Data Splitting** | **10%** | Implement a patient-aware train/test split (no data from the same patient in both sets). |
| **Baseline & Improvement** | **10%** | Define a "trivial baseline" and demonstrate improvement with the regression method. |
| **Statistical Testing** | **10%** | Formally compare performance using tests like a paired t-test or Wilcoxon signed-rank test. |
| **Ablation Studies** | **10%** | Analyze design choices (e.g., L1 vs. L2 loss or SDF vs. binary masks). |
---

## 5. Report Guidelines 
The report must follow the IEEE format and include:
* **Introduction:** Problem description and the proposed approach.
* **Methods:** Preprocessing, baseline model, and loss functions used.
* **Experiments:** Training setup, results, and ablation studies.
* **Conclusion:** Summary of findings.
* **Member Contributions:** Responsibilities of each group member.

---

## References
* [1] T. D. Dang, et al. "Image-level regression for uncertainty-aware retinal image segmentation," WACV, 2025.
* [2] T. Dang, et al. "Singr: Brain tumor segmentation via signed normalized geodesic transform regression," MICCAI, 2024.
* [3] E. Panfilov, et al. "Improving robustness of deep learning based knee mri segmentation," ICCVW, 2019.
* [4] E. Panfilov, et al. "Deep learning-based segmentation of knee mri...", Journal of Orthopaedic Research, 2022.