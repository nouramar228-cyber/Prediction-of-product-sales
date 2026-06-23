<img width="3352" height="1638" alt="linear_regression_coefficients" src="https://github.com/user-attachments/assets/328d36ba-a826-43db-b77f-fe90338d3c74" /># Prediction-of-product-sales Using Machine Learning

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
<img width="1769" height="1361" alt="sales_plot" src="https://github.com/user-attachments/assets/e8c8dd53-0ae3-4d1f-995b-3acf777fa7c5" />


---

## Insight 2: Outlet Type Significantly Impacts Sales

Supermarket Type3 stores consistently produce the highest average sales compared to other outlet types.

![Outlet Type](images/outlet_type_sales.png)
<img width="2141" height="1682" alt="boxplot_outlet_sales" src="https://github.com/user-attachments/assets/d0d0b5bb-5396-48ce-afab-ab465f620069" />

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
<img width="3352" height="1638" alt="linear_regression_coefficients" src="https://github.com/user-attachments/assets/99e2a8c7-4aee-415b-9f62-3d62510b3389" />


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
<img width="2897" height="1638" alt="tuned_random_forest_feature_importance" src="https://github.com/user-attachments/assets/26a3a356-121c-4f9b-99f4-4b7e8f0248aa" />


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


