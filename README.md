# Week-11-Team-3
# 📊 ESG + Financial + GAF Stock Risk Classification

## Group 3

This project develops a machine learning framework for **stock risk classification** by combining:

- 🌱 ESG (Environmental, Social and Governance) metrics
- 💰 Financial indicators
- 🖼️ Gramian Angular Field (GAF) images generated from historical stock prices

The project compares multiple machine learning approaches, including traditional models, deep learning, transfer learning, and a hybrid model, to identify the most effective method for predicting stock risk levels.

---

# Project Objective

The objective of this project is to classify S&P 500 companies into three stock risk categories:

- **Low Risk**
- **Medium Risk**
- **High Risk**

Instead of relying only on financial data, the project combines:

- ESG ratings
- Financial ratios
- Historical stock price behaviour (converted into images)

to improve prediction performance.

---

# Dataset

Four datasets are used throughout the project.

| Dataset | Description |
|----------|-------------|
| **DS1** | S&P 500 ESG Risk Ratings |
| **DS2** | ESG Scores and Metrics |
| **DS3** | Financial Statement Data |
| **DS4** | Historical Stock Prices |

These datasets are merged using stock ticker symbols to create one complete dataset for modelling.

---

# Project Workflow

The notebook follows a complete end-to-end machine learning pipeline.

## 1. Install Required Packages

Installs all required Python libraries such as:

- Scikit-learn
- TensorFlow
- XGBoost
- SHAP
- Optuna
- PyTS
- Matplotlib
- Seaborn

---

## 2. Load Data

- Mount Google Drive
- Load all four datasets
- Verify dataset structure

---

## 3. Data Preparation

- Merge datasets
- Handle missing values
- Clean features
- Generate the final dataset

---

## 4. Risk Label Creation

Risk labels are created based on stock volatility and mapped into three classes:

- Low
- Medium
- High

These labels become the prediction target.

---

## 5. Exploratory Data Analysis (EDA)

The notebook performs exploratory analysis including:

- Risk class distribution
- ESG score distributions
- Financial feature visualization
- Correlation analysis

---

## 6. GAF Image Generation

Historical stock prices are converted into **Gramian Angular Summation Field (GASF)** images.

These images allow deep learning models to learn temporal stock price patterns using computer vision techniques.

---

## 7. Train/Test Split

The data is divided using a **stratified 70/15/15 split**:

- 70% Training
- 15% Validation
- 15% Testing

This maintains balanced class distributions.

---

## 8. Feature Engineering

The notebook creates tabular features from:

- ESG scores
- Financial variables
- Derived indicators

These features are used by traditional machine learning models.

---

## 9. Models Implemented

The project evaluates multiple models.

### CNN Baseline

A custom Convolutional Neural Network trained using GAF images.

---

### Random Forest

Traditional machine learning model trained using tabular ESG and financial features.

---

### Random Forest + Optuna

Hyperparameter tuning using Optuna to improve Random Forest performance.

---

### ResNet50 Transfer Learning

A pretrained ResNet50 model used for image classification and feature extraction.

---

### Hybrid Model

The final hybrid model combines:

- ResNet50 image embeddings
- Tabular ESG features
- Financial features
- XGBoost classifier

This is the primary model proposed in the project.

---

## 10. Model Evaluation

Models are evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion Matrix

Performance comparisons are generated automatically.

---

## 11. Explainable AI

The project includes **SHAP (SHapley Additive Explanations)** to explain model predictions.

SHAP is used to identify the most influential features contributing to stock risk classification.

---

## 12. KPI Dashboard

A final dashboard summarises:

- Model performance
- Experiment logs
- Evaluation metrics
- Reproducibility checks

---

## 13. Streamlit Web Application

The notebook automatically generates a Streamlit application (`app.py`) that allows users to:

- Select company information
- Predict stock risk
- View prediction probabilities
- Visualize model outputs

---

# Project Structure

```
.
├── GROUP_3_ESG_GAF_Stock_Risk_Classification.ipynb
├── app.py
├── datasets/
│   ├── SP 500 ESG Risk Ratings.csv
│   ├── sp500_esg_data.csv
│   ├── financial_data.csv
│   └── historical_prices.csv
├── outputs/
├── models/
├── figures/
└── README.md
```

*(Folder names may vary depending on your local project setup.)*

---

# Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- TensorFlow / Keras
- Scikit-learn
- XGBoost
- Optuna
- SHAP
- PyTS
- Streamlit

---

# Key Features

- End-to-end machine learning pipeline
- Multi-source data integration
- ESG + Financial feature engineering
- Gramian Angular Field image generation
- Traditional ML models
- Deep learning models
- Transfer learning
- Hybrid learning framework
- Hyperparameter optimisation
- Explainable AI using SHAP
- Interactive Streamlit application

---

# How to Run

1. Clone this repository.

```bash
git clone <repository-url>
```

2. Install the required packages.

```bash
pip install -r requirements.txt
```

*(or install the libraries listed in the notebook.)*

3. Place all required datasets inside the project directory.

4. Update the dataset path (if required).

5. Run the notebook from the first cell to the last cell.

6. To launch the web application:

```bash
streamlit run app.py
```

---

# Output

The project generates:

- Trained machine learning models
- GAF image datasets
- Performance metrics
- SHAP explainability plots
- Confusion matrices
- Experiment logs
- Streamlit application
- Final prediction outputs

---

# Authors

**Group 3**

ESG + Financial + GAF Stock Risk Classification Project

---

# License

This project is developed for academic purposes.

# label 
Sometimes the app might crash because of the public platform used to run it, please press ctrl+r for restarting the app
