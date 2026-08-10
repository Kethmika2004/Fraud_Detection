# 🕵️‍♂️ OctWave 3.0 - Credit Card Fraud Detection

> *Somewhere in a sea of legitimate transactions, a handful of frauds are hiding. This is the hunt.*

A machine learning pipeline built for the **OctWave 3.0 Credit Card Fraud Detection Challenge**, tuned and evaluated on **F1-score** — because in fraud detection, missing the needle in the haystack is far more costly than a false alarm.

---

## ⚡ TL;DR

| | |
|---|---|
| **Model** | LightGBM (Gradient Boosted Trees) |
| **Tuning** | Optuna (Bayesian hyperparameter search) |
| **Metric** | F1-score |
| **OOF F1** | **~0.9959** |
| **Status** | ✅ Pipeline complete → 📤 Kaggle submission pending |

---

## 🎯 The Problem

Credit card fraud is a classic *needle-in-a-haystack* problem: fraudulent transactions are rare, patterns shift constantly, and the cost of a false negative (missed fraud) vastly outweighs the cost of a false positive (flagged legit transaction). This challenge is about building a model that can tell the difference — reliably, and at scale.

## 🛠️ The Approach

1. **EDA & preprocessing** - understanding class imbalance, feature distributions, and transaction patterns
2. **Feature engineering** - crafting signals that help separate fraud from noise
3. **Model: LightGBM** - chosen for speed, performance on tabular data, and native handling of imbalanced classes
4. **Hyperparameter tuning: Optuna** - automated search across the hyperparameter space to squeeze out every last bit of F1
5. **Validation** - out-of-fold (OOF) predictions to get an honest, leak-free estimate of performance

## 📊 Results

```
Out-of-Fold F1-Score: 0.9959
```

A high-precision, high-recall model built to catch fraud without crying wolf.

## 📁 Repo Structure

```
octwave_26/
├── OctWave_Fraud_Detection_LightGBM_Optuna.ipynb   # Main pipeline: EDA → FE → LightGBM → Optuna tuning
└── README.md
```

## 🚀 Running It

This notebook was developed in Google Colab. To reproduce:

1. Open the `.ipynb` in Colab or Jupyter
2. Install dependencies (`lightgbm`, `optuna`, `pandas`, `scikit-learn`)
3. Run all cells top to bottom
4. Final predictions are generated for Kaggle submission

## 🧩 What's Next

- [ ] Final Kaggle submission
- [ ] Threshold tuning for deployment-ready precision/recall trade-off
- [ ] Feature importance deep dive

---

*Built with 🔥 gradient boosting and a healthy dose of Optuna trials because good hyperparameters aren't found, they're earned.*
