# HYBRID GRAPH–MACHINE LEARNING FRAMEWORK  
## FOR ACCURATE AND INTERPRETABLE BAND GAP PREDICTION

This repository contains the official source code and computational framework for predicting the **electronic band gap of crystalline materials** using a hybrid approach that combines **graph-based structural embeddings** with **advanced machine learning regressors**.

The framework is designed for **high-precision band gap prediction**, scalability to large materials datasets, and extensibility for materials informatics research.

---

## 🚀 Overview

This work proposes a hybrid computational pipeline that integrates:

- **Graph Neural Networks (GNNs)** for structural representation learning  
- **Gradient Boosting Decision Trees (GBDTs)** and **FT-Transformers** for regression  
- **Stacking-based ensemble learning** for improved accuracy and robustness  

High-dimensional structural embeddings are extracted from crystal structures using **CGCNN**, **MEGNet**, and **SchNet**, and subsequently processed through an optimized ensemble of machine learning models.

The resulting framework is suitable for:
- Materials discovery
- Screening of crystalline compounds
- Data-driven materials science research

---

## 📁 Repository Structure

```text
.
├─ *.ipynb                 # Jupyter notebooks for individual model training
│                           # (CatBoost, XGBoost, LightGBM, MLP, FT-Transformer, etc.)
├─ cgcnn_emb_extracker.py  # Script for extracting structural embeddings from CIF files
├─ stack.ipynb             # Final stacking ensemble logic
├─ data/                   # Dataset directory (ignored by git)
├─ requirements.txt        # Python dependencies (Python 3.8)
├─ .gitignore
└─ README.md
```
## 📦 Installation & Environment

This project is tested with Python 3.8.
Using a virtual environment or Conda environment is strongly recommended.

Clone the Repository
```text
git clone https://github.com/YZE-Crystal/bandgap-prediction.git
cd bandgap-prediction
```

Install Dependencies
```text
pip install -r requirements.txt
```

## 📊 Data Availability

The dataset is not stored on GitHub. The framework is designed to be plug-and-play.
After logging in with your API key, running the data scripts will automatically download and extract the dataset into the `/data` directory.


## 🛠️ Usage Guide

The recommended execution order is as follows:

### 1. Data Download
- `data_fetcher.ipynb`
- `cif_download.ipynb`

### 2. Preprocessing
- Run `preproccesing.ipynb` to clean and prepare the dataset

### 3. Feature Extraction
- `cgcnn_emb_extracker.py`
- `megnet_emb_extracker.ipynb`
- `schnet_emb_extracker.ipynb`

### 4. Model Training
- `CatBoost.ipynb`
- `XGBoost.ipynb`
- `LightGBM.ipynb`
- `MLP.ipynb`
- `Ftt.ipynb`

### 5. Ensemble Learning
- Run `stack.ipynb` to generate the final hybrid predictions

---

## 🧠 Models and Methods

### Graph-Based Embedding Models
- CGCNN
- MEGNet
- SchNet

### Machine Learning Regressors
- Gradient Boosting Decision Trees (CatBoost, XGBoost, LightGBM)
- Multi-Layer Perceptron (MLP)
- FT-Transformer

### Ensemble Strategy
- Stacking ensemble combining all base learners

---

## 🎯 Objective

A hybrid computational framework for **high-precision band gap prediction in crystals**,  
integrating **Graph Neural Network (CGCNN, MEGNet, SchNet) embeddings** with  
**GBDT and FT-Transformer ensemble models**.

---

## 📜 License

License information will be added in a future update.

---

## 🤝 Contributions

This project is developed as a collaborative research effort under the **YZE-Crystal** organization.  
Contributions, issues, and suggestions are welcome.

