# ML_Internship_Assignment
# Predicting User Churn for an E-commerce Platform

## Objective
This project aims to predict user churn on an e-commerce platform using event data and provide actionable business insights. The key goals are:
- **Prediction:** Identify users most likely to churn (stop returning or purchasing).
- **Insights:** Understand the reasons behind churn and propose business strategies to retain users.

---

## Dataset
The dataset, `events.csv`, contains user activities such as:
- **Columns:**
  - `event_time`: Datetime of the event (e.g., 2020-12-01 09:00:00).
  - `event_type`: Type of event (`view`, `cart`, `purchase`).
  - `product_id`: Identifier of the product.
  - `category_id`: Identifier of the product’s category.
  - `category_code`: Human-readable category code (if available).
  - `brand`: Brand of the product.
  - `price`: Price of the product.
  - `user_id`: Identifier of the user.
  - `user_session`: Identifier of the user's session.

---

## Approach
1. **Exploratory Data Analysis (EDA):**
   - Analyzed user behavior patterns.
   - Explored event distributions, product/brand popularity, and user-level summaries.

![download (2)](https://github.com/user-attachments/assets/75d5e4cf-381f-4d41-8b85-5746378a015c)

  ![Screenshot 2025-01-08 135704](https://github.com/user-attachments/assets/b21a8ba9-8ad6-439e-8895-85dcb303956c)
     
   
![Screenshot 2025-01-08 135637](https://github.com/user-attachments/assets/2d7a5a95-c17e-4c24-a019-5b8815120f29)


2. **Defining Churn:**
   - Defined churn as users with no purchase activity in the last 30 days.
   - Justified the definition based on business reasoning and user activity patterns.

3. **Feature Engineering:**
   - Created features capturing user behavior, including:
     - RFM metrics (Recency, Frequency, Monetary).
     - Session-based metrics (session count, average duration, etc.).
     - Behavioral ratios (view-to-cart, cart-to-purchase, etc.).
     - Product and brand preferences.

4. **Predictive Modeling:**
   - Built and compared models (e.g., Logistic Regression, Random Forest, XGBoost).
   - Evaluated model performance using metrics such as Precision, Recall, F1 Score, and AUC.
   ![download (1)](https://github.com/user-attachments/assets/7141229d-1e98-40d9-b427-6e72b11ac520)

  
5. **Interpretation & Insights:**
   - Identified influential features using SHAP values and feature importance plots.
   - Connected insights to user retention strategies.
   
   ![SHAP Values](https://github.com/user-attachments/assets/4e646f06-700b-4c4b-b7b2-0d1269ad1dea)

   ![download (4)](https://github.com/user-attachments/assets/d1776703-3528-4fdf-a98a-eba520a7b250)

   ![download (5)](https://github.com/user-attachments/assets/9b68eb6c-4a06-45b4-b770-cb538614606d)

7. **Recommendations:**
   - Proposed targeted interventions, such as personalized offers, marketing campaigns, and product improvements.

---

## Results
- **Model Performance:**
  - Precision: '1.00'
  - Recall: `1.00`
  - F1 Score: `1.00`
  - AUC: `0.9999989099077742`

- **Key Insights:**
  - Users with a high view-to-cart ratio but low cart-to-purchase ratio are more likely to churn.
  - Certain product categories and brands have higher churn rates.
---
