# ☕ Dirty Cafe Sales Data Analysis

A Python-based exploratory data analysis project focused on cleaning, transforming, and visualizing cafe transaction data using **Pandas, NumPy, Seaborn, and Matplotlib**.

## 📌 Project Overview

This project analyzes a cafe sales dataset containing **10,000 transaction records and 8 original columns**. The dataset includes information about transaction IDs, items, quantities, unit prices, total spending, payment methods, locations, and transaction dates.

The project focuses on:

- Understanding the structure and quality of the dataset
- Identifying missing and invalid values
- Cleaning categorical and numerical data
- Converting and extracting date-related information
- Standardizing inconsistent values
- Performing exploratory data analysis
- Creating visualizations to understand spending and transaction patterns

## 🎯 Objectives

- Perform initial data inspection and statistical analysis
- Identify missing values and inconsistent entries
- Clean invalid values such as `ERROR` and `UNKNOWN`
- Convert numerical columns into appropriate data types
- Extract day, month, and year from transaction dates
- Analyze item, payment method, and venue distributions
- Explore relationships between total spending, price, venue, and transaction dates

## 🛠️ Technologies & Libraries

- **Python**
- **Pandas** – data manipulation and analysis
- **NumPy** – numerical operations and conditional data transformation
- **Seaborn** – statistical data visualization
- **Matplotlib** – plotting and visualization
- **Statistics** – statistical operations

## 📂 Dataset

The dataset used in this project is:

`dirty_cafe_sales.csv`

### Original Columns

| Column | Description |
|---|---|
| Transaction ID | Unique identifier for each transaction |
| Item | Cafe item purchased |
| Quantity | Quantity purchased |
| Price Per Unit | Price of one unit |
| Total Spent | Total amount spent |
| Payment Method | Method used for payment |
| Location | Transaction location |
| Transaction Date | Date of the transaction |

The notebook later renames:
- `Item` → `Smoothie`
- `Location` → `Venue`

## 🧹 Data Cleaning & Preprocessing

The notebook performs several data preparation steps:

1. **Initial inspection**
   - Used `head()`, `tail()`, `shape`, `info()`, and `describe()`.
   - The initial dataset contains **10,000 rows and 8 columns**.

2. **Column renaming**
   - `Item` was renamed to `Smoothie`.
   - `Location` was renamed to `Venue`.

3. **Missing-value analysis**
   - Missing values were checked using `isnull().sum()`.
   - Missing categorical values were handled using the mode.

4. **Numerical conversion**
   - `Quantity`, `Price Per Unit`, and `Total Spent` were converted to numeric values.
   - Invalid numeric values were converted and handled as zero.

5. **Invalid date handling**
   - `UNKNOWN` and `ERROR` values in `Transaction Date` were replaced with missing values.
   - The transaction date was converted into a datetime format.
   - Day, month, and year were extracted into separate columns.

6. **Transaction ID cleaning**
   - The `TXN_` prefix was removed from transaction IDs.
   - Transaction IDs were converted to integers.

7. **Categorical value standardization**
   - `UNKNOWN` Smoothie values were mapped to `Tea`.
   - `ERROR` Smoothie values were mapped to `Coffee`.
   - `ERROR` values in Payment Method and Venue were standardized to `UNKNOWN`.

## 📊 Exploratory Data Analysis

The project examines:

- Item/Smoothie frequency
- Payment method distribution
- Venue distribution
- Transaction year distribution
- Numerical skewness
- Total spending distribution
- Transaction month and day patterns
- Relationship between total spending and price per unit
- Spending across different venues

## 📈 Visualizations

The notebook includes several visualizations using Seaborn and Matplotlib:

- KDE plot for transaction month
- Scatter plot of **Total Spent vs Price Per Unit**, grouped by Venue
- Count plot of transactions by month
- Bar plot of **Total Spent vs Smoothie**
- KDE plot for transaction day
- Line plot of **Total Spent vs Transaction Day**
- Histogram of Total Spent
- Bar chart of **Venue vs Total Spend**

## 💡 Key Findings

Based on the analysis performed in the notebook:

- **Juice** has the highest transaction frequency among the original item categories, with **1,504 records**.
- After standardizing invalid item values, **Coffee** and **Tea** become more frequent categories.
- **Digital Wallet** is the most frequent payment method, with **4,870 transactions** in the analyzed data.
- **Takeaway** is the most frequent venue, with **6,287 transactions**.
- The numerical analysis shows a strong positive relationship between `Total Spent` and the transaction's spending-related values, with `Total Spent` having a skewness of approximately **0.817**.
- All transactions in the dataset belong to the year **2023**.

## 📁 Project Structure

```text
dirty-cafe-data-analysis/
│
├── Cafe_roject.ipynb
├── dirty_cafe_sales.csv
└── README.md
```

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone <your-repository-url>
```

### 2. Open the project

Open the project folder in **Jupyter Notebook** or **VS Code**.

### 3. Install required libraries

```bash
pip install pandas numpy seaborn matplotlib
```

### 4. Run the notebook

Open:

```text
Cafe_roject.ipynb
```

Run the cells from top to bottom to reproduce the data cleaning, analysis, and visualizations.

## 👩‍💻 Skills Demonstrated

- Python for Data Analysis
- Pandas DataFrame Operations
- Data Cleaning
- Missing-Value Handling
- Data Type Conversion
- Date-Time Processing
- Categorical Data Transformation
- Exploratory Data Analysis (EDA)
- Statistical Analysis
- Data Visualization
- Seaborn & Matplotlib

## 📌 Conclusion

This project demonstrates an end-to-end workflow for working with a messy cafe sales dataset — from initial inspection and data cleaning to exploratory analysis and visualization. It highlights practical Python and Pandas skills for preparing real-world transactional data and extracting useful patterns from it.
