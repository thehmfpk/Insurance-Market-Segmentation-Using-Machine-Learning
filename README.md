# Insurance Market Segmentation using Unsupervised Machine Learning

## Project Title
**Insurance Customer Clustering & Market Segmentation**

## Description
This project focuses on performing customer segmentation for an insurance company to define a marketing strategy. Using a dataset of approximately 9,000 active credit card holders, the model identifies distinct groups based on customer behavior—such as spending habits, payment frequency, and credit usage. By utilizing **K-Means Clustering** and **Principal Component Analysis (PCA)**, the project transforms raw financial data into actionable business insights.

---

## Table of Contents
* [Dataset](#dataset)
* [Technical Stack](#technical-stack)
* [Project Workflow](#project-workflow)
* [Implementation Details](#implementation-details)
* [Results & Visualizations](#results)

---

## Dataset
The dataset `Customer Data.csv` contains 18 behavioral variables for each customer. 

**Key variables include:**
- `BALANCE`: Balance amount left in the account to make purchases.
- `PURCHASES`: Total amount of purchases made from the account.
- `CASH_ADVANCE`: Cash in advance given by the user.
- `CREDIT_LIMIT`: Limit of credit card for the user.
- `PAYMENTS`: Amount of payment done by user.
- `MINIMUM_PAYMENTS`: Minimum amount of payments made by user.
- `PRC_FULL_PAYMENT`: Percent of full payment paid by user.
- `TENURE`: Term of credit card service for user.

---

## Technical Stack
- **Language:** Python 3.x
- **Libraries:** - `Pandas` & `NumPy`: Data manipulation and cleaning.
  - `Matplotlib` & `Seaborn`: Statistical data visualization.
  - `Scikit-Learn`: 
    - `StandardScaler`: Feature scaling.
    - `PCA`: Dimensionality reduction.
    - `KMeans`: Unsupervised clustering algorithm.

---

## Project Workflow
1. **Data Exploration (EDA):** Identifying missing values and understanding the distribution of features.
2. **Data Cleaning:** Handling null values in `MINIMUM_PAYMENTS` and `CREDIT_LIMIT`.
3. **Feature Scaling:** Applying `StandardScaler` to ensure all features have a mean of 0 and a standard deviation of 1, as K-Means is distance-based.
4. **Dimensionality Reduction (PCA):** Reducing the feature set into principal components to capture the maximum variance and simplify the model.
5. **Hyperparameter Tuning:** Using the **Elbow Method** to find the optimal number of clusters ($K$).
6. **Clustering:** Training the K-Means model and assigning cluster labels to the original data.

---

## Implementation Details
The project is organized in the Jupyter Notebook `Market_Segmentation_in_Insurance_ML.ipynb`:
- **Preprocessing:** Removing the `CUST_ID` column as it is not needed for training.
- **Optimization:** We calculated the **Within-Cluster Sum of Squares (WCSS)** for multiple cluster counts to determine where the "elbow" occurs.
- **PCA Transformation:** The data is compressed into a 2D/3D space for easier visualization of the segment boundaries.

---

## Results
The segmentation revealed distinct groups of customers:
- **Cluster 0 (Example):** High-spending customers with high credit limits.
- **Cluster 1 (Example):** Customers who prefer cash advances and maintain low purchase activity.
- **Cluster 2 (Example):** Cautious spenders who pay their balances in full.

These segments allow the insurance company to target specific groups with custom products, such as credit protection insurance for high-balance users or reward programs for frequent spenders.

---

## Author: Hafiz Muhammad Faizan
## Project Status: Completed
