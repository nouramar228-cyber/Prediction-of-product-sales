# Prediction-of-product-sales Using Machine Learning

# Project Overview

This project focuses on predicting retail product sales using machine learning techniques. The goal is to help retailers understand which product and outlet characteristics most strongly influence sales performance.

The project analyzes supermarket sales data and builds predictive models to forecast future sales. These insights can help businesses improve inventory management, pricing strategies, and store performance.

---

# Business Problem

Retail businesses need accurate sales predictions to:
- Improve inventory planning
- Optimize pricing strategies
- Increase revenue
- Understand factors affecting product sales

This project uses historical sales data to predict `Item_Outlet_Sales`.

---

# Dataset Information

The dataset includes:
- Product characteristics
- Store information
- Product visibility
- Product pricing
- Historical sales performance

Target Variable:
- `Item_Outlet_Sales`

---

# Data Insights

## Insight 1: Product Price Strongly Influences Sales

Higher-priced products generally achieve higher sales revenue. The visualization below shows a positive relationship between `Item_MRP` and `Item_Outlet_Sales`.

![MRP vs Sales](images/boxplot_mrp.png)

---

## Insight 2: Outlet Type Significantly Impacts Sales

Supermarket Type3 stores consistently produce the highest average sales compared to other outlet types.

![Outlet Type](images/outlet_type_sales.png)

---

# Machine Learning Models

Two machine learning models were developed:

- Linear Regression
- Random Forest Regressor

The Random Forest model achieved the best predictive performance.

---

# Model Performance

| Model | Train R² | Test R² | RMSE |
|---|---|---|---|
| Linear Regression | 0.56 | 0.57 | 1094 |
| Random Forest | 0.94 | 0.55 | 1136 |
| Tuned Random Forest | 0.67 | 0.60 | 1050 |

---

# Linear Regression Coefficients

![Linear Regression Coefficients](images/linear_regression_coefficients.png)

## Interpretation

The most impactful features in the Linear Regression model were:

1. `Item_MRP`
   - Products with higher prices tend to generate higher sales.

2. `Outlet_Type_Supermarket_Type3`
   - Supermarket Type3 outlets strongly increase sales performance.

3. `Item_Visibility`
   - Product visibility influences customer purchasing behavior.

---

# Random Forest Feature Importance

![Feature Importance](images/random_forest_feature_importance.png)

## Top Important Features

1. Item_MRP
2. Outlet_Type
3. Item_Visibility
4. Outlet_Establishment_Year
5. Item_Type

## Interpretation

The Random Forest model identified product price (`Item_MRP`) as the strongest predictor of sales. Outlet characteristics and product visibility also play major roles in determining sales performance.

---

# Final Recommendation

The Tuned Random Forest model is recommended because it achieved the best balance between prediction accuracy and generalization performance.

Business stakeholders should:
- Focus on pricing optimization strategies
- Improve product visibility and placement
- Expand high-performing supermarket outlet types
- Use predictive analytics to improve inventory planning

---

# Repository Structure

```bash
sales-prediction-retail-analytics/
│
├── data/
├── notebooks/
├── images/
├── README.md
└── requirements.txt
