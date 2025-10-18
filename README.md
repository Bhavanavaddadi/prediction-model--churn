# 📈 Customer Churn Prediction App

A complete end-to-end data science project that trains an XGBoost model to predict customer churn and deploys it as an interactive web app using Gradio.

## 💾 Dataset
This project uses the "Telco Customer Churn" dataset.

Source: Kaggle

Original Creator: IBM Sample Datasets

Description: The dataset contains 7043 customer records, each with 21 attributes. These attributes include:

Demographic Info: Gender, senior citizen status, partner, dependents.

Customer Account Info: Tenure, contract type, payment method, monthly charges, and total charges.

Services: Phone service, multiple lines, internet service, online security, tech support, etc.

Target Variable: The Churn column, which indicates whether the customer left the company.

## 🚀 App Preview

Here is a look at the final application in action. The user can input a customer's details on the left and instantly receive a prediction and probability on the right.
<img width="1889" height="903" alt="image" src="https://github.com/user-attachments/assets/a14f66e5-3ffc-4618-a890-543943b5678f" />
<img width="931" height="895" alt="image" src="https://github.com/user-attachments/assets/cfc23af1-e801-4d54-adc9-0b8b257902a4" />


## 🎯 Project Overview

The goal of this project was to leverage the Telco Customer Churn dataset to build a highly accurate machine learning model. The project covers the entire data science workflow:

1.  **Data Cleaning & Preprocessing:** Loaded the data, handled missing values, and corrected data types (e.g., `TotalCharges`).
2.  **Model Training:** Built a scikit-learn pipeline to preprocess data and train an XGBoost classifier.
3.  **Model Evaluation:** Assessed the model's performance using metrics like accuracy, precision, and recall.
4.  **Deployment:** Created a simple, user-friendly web app with Gradio to make the model usable by anyone.

## 📊 Model Performance

The final model performs well, with a strong ability to identify customers who are likely to churn. Here are the key metrics from the test set:

<img width="547" height="336" alt="image" src="https://github.com/user-attachments/assets/fdbf41f3-177d-40c9-8b40-dc46c3527030" />
<img width="649" height="549" alt="image" src="https://github.com/user-attachments/assets/ee29cc19-3ee9-4c1b-a412-5f2445ea1fee" />


## 📁 Repository Files
* **`ChurnPrediction.ipynb`**: The saved colab file.

# From this, we can gather several key insights:

Excellent at Identifying Loyal Customers (True Negatives): The model is very strong at its main task: correctly identifying customers who are not going to churn. It successfully found 897 loyal customers, which is its best-performing area.

The Biggest Challenge - Missed Opportunities (False Negatives): The model's primary weakness is that it missed 187 customers who did churn, incorrectly labeling them as "safe." From a business perspective, this is the most critical error, as it represents 187 lost opportunities for a retention campaign.

Decent Churn-Catching Ability (True Positives): The model successfully identified 187 customers who were going to churn. These are the people the business could save by targeting them with discounts or special offers.

The 50% Mark: An interesting finding is that the model caught exactly as many churning customers (187) as it missed (187). This means its "Recall" for churning customers is 50% — it's finding half of all the customers who are about to leave.

Wasted Effort (False Positives): The model incorrectly flagged 136 loyal customers as "likely to churn." This could lead to wasted marketing money, as the company would be giving discounts to people who weren't planning on leaving anyway.

In summary: The model is highly reliable at finding safe customers but is currently in a "coin-flip" (50/50) scenario for identifying at-risk customers. The next step to improve this project would be to focus on techniques (like oversampling, or tuning model parameters) to reduce the 187 "False Negatives" and catch more of the customers who are about to leave.

