# QSAR Solubility Prediction

A machine learning model that predicts aqueous solubility of molecules 
from their chemical structure (SMILES), using RDKit descriptors and 
Random Forest regression.

## Problem
Solubility is a critical property in drug discovery — poorly soluble 
compounds often fail in development. This project predicts solubility 
directly from molecular structure.

## Dataset
ESOL (Delaney) dataset — 1144 molecules with experimentally measured 
aqueous solubility values.

## Method
1. Loaded SMILES strings and calculated 6 RDKit molecular descriptors:
   MolWt, LogP, NumHDonors, NumHAcceptors, NumRotatableBonds, TPSA
2. Trained a Random Forest Regressor (100 estimators)
3. Evaluated using train-test split and 5-fold cross-validation

## Results
- R² Score (test set): 0.901
- R² Score (5-fold CV): 0.913
- Most important feature: **LogP** (81.3% importance) — confirming 
  that lipophilicity is the dominant factor in aqueous solubility

## Tools
Python, RDKit, Pandas, Scikit-learn, Matplotlib

## How to run
Open `notebook.ipynb` in Google Colab and run all cells.
