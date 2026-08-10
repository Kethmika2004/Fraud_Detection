# 🕵️‍♂️ OctWave 3.0 - Credit Card Fraud Detection

> *Somewhere in a sea of legitimate transactions, a handful of frauds are hiding. This is the hunt.*

<img width="1537" height="1023" alt="ChatGPT Image Aug 11, 2026, 01_19_02 AM" src="https://github.com/user-attachments/assets/299c9659-4ddd-402b-ad92-05a80444f3bc" />

A machine learning pipeline built for the **OctWave 3.0 Credit Card Fraud Detection Challenge**, tuned and evaluated on **F1-score** because in fraud detection, missing the needle in the haystack is far more costly than a false alarm.

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
 
A high precision, high recall model built to catch fraud without crying wolf.
 
<img width="1615" height="612" alt="Screenshot 2026-08-10 234359" src="https://github.com/user-attachments/assets/671de311-c229-4414-a083-e1795aec99bb" />

*Left: the precision recall curve stays near perfect across almost the entire recall range before collapsing sharply at the extreme tail. Right: F1-score peaks at a decision threshold of **0.660**, which is what the model uses to separate fraud from legitimate transactions.*

## 📁 Repo Structure

```
octwave_26/
├── OctWave_Fraud_Detection_LightGBM_Optuna.ipynb   # Main pipeline: EDA → FE → LightGBM → Optuna tuning
├── OctWave_Fraud_Detection_LightGBM_Optuna.py      # Main pipeline: EDA → FE → LightGBM → Optuna tuning
├── Fraud_Detection.ipynb                           # Basic one
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
