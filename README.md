# Project Title: Predicting Customer Purchase Behavior Using a Decision Tree Classifier

## Problem Definition

In modern marketing, businesses strive to personalize outreach and reduce unnecessary costs. A critical challenge is predicting whether a potential customer will purchase a product based on their previous behavior and demographics.

This project aims to build a **Decision Tree Classifier** that predicts whether a customer will subscribe to a **term deposit** using features such as age, job type, education level, and past campaign outcomes.

---

## Dataset Overview

- **Source:** UCI Machine Learning Repository  
- **Dataset URL:** [Bank Marketing Dataset](https://archive.ics.uci.edu/dataset/222/bank+marketing)  
- **Input Features Include:**
  - Age, Job, Marital Status, Education
  - Loan, Housing, Default
  - Contact method, Day/Month of contact
  - Duration of last contact
  - Campaign-related features (e.g., number of contacts, previous outcomes)

- **Target Variable:** `y` — whether the customer subscribed to a term deposit ("yes" or "no")

---

## Project Objective

To build a machine learning model that predicts term deposit subscription based on:
- **Demographic data**
- **Marketing communication methods**
- **Past interaction history**

---

## Tools & Libraries Used

- **Python**
- **Pandas:** For loading and preprocessing the dataset  
- **NumPy:** For numerical operations  
- **Matplotlib & Seaborn:** For visualizing insights  
- **Scikit-learn:** For training and evaluating the Decision Tree model

---

## Steps Followed

### 1. Data Import & Exploration
- The dataset was loaded into a dataframe.
- Summary statistics were reviewed to understand feature distributions.
- Class imbalance and missing values were identified.
- The proportion of "yes" vs "no" in the target variable was examined.

### 2. Data Preprocessing
- Categorical columns (like job, marital status, education) were converted to numerical codes.
- The dataset was split into **features (X)** and **target (y)**.
- A **train-test split** was performed to separate training and testing data for model validation.

### 3. Model Building
- A **Decision Tree Classifier** was initialized using Scikit-learn.
- The model was trained on the training portion of the dataset.

### 4. Evaluation
- Predictions were made on the test set.
- Model performance was assessed using:
  - **Accuracy Score**
  - **Confusion Matrix**
  - **Classification Report** (which includes precision, recall, and F1-score)

### 5. Visualization
- The trained decision tree was visualized to understand decision paths and feature splits using a built-in plotting function.

---

## Output

- A trained model that classifies whether a customer is likely to purchase or not.
- Performance metrics to judge model quality.
- A visual decision tree to interpret model logic.

---

## Key Insights

### 1. Influential Features
- **Call Duration:** Longer contact calls correlate with higher chance of purchase.
- **Previous Campaign Outcome:** Positive past interactions lead to higher success in future.
- **Communication Channel and Timing:** Contacting via certain methods (e.g., mobile) and in specific months leads to better responses.

### 2. Customer Segmentation
- The tree structure naturally segments customers into:
  - High-conversion groups (long call durations + positive previous contact)
  - Low-probability groups (many failed attempts, short calls)

### 3. Cost Reduction Strategy
- Identifying uninterested customers early helps reduce marketing expenses.
- Resources can be focused on more promising leads.

### 4. Transparency and Interpretability
- Decision Trees are not black-box models — every decision path is visible.
- This increases **trust** among non-technical stakeholders.

### 5. Data Imbalance Consideration
- There are typically more "no" responses than "yes".
- Accuracy alone is misleading; precision, recall, and F1-score are used to evaluate effectiveness, especially for the minority "yes" class.

---

## Conclusion

This project successfully demonstrates how a Decision Tree Classifier can be applied to marketing data to:
- Predict customer behavior,
- Understand key influencing factors,
- Segment customer profiles, and
- Guide strategic decisions for future campaigns.

The model's interpretability makes it a valuable tool for both data scientists and business decision-makers.

