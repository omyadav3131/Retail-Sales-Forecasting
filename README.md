# 📊 Retail Sales Forecasting & Business Analytics

## 📌 Project Overview

This project is an end-to-end retail sales analytics and machine learning project focused on understanding sales patterns and predicting product outlet sales.

The project combines data preprocessing, exploratory analysis, regression modeling, model evaluation, and an interactive Power BI dashboard to generate data-driven business insights.

The objective is to demonstrate how data analytics and machine learning can support retail decision-making by identifying sales drivers and analyzing outlet and product performance.

---

## 🎯 Business Problem

Retail businesses need to understand product demand, outlet performance, and the factors influencing sales.

This project addresses the following questions:

- Which product categories generate the highest sales?
- Which outlet types contribute the most revenue?
- How does product price relate to sales performance?
- Do outlet characteristics influence product sales?
- Can machine learning models predict product outlet sales?

---

## ⚙️ Technology Stack

### Programming Language

- Python

### Data Analysis and Machine Learning

- Pandas
- NumPy
- Scikit-learn
- Matplotlib

### Business Intelligence

- Power BI

### Development Tools

- Jupyter Notebook
- Git
- GitHub

---

## 🔄 Project Workflow

1. Load and understand the retail sales dataset.
2. Clean and preprocess the data.
3. Handle missing values and categorical features.
4. Perform feature engineering.
5. Prepare features and the target variable.
6. Apply log transformation to the sales target.
7. Split the dataset into training and testing sets.
8. Train multiple regression models.
9. Evaluate models on the original sales scale.
10. Select the best-performing model.
11. Save the final trained model.
12. Analyze business trends using Power BI.

---

## 🤖 Machine Learning Models

Three regression models were trained and evaluated:

1. Linear Regression
2. Random Forest Regressor
3. Gradient Boosting Regressor

The dataset was divided into:

- 80% Training Data
- 20% Testing Data

The target variable `Item_Outlet_Sales` was log-transformed using `log1p` during model training.

For final evaluation, model predictions were converted back to the original sales scale using `expm1`.

---

## 📈 Model Performance

The models were evaluated using:

- RMSE — Root Mean Squared Error
- R² Score — Coefficient of Determination
- MAE — Mean Absolute Error

### Performance on Original Sales Scale

| Model | RMSE | R² Score | MAE |
|---|---:|---:|---:|
| Linear Regression | 1084.56 | 0.5672 | 744.81 |
| Random Forest | 1090.77 | 0.5623 | 744.81 |
| Gradient Boosting | 1095.14 | 0.5587 | 746.05 |

---

## 🏆 Final Model Selection

Linear Regression achieved the lowest RMSE and highest R² score among the evaluated models while maintaining a comparable MAE.

Based on the evaluation results, **Linear Regression was selected as the final model**.

This result also demonstrates that a more complex machine learning model does not always guarantee better predictive performance.

The final trained model is stored in:

`models/final_model.pkl`

---

## 📊 Power BI Dashboard

An interactive Power BI dashboard was developed to analyze retail sales performance and identify important business trends.

### Dashboard Visualizations

- Sales by Item Type
- Sales by Outlet Type
- Sales by City Tier
- Store Age vs Sales
- Price vs Sales Relationship

---

## 📷 Dashboard Preview

![Dashboard Preview](reports/Dashboard.png)

---

## 💡 Key Business Insights

- Fruits and Vegetables emerged as the highest-performing product category by total sales.
- Tier-3 outlet locations generated the highest overall revenue in the analyzed dataset.
- Supermarket Type 1 contributed the largest share of total sales.
- Product price showed a positive relationship with outlet sales.
- Outlet characteristics and store age influenced sales performance.

---

## 📂 Project Structure

```text
Retail-Sales-Forecasting/
│
├── data/
│   ├── raw/
│   │   └── train.csv
│   │
│   └── processed/
│       └── cleaned_data.csv
│
├── notebooks/
│   ├── 01_data_preprocessing.ipynb
│   └── 02_model_training.ipynb
│
├── models/
│   └── final_model.pkl
│
├── dashboard/
│   └── retail_sales_dashboard_data.csv
│
├── reports/
│   ├── Dashboard.pbix
│   ├── Dashboard.png
│   ├── Retail-Sales-Forecasting-and-Business-Analytics.pdf
│   └── Retail-Sales-Forecasting-and-Business-Analytics.pptx
│
└── README.md

```

---

## 📓 Notebooks

### 01 — Data Preprocessing

`notebooks/01_data_preprocessing.ipynb`

Includes:

- Dataset loading
- Missing value handling
- Data cleaning
- Feature preparation
- Processed dataset generation

### 02 — Model Training and Evaluation

`notebooks/02_model_training.ipynb`

Includes:

- Feature engineering
- Target transformation
- Train-test split
- Linear Regression
- Random Forest
- Gradient Boosting
- Original-scale model evaluation
- RMSE, R², and MAE comparison
- Final model selection
- Model persistence using Joblib

---

## 🚀 Future Improvements

Potential improvements include:

- Perform hyperparameter tuning using GridSearchCV or RandomizedSearchCV.
- Experiment with XGBoost and LightGBM.
- Add cross-validation for more robust model evaluation.
- Perform detailed residual analysis.
- Develop a Streamlit application for real-time sales prediction.
- Add time-series forecasting when time-based sales data is available.
- Deploy the prediction application to a cloud platform.

---

## 👨‍💻 Author

**Om Yadav**

MCA Student | Data Analytics & Java Development

Focused on Python, SQL, Power BI, Machine Learning, and Java Development.