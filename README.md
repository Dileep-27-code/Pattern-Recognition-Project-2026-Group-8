
# Pattern Recognition Project - Monsoon 2026

## Project Overview

This repository contains the implementation of a Pattern Recognition project for the Monsoon 2026 semester. The objective is to perform **multi-class ECG heartbeat classification (5 classes)** using machine learning techniques to address the real-world problem of automated cardiac arrhythmia detection.

The project utilizes the **MIT-BIH Arrhythmia Dataset** and implements a comprehensive feature extraction pipeline incorporating:

- **Statistical Features** – Extracting statistical characteristics of ECG signals.
- **Morphological Features** – Capturing waveform shape and structural characteristics.
- **Discrete Wavelet Transform (DWT) Features** – Analyzing ECG signals across multiple frequency scales.

The extracted features are evaluated using classical machine learning classifiers:

- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)
- Random Forest (RF)

Model performance is evaluated using **5-Fold Stratified Cross-Validation**, ensuring reliable and consistent assessment across all five heartbeat categories.

---

## Project Structure

```text
Project/
│
├── main.py                         # Main execution script
│                                   # Extracts dataset From Kaggle Directly, runs pipeline,
│                                   # and displays evaluation metrics
│
├── pr_colab.ipynb                 # Complete analysis and model training notebook
│
├── requirements.txt                # Project dependencies
│                                   # NumPy, Pandas, Scikit-learn, etc.
│
├── README.md                       # Project documentation
│
└── pr_pre_processed/                # Pre-computed feature arrays
    │                               # Avoids uploading the ~400 MB raw dataset
    │
    ├── X_dwt.npy                  # DWT feature matrix
    ├── X_morph.npy                # Morphological feature matrix
    ├── X_stat.npy                  # Statistical feature matrix
    ├── y.npy                       # Target class labels
    │
    ├── pr_pre_processed_py.py      # Feature extraction and preprocessing script
    ├── pre_processed_colab.ipynb   # Original preprocessing notebook
    └── pre_process_read_me.txt     # Preprocessing instructions
```

---

## Dataset

**MIT-BIH Arrhythmia Dataset**

The project uses the MIT-BIH Arrhythmia Dataset for ECG heartbeat classification.

- Dataset: [MIT-BIH Arrhythmia Dataset - Kaggle](https://www.kaggle.com/datasets/shayanfazeli/heartbeat)
- Task: Multi-class classification
- Number of classes: 5
- Learning type: Supervised learning

---

## Feature Extraction

Three different feature extraction techniques are implemented:

| Feature Type | Description |
|---|---|
| Statistical | Statistical characteristics of ECG signals |
| Morphological | ECG waveform shape and morphological characteristics |
| DWT | Multi-resolution time-frequency representation |

The extracted feature matrices are stored as NumPy arrays inside `pr_pre_processed/` to avoid repeatedly performing computationally expensive preprocessing.

---

## Machine Learning Models

The following classifiers are implemented and evaluated:

| Model | Description |
|---|---|
| SVM | Support Vector Machine |
| KNN | K-Nearest Neighbors |
| RF | Random Forest |

### Evaluation Method

- 5-Fold Stratified Cross-Validation
- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix


## Project Objective

To investigate and compare different feature extraction techniques and classical machine learning classifiers for automated ECG heartbeat classification, identifying effective approaches for recognizing different heartbeat categories.

---

## Technologies Used

- Python
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- SciPy
- PyWavelets
- Jupyter Notebook

---

## Contributors

- P. Dileep Kumar [S20240020323]
- M. Jaswanth [S20240020303]

  
Pattern Recognition Project - Monsoon 2026

