# Asteroids, Algorithms, and Explainability: A Unified Framework for Efficient Classification of Near-Earth Objects

## Overview

This repository contains the implementation of a comprehensive framework for asteroid based analsis using machine learning, deep learning, and explainable artificial intelligence (XAI) techniques. The objective of this study is to accurately classify potentially hazardous asteroids (PHAs) using orbital and physical characteristics while ensuring model interpretability through multiple explainability methods. The framework evaluates several state-of-the-art models and investigates the impact of class imbalance handling techniques on prediction performance.

## Key Features

* Data preprocessing and feature engineering
* Class imbalance handling using:

  * SMOTE
  * ADASYN
  * Tomek Links
  * SMOTE-Tomek
* Traditional machine learning models
* Deep learning architectures
* Transformer-based models
* Explainable AI techniques:

  * SHAP
  * LIME
  * Shapash
* Statistical significance testing

---

## Repository Structure

```text
.
├── data/
│   └── classast-pha1.csv
│
├── notebooks/
│   └── Asteroid_prediction.ipynb
│
├── figures/
│   └── generated plots and visualizations
│
├── requirements.txt
├── README.md
└── LICENSE
```

---

## Dataset

The dataset contains asteroid-related attributes used to predict whether an asteroid is potentially hazardous.

Typical features include:

| Feature                  | Description                         |
| ------------------------ | ----------------------------------- |
| Semi-major axis          | Orbital size                        |
| Eccentricity             | Orbit shape                         |
| Inclination              | Orbital inclination                 |
| Perihelion distance      | Closest distance to the Sun         |
| Aphelion distance        | Farthest distance from the Sun      |
| MOID                     | Minimum Orbit Intersection Distance |
| Absolute magnitude       | Asteroid brightness                 |
| Other orbital parameters | Additional predictive features      |

Target Variable:

* Hazardous (1)
* Non-Hazardous (0)

---

## Methodology

The overall workflow of the proposed framework is shown below:

```text
Dataset
   │
   ▼
Data Cleaning
   │
   ▼
Feature Selection
   │
   ▼
Class Balancing
(SMOTE / ADASYN / Tomek Links)
   │
   ▼
Train-Test Split
   │
   ▼
Model Development
   │
   ├── Machine Learning Models
   ├── Deep Learning Models
   ├── TabNet
   ├── FT-Transformer
   └── SAN
   │
   ▼
Performance Evaluation
   │
   ▼
Explainable AI Analysis
(SHAP, LIME, Shapash)
```

---

## Implemented Models

### Deep Learning Models

* CNN-LSTM-Attention
* GRU-Attention
* LSTM-Based Networks

### Transformer-Based Models

* FT-Transformer
* TabNet
* Self-Attention Network (SAN)

### Baseline Models

Additional machine learning baselines are included for comparison.

---

## Explainable AI

To improve transparency and interpretability, the following XAI techniques are used:

### SHAP

SHAP values quantify the contribution of each feature to model predictions.

### LIME

LIME provides local explanations for individual predictions.

### Shapash

Shapash offers interactive visualization and interpretation of model outputs.

---

## Statistical Analysis

Statistical significance testing is performed to compare model performance and verify the robustness of experimental results.

Methods include:

* Paired statistical tests
* Performance comparison across models
* Evaluation under different balancing strategies

---

## Installation

### Clone the Repository

```bash
git clone https://github.com/your-username/your-repository.git

cd your-repository
```

### Create Environment

```bash
python -m venv venv

source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Running the Notebook

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
notebooks/Asteroid_prediction.ipynb
```

Run all cells sequentially to reproduce the experiments.

---

## Reproducibility

To ensure reproducibility:

* Fixed random seeds are used where applicable.
* All preprocessing steps are included in the notebook.
* Hyperparameter configurations are documented.
* Evaluation metrics are generated automatically.

---

## Results

The framework evaluates multiple predictive models using:

* Accuracy
* Precision
* Recall
* F1-Score
* ROC-AUC
* Confusion Matrix

Detailed experimental results and visualizations are available within the notebook.

---

## Requirements

Example dependencies:

```text
numpy
pandas
scikit-learn
tensorflow
keras
torch
pytorch-tabnet
imbalanced-learn
shap
lime
shapash
matplotlib
seaborn
plotly
```

## License

The code is made available to support the reproducibility of the results presented in the associated manuscript. Licensing terms will be determined upon publication.

---

## Contact

For questions, suggestions, or collaboration opportunities, please contact the corresponding author through the information provided in the associated publication.
