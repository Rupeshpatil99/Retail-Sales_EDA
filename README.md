# Retail Sales EDA Project

## Project Overview
This project performs Exploratory Data Analysis (EDA) on a retail sales dataset using Python. The analysis covers data inspection, data cleaning, feature engineering, univariate analysis, bivariate analysis, correlation analysis, and outlier treatment.

## Dataset
The original dataset is stored in `retail.csv`.

- Rows: 3,060
- Columns: 17
- Main areas: orders, customers, products, quantity, pricing, discounts, delivery, payment methods, ratings, shipping, coupons, and returns.

## Tools & Libraries
- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn

## EDA Workflow

1. **Initial Data Inspection**
   - Shape and columns
   - Data types
   - Descriptive statistics
   - Missing-value inspection
   - Duplicate-value inspection

2. **Data Cleaning**
   - Removed duplicate records
   - Standardized gender values
   - Converted negative values in Quantity, DiscountPercent, and DeliveryDays to absolute values
   - Limited DiscountPercent to the 0–100 range
   - Treated unrealistic CustomerAge values as missing
   - Handled missing values using row deletion and imputation

3. **Feature Engineering**
   - Converted `OrderDate` to datetime
   - Created `Year`
   - Created `Monthname`
   - Created `Dayname`
   - Created `Quarter`
   - Created `sales`
   - Created `QuantityType`

4. **Visualization**
   - Count plots
   - Histograms
   - KDE distributions
   - Pie chart
   - Correlation heatmap
   - Pairplot
   - Boxplots
   - Categorical comparisons

5. **Outlier Treatment**
   - Identified numeric columns
   - Applied IQR-based clipping to reduce the effect of extreme values

## Key Analysis Observations
Based on the completed notebook:
- Gender values required standardization because multiple representations were present.
- Negative values were found in Quantity, DiscountPercent, and DeliveryDays and were cleaned.
- Discount percentages above 100 were capped at 100.
- Customer ages outside the selected valid range were treated as missing.
- Missing values were present in several customer, payment, rating, shipping, coupon, and return-related columns.
- Payment-method distribution was compared across years.
- Gender distribution was compared across cities and product categories.
- Numeric relationships were explored using a correlation heatmap and pairplot.

## Project Files

```text
Retail-EDA/
│
├── Retail_EDA.ipynb
├── retail.csv
├── cleaned_sales.csv
├── README.md
└── .gitignore
```

## How to Run

1. Clone the repository.
2. Open `Retail_EDA.ipynb` in Jupyter Notebook or JupyterLab.
3. Make sure `retail.csv` is in the same folder as the notebook.
4. Run the notebook cells from top to bottom.

## Author
Rupesh Patil
