# Heart Disease EDA Project

**Project:** Exploratory Data Analysis (EDA) on Heart Disease Dataset

**Short description:**
An in-depth exploratory data analysis project to uncover key factors influencing heart disease, understand correlations between medical indicators, and prepare the dataset for predictive modeling.

 

## Overview

This project performs comprehensive exploratory data analysis (EDA) on a heart disease dataset. The aim is to discover patterns, correlations, and feature relationships that help understand the likelihood of heart disease.

## Dataset

* **Source:** (Add dataset source or file, e.g., `heart.csv`)
* **Common columns:** `age`, `sex`, `cp` (chest pain type), `trestbps` (resting blood pressure), `chol` (cholesterol), `fbs` (fasting blood sugar), `restecg`, `thalach` (max heart rate), `exang` (exercise induced angina), `oldpeak`, `slope`, `ca`, `thal`, `target`.
* **Rows:** ~300+ samples (varies by dataset version)

## Objectives

* Understand feature distributions and detect missing values.
* Identify correlations among key cardiovascular features.
* Visualize trends and relationships between health parameters and heart disease presence.
* Prepare insights for predictive model building.

## Repository Structure

```
heart-disease-eda/
├─ data/
│  └─ heart.csv
├─ notebooks/
│  └─ Heart_EDA.ipynb
├─ src/
│  ├─ clean_data.py
│  ├─ visualize.py
│  └─ analyze.py
├─ outputs/
│  ├─ figures/
│  └─ summary.txt
├─ requirements.txt
└─ README.md
```

## Getting Started

1. Clone this repository:

```bash
git clone https://github.com/<your-username>/heart-disease-eda.git
cd heart-disease-eda
```

2. Create a virtual environment & install dependencies:

```bash
python -m venv venv
source venv/bin/activate   # or venv\Scripts\activate on Windows
pip install -r requirements.txt
```

3. Open the notebook:

```bash
jupyter notebook notebooks/Heart_EDA.ipynb
```

## EDA Steps / What I did

1. **Load Data** – imported CSV, checked shape, and feature types.
2. **Data Cleaning** – handled missing values, checked duplicates.
3. **Univariate Analysis** – plotted histograms and boxplots for numerical features.
4. **Bivariate Analysis** – analyzed relationships between variables using scatter, heatmaps, and pairplots.
5. **Target Analysis** – compared health indicators across `target` values (0 = No disease, 1 = Disease).
6. **Correlation Analysis** – visualized feature correlations via heatmap.
7. **Feature Insights** – identified top predictors of heart disease (e.g., `thalach`, `cp`, `oldpeak`, `exang`).
8. **Outlier Detection** – used IQR and boxplots to spot outliers.
9. **Feature Engineering** – created age groups, risk levels, and normalized features.

## Key Findings (example)

* **Chest pain type** (`cp`) and **maximum heart rate** (`thalach`) have a strong influence on heart disease.
* **Oldpeak** and **exercise-induced angina** (`exang`) show a strong negative correlation with heart health.
* **Age** and **sex** influence risk, with males showing higher occurrence rates.
* Certain ECG readings (`restecg`) correlate with `target` presence.

> Replace these with insights from your actual dataset.

## How to reproduce

Simply run:

```bash
jupyter notebook notebooks/Heart_EDA.ipynb
```

Or run a script version (if available):

```bash
python src/run_eda.py --input data/heart.csv --output outputs/figures/
```

## Notebooks & scripts

* `Heart_EDA.ipynb` — main exploratory notebook.
* `visualize.py` — reusable plotting functions.
* `clean_data.py` — data cleaning utilities.

## Visualizations (recommended)

* Distribution plots of `age`, `chol`, `thalach`, `trestbps`.
* Boxplots of `target` vs `chol`, `oldpeak`, and `thalach`.
* Correlation heatmap.
* Pairplots grouped by `target`.

## Requirements

Example `requirements.txt`:

```
pandas
numpy
matplotlib
seaborn
jupyter
scikit-learn
plotly  # optional
```

## Future Work

* Apply ML models like Logistic Regression, Decision Tree, Random Forest.
* Build an interactive dashboard (e.g., Streamlit or Dash).
* Use feature importance visualization.
 
