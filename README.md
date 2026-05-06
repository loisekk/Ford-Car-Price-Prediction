<div align="center">

# 🚗 Ford Car Price Analysis & Prediction

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-Visualization-3F4F75?style=for-the-badge&logo=plotly&logoColor=white)
![Kaggle](https://img.shields.io/badge/Kaggle-Dataset-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)

**End-to-end exploratory data analysis and linear regression modelling on a real-world Ford used-car dataset — comparing One-Hot and Label Encoding strategies for price prediction.**

</div>

---

## 📌 Project Overview

This project performs a complete data science pipeline on the [Ford Car Price Prediction](https://www.kaggle.com/datasets/adhurimquku/ford-car-price-prediction) dataset from Kaggle. Starting from raw CSV data, the notebook covers structured EDA, feature engineering, categorical encoding (One-Hot vs Label), feature scaling, and regression modelling — culminating in a performance comparison between two encoding approaches using R² and Adjusted R².

---

## ✨ Features

- **Exploratory Data Analysis (EDA)** — distribution plots, correlation heatmaps, and multi-dimensional scatter plots (including 3D price/mileage/year)
- **Categorical Encoding Comparison** — side-by-side implementation of One-Hot Encoding (`pd.get_dummies`) and Label Encoding (`sklearn.LabelEncoder`) on model, transmission, and fuel type
- **Feature Scaling** — StandardScaler applied to all numeric columns (year, mileage, tax, mpg, engineSize) to normalise feature magnitudes
- **Linear Regression Modelling** — trained and evaluated separately for both encoding strategies
- **Performance Metrics** — R² Score and Adjusted R² Score computed and compared across both models
- **Rich Visualisations** — Seaborn boxplots, scatterplots, histograms, and interactive Plotly charts with dark themes

---

## 🗂️ Project Structure

```
ford-dataset-analysis/
│
├── ford-dataset-analysis.ipynb   # Main notebook
├── README.md                     # Project documentation
└── assets/                       # (Optional) saved plot images
```

---

## 📊 Dataset

| Attribute     | Details                                              |
|---------------|------------------------------------------------------|
| **Source**    | Kaggle — `adhurimquku/ford-car-price-prediction`     |
| **File**      | `ford.csv`                                           |
| **Features**  | model, year, transmission, mileage, fuelType, tax, mpg, engineSize |
| **Target**    | `price` (GBP)                                        |

---

## 🔬 Analysis Pipeline

```
Raw Data
   │
   ├── 1. Data Inspection       →  .shape, .describe(), .info(), null checks
   │
   ├── 2. EDA                   →  Price distribution, correlation heatmap,
   │                                box plots by year/engine/fuel/transmission,
   │                                3D scatter (mileage × year × price)
   │
   ├── 3. Feature Engineering   →  price_bins (pd.cut), X/y split
   │
   ├── 4a. One-Hot Encoding     →  pd.get_dummies → StandardScaler → Linear Regression
   │
   ├── 4b. Label Encoding       →  LabelEncoder → StandardScaler → Linear Regression
   │
   └── 5. Evaluation            →  R² Score, Adjusted R² Score (both models)
```

---

## 🛠️ Tech Stack

| Library         | Purpose                              |
|-----------------|--------------------------------------|
| `pandas`        | Data loading, manipulation, encoding |
| `numpy`         | Numerical operations                 |
| `seaborn`       | Statistical visualisations           |
| `matplotlib`    | Plot rendering                       |
| `plotly`        | Interactive dark-theme charts        |
| `scikit-learn`  | Encoding, scaling, regression, metrics |

---

## 🚀 Getting Started

### Prerequisites

```bash
pip install pandas numpy seaborn matplotlib plotly scikit-learn
```

### Run Locally

```bash
git clone https://github.com/<your-username>/ford-dataset-analysis.git
cd ford-dataset-analysis
jupyter notebook ford-dataset-analysis.ipynb
```

> **Note:** Download `ford.csv` from [Kaggle](https://www.kaggle.com/datasets/adhurimquku/ford-car-price-prediction) and update the file path in the notebook's data-loading cell.

---

## 📈 Results

| Encoding Strategy | R² Score | Adjusted R² |
|-------------------|----------|-------------|
| One-Hot Encoding  | —        | —           |
| Label Encoding    | —        | —           |

> *Fill in your actual metric values after running the notebook.*

---

## 💡 Key Learnings

- One-Hot Encoding creates more columns but avoids imposing an artificial ordinal relationship on categorical variables like car model and fuel type.
- Label Encoding is more memory-efficient but can mislead distance-based algorithms by implying an order where none exists.
- StandardScaler is essential before linear regression when features have vastly different ranges (e.g., mileage in thousands vs engine size in single digits).
- Adjusted R² penalises unnecessary features and gives a more honest measure of model fit than plain R².

---

## 👤 Author

**Yash Brahmankar**
B.Tech AI & ML | OIST (2024–2028)

[![GitHub](https://img.shields.io/badge/GitHub-loisekk-181717?style=flat&logo=github)](https://github.com/loisekk)
[![Email](https://img.shields.io/badge/Email-yashbrahmankar95@gmail.com-D14836?style=flat&logo=gmail&logoColor=white)](mailto:yashbrahmankar95@gmail.com)

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
