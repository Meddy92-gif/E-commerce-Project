# Superstore Data Processing and Analysis

## Overview
This repository contains a Python script for processing, cleaning, and analyzing a sample superstore dataset. The script leverages popular data science libraries such as Pandas, NumPy, Matplotlib, and Scikit-learn to extract meaningful insights and store processed data in an SQLite database.

## Features
- **Data Loading**: Reads and preprocesses the `Sample-Superstore.csv` dataset.
- **Data Cleaning & Transformation**:
  - Renames columns for consistency.
  - Removes duplicate records.
  - Splits data into multiple CSV files for different entities (Orders, Customers, Products, and Sales).
- **SQLite Database Integration**:
  - Creates normalized tables (Customers, Products, Orders, and Salesinfo).
  - Establishes foreign key relationships.
  - Inserts cleaned data into SQLite tables.
- **Exploratory Data Analysis (EDA)**:
  - Identifies duplicate records.
  - Uses statistical analysis to find key trends.
  - Sets up basic visualization tools with Matplotlib and Seaborn.
- **Predictive Modeling**:
  - Implements Linear Regression and Polynomial Regression for trend analysis.

## Technologies Used
- **Python**: A core programming language for data processing.
- **Libraries**:
  - `numpy`: Numerical operations
  - `pandas`: Data manipulation and analysis
  - `matplotlib & seaborn`: Data visualization
  - `scipy`: Statistical functions
  - `scikit-learn`: Machine learning models
  - `sqlite3`: Database management

## Dataset
The dataset consists of transactional records from a superstore, containing attributes like:
- **Orders**: Order ID, Order Date, Ship Date, Ship Mode
- **Customers**: Customer ID, Name, Region, City, State
- **Products**: Product ID, Name, Category, Sub-Category
- **Sales Info**: Sales, Quantity, Discount, Profit
   
4. **Check the Output:**
   - Cleaned CSV files will be saved in the working directory.
   - SQLite database `superstore.db` will contain structured data.

## Future Enhancements
- Implement additional EDA visualizations.
- Enhance database normalization.
- Apply more advanced predictive models.

___________________________________________________________________________________________________________________________________________________________________________________________________________



# Customer Purchase Behavior Analysis

## Overview
This project analyzes customer purchase behavior using data from a retail dataset. It performs clustering and regression analysis on monetary, frequency, and recency metrics to gain insights into customer purchasing patterns.

## Dataset
The dataset used for this analysis is **Sample-Superstore.csv**, which contains transactional data including order details, sales, profit, and customer information.

## Features Used
- **Order Date & Ship Date**: Used to calculate recency and shipping behavior.
- **Sales & Profit**: Monetary values used to assess customer spending patterns.
- **Quantity & Discount**: Product purchase behavior indicators.
- **Customer ID**: Unique identifier for tracking repeat customers.
- **Region, Segment, Ship Mode**: Categorical variables impacting customer trends.

## Steps in Analysis

### 1. Data Preprocessing
- Read and clean the dataset.
- Convert `Order Date` to datetime format.
- Divide the dataset into subsets and determine the relations considering the main characteristics of a Primary Key and Foreign Key:

![image](https://github.com/user-attachments/assets/7eb9a484-02f2-457d-a89d-e6ee87921733)

- Aggregate data by `Customer ID` to compute the following:
  - **Repeat Purchase Count**
  - **Total Sales per Customer**
  - **Total Quantity Purchased**
  - **Average Discount Received**
  - **Total Profit per Customer**
  - **Recency (days since last purchase)**
  - **Most Frequent Ship Mode, Segment, and Region**

### 2. Regression Analysis
- **Linear Regression**: Predicts repeat purchase count based on sales, discount, profit, segment, and recency.
- **Model Evaluation**: Root Mean Squared Error (RMSE) is calculated to assess model accuracy.
- **Visualization**:
  - Actual vs. Predicted Repeat Purchase Count
  - Sales vs. Repeat Purchase Count with Regression Line

### 3. Sales Forecasting by Segment
- Extracts `Quarter` from `Order Date` to track sales trends.
- Aggregates `Sales` and `Profit Margin` by `Segment` and `Quarter`.
- Fits **Linear and Polynomial Regression** models to forecast future sales.
- **Plots Trends** for different customer segments.

### 4. Clustering Analysis (Monetary, Frequency, Recency)
- Creates three customer behavior metrics:
  - **Monetary**: Total amount spent per customer.
  - **Frequency**: Number of unique orders per customer.
  - **Recency**: Days since last order.
- **Detects Outliers** using box plots.
- **Removes Outliers** using the Interquartile Range (IQR) method.

## Key Findings
- Customers with higher sales tend to make repeat purchases more frequently.
- Discount impacts purchase frequency but may reduce profit margins.
- Different customer segments exhibit unique purchase behaviors over time.
- Clustering customers based on monetary, frequency, and recency provides actionable insights for targeted marketing.

## Technologies Used
- **Python** (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn)
- **Machine Learning Models**: Linear Regression, Polynomial Regression, Clustering

To view the generated plots and metrics, check the [following repositories](https://github.com/Meddy92-gif/E-commerce-Project/blob/master/EDA_Superstore.ipynb)
To analyze the ML-driven clustering,have a look at [here](https://github.com/Meddy92-gif/E-commerce-Project/blob/master/k-means-clustering.ipynb) 

---
After significant technical enhancements, I hope this project will provide a foundational approach to customer analytics using retail data, aiding in data-driven business decision-making.



