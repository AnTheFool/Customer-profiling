# MANA Customer Segmentation and Analysis

## Overview
This project is part of the **DAZONE 2024 Data Analysis Competition** hosted by **Viettel Business Solutions Corporation**. The goal of the project is to perform an in-depth **customer segmentation analysis** to help businesses better understand their customers, improve product offerings, and tailor marketing strategies.

## Project Objectives
- **Data Cleaning & Preprocessing**: Handle missing values, remove duplicates, and transform data into a structured format.
- **Exploratory Data Analysis (EDA)**: Identify key demographic trends and spending behaviors.
- **Feature Engineering**: Create new variables to enhance clustering performance.
- **Customer Segmentation**: Apply **K-Means Clustering** to classify customers into distinct groups.
- **Data-Driven Insights & Recommendations**: Provide actionable suggestions based on customer profiles.

## Data Processing Steps
### 1. Data Cleaning
- Removed duplicate **CustomerIDs**, reducing dataset size from 3,069 to 2,240 unique records.
- Imputed missing values using the **K-Nearest Neighbors (KNN)** algorithm.
- Combined similar columns, such as merging **Phone** and **Phone_Number**.
- Standardized date-related features, extracting **Year_Register** and **Month_Register** from **Registration_Time**.
- Addressed outliers, particularly in **Income**, where extreme values were removed.
- Converted relevant variables from **float to integer** for efficiency.

### 2. Exploratory Data Analysis (EDA)
- **Age Distribution**: Most customers are between **32-41 years old**.
- **Income Analysis**:
  - Customers with **higher education levels** earn and spend more.
  - Non-parents spend **significantly more** than parents (170% higher spending gap).
- **Product Preferences**:
  - **Alcohol and seafood** have the highest correlation with income.
  - **Non-parents** show higher spending in all categories.

### 3. Feature Engineering
- Created new variables:
  - **Customer Age** from birth year.
  - **Parental Status** based on number of children.
  - **Total Spend Ratio**: Spending relative to income.
- Encoded categorical variables (e.g., **Marital Status, Education Level, Gender**).
- Standardized numerical features using **StandardScaler**.

### 4. Customer Segmentation (K-Means Clustering)
- Applied **Principal Component Analysis (PCA)** for dimensionality reduction.
- Used **Elbow Method and Silhouette Score** to determine optimal cluster count (**K=4**).
- Identified customer personas based on cluster characteristics.

## Key Findings & Recommendations
- **High-income, high-spending customers**: Target premium products (e.g., luxury alcohol & seafood).
- **Non-parents spend more**: Tailor promotions to encourage repeat purchases.
- **Low-income customers**: Offer budget-friendly product bundles to increase engagement.
- **Education impacts spending**: Premium campaigns should focus on customers with **higher degrees**.

## Technologies Used
- **Python (Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn)**
- **Jupyter Notebook**
- **Machine Learning Algorithms**: PCA, K-Means Clustering

