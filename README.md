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
- **Python**: Core programming language for data processing.
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

## How to Run
1. **Install Dependencies:**
   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn
   ```
2. **Run the Script:**
   ```bash
   python superstore_analysis.py
   ```
   running the scripts work also on jupyter files
   
4. **Check the Output:**
   - Cleaned CSV files will be saved in the working directory.
   - SQLite database `superstore.db` will contain structured data.

## Future Enhancements
- Implement additional EDA visualizations.
- Enhance database normalization.
- Apply more advanced predictive models.


