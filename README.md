# Deep Learning - Project 3

## Team Members:
- **Rahil Singhi** (rs9174@nyu.edu)  
- **Alper Mumcular** (am14533@nyu.edu)  
- **Divya Srinivasan** (ds7852@nyu.edu)  

### Institution:  
New York University

---

## Project Overview

This is the third project for the Deep Learning course at NYU. The objective of this project was to perform adversarial attacks on a pre-trained ResNet-34 model using the ImageNet-1K dataset. The goal was to significantly degrade model performance using imperceptible perturbations under various constraints.

---

## Tasks and Summary

### Task 1: Baseline Evaluation
- Evaluated the pre-trained ResNet-34 model on the given subset of the ImageNet-1K dataset.
- Achieved a **Top-1 Accuracy of 76.0%** and **Top-5 Accuracy of 94.2%**.

### Task 2: Pixel-wise Attacks (FGSM)
- Implemented FGSM (Fast Gradient Sign Method) with ε = 0.02.
- Generated **Adversarial Test Set 1**.
- Achieved a **Top-1 Accuracy of 6.0%** and **Top-5 Accuracy of 35.6%**.

### Task 3: Improved Attacks
- Designed a multi-step gradient attack using PGD (Projected Gradient Descent).
- Generated **Adversarial Test Set 2**.
- Achieved a **Top-1 Accuracy of 0%** and **Top-5 Accuracy of 7.8%** for Iterative-FGSM.
- Achieved a **Top-1 Accuracy of 0%** and **Top-5 Accuracy of 8%** for PGD.

### Task 4: Patch Attacks
- Restricted attack to a **32x32** random patch with ε = 0.5 (between 0.3 - 0.5).
- Used a targeted PGD-style attack.
- Generated **Adversarial Test Set 3**.
- Achieved a **Top-1 Accuracy of 27.8%** and **Top-5 Accuracy of 67.6%**.

### Task 5: Transferability
- Evaluated all datasets (original and adversarial) on DenseNet-121 to observe transferability.
- Observed consistent drop in performance across all three adversarial test sets, showing high transferability of attacks.

---

## Results

| **Model**     | **Dataset/Task**         | **Top-1 Accuracy** | **Top-5 Accuracy** |
|---------------|--------------------------|--------------------|--------------------|
| ResNet-34     | Baseline                 | 76.0%              | 94.2%              |
| ResNet-34     | Task 2: FGSM             | 6.0%               | 35.6%              |
| ResNet-34     | Task 3: Iterative FGSM   | 0.0%               | 7.8%               |
| ResNet-34     | Task 3: PGD              | 0.0%               | 8.0%               |
| ResNet-34     | Task 4: Patch PGD        | 27.8%              | 67.6%              |
| DenseNet-121  | Baseline                 | 76.0%              | 94.2%              |
| DenseNet-121  | FGSM Transfer            | 63.2%              | 89.2%              |
| DenseNet-121  | PGD Transfer             | 64.4%              | 90.6%              |
| DenseNet-121  | Patch Attack Transfer    | 70.2%              | 91.8%              |

---

## Report:
- A detailed report for the project can be found in the file:  
  `project3_report.pdf`

---

## Setup & Execution:

1. **Upload** `DL_Project3_Final.ipynb` to **Google Colab**.
2. **Upload** `TestDataSet.zip` to **Google Colab**.
3. **Run all cells** in the notebook.


---

## Notes:
- All attacks conform to the ε constraints specified in the problem statement.
- Visualizations for adversarial examples can be found in the respective notebook.
