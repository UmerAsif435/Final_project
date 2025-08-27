# Final_project
Final Dissertation


---


## Project Overview

This dissertation explores the use of deep learning for classifying chest X-ray images into three diagnostic categories: **Normal**, **Lung Opacity**, and **Viral Pneumonia**. The study compares a baseline **Custom CNN** with two transfer learning models—**MobileNetV2** and **VGG16**—to evaluate trade-offs between accuracy and computational efficiency.

The project demonstrates the potential of transfer learning in medical image analysis and highlights how deep learning can support radiologists in improving diagnostic reliability.

---

## Project Structure

* `data/` → Chest X-ray dataset (from Kaggle)
* `notebooks/` → colab/jupyter notebooks containing EDA, model training, and evaluation
* `results/` → Accuracy/loss curves, confusion matrices, and prediction outputs
* `figures/` → Workflow diagrams (Custom CNN, MobileNetV2, VGG16)
* `report/` → Final dissertation document (Word/PDF)

---

## Methodology

1. **Exploratory Data Analysis (EDA):**

   * Examined dataset structure, class distribution, and representative images
   * Verified dataset balance across three classes

2. **Model Development:**

   * **Custom CNN:** Baseline model with three convolutional blocks
   * **MobileNetV2:** Lightweight transfer learning model with frozen base layers
   * **VGG16:** Deep transfer learning model with superior feature extraction capacity

3. **Training Strategy:**

   * Image size: 224 × 224
   * Batch size: 32
   * Optimizer: Adam (lr=0.0001)
   * Early stopping (patience=5)
   * Epochs: 25–30

4. **Evaluation Metrics:**

   * Accuracy and Loss curves
   * Confusion matrices
   * Precision, Recall, F1-score

---

## Key Results

* **Custom CNN:** 83% accuracy, struggled with subtle distinctions between Normal and Lung Opacity
* **MobileNetV2:** 84% accuracy, balanced performance with efficiency advantages
* **VGG16:** 89% accuracy, strongest performance across all classes but higher computational cost

---

## Conclusion

* Transfer learning significantly improved performance compared to the baseline CNN
* **MobileNetV2** is ideal for efficiency in resource-constrained environments
* **VGG16** provides maximum diagnostic accuracy, making it suitable for clinical decision-support systems

---

## Future Work

* Expand dataset for improved generalisation
* Apply advanced augmentation and preprocessing techniques
* Incorporate explainability tools (Grad-CAM, SHAP) for clinical interpretability
* Explore ensemble modelling to balance accuracy and efficiency

---

## Requirements

To run the notebooks, install the following libraries:

```bash
pip install tensorflow keras matplotlib seaborn scikit-learn
```

---

