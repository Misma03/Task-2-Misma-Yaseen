# Project 2: Exploratory Data Analysis (EDA)

**Internship:** DecodeLabs – Data Analytics Industrial Training (Batch 2026)

##  Objective
Analyze the cleaned dataset to uncover patterns, trends, outliers, and relationships between variables — transforming a static table of numbers into meaningful, actionable insights.

##  Dataset
- **Input file:** `Dataset for Analytics CLEANED.xlsx` (output of Project 1)
- **Rows:** 1,200 orders
- **Columns:** 14

##  Tools & Technologies
- Python
- pandas, numpy
- matplotlib, seaborn

##  Steps Performed

1. **Loaded the cleaned dataset** and reviewed its shape and column data types.
2. **Generated descriptive statistics** (mean, median, std, min, max, quartiles) for `Quantity`, `UnitPrice`, `TotalPrice`, and `ItemsInCart`.
3. **Compared mean vs. median** for key numeric columns to check for skewness.
4. **Analyzed categorical distributions:**
   - Orders by Product
   - Orders by OrderStatus
   - Orders by PaymentMethod
5. **Analyzed monthly sales trends** by grouping `TotalPrice` by month.
6. **Identified top and bottom performing products** by total revenue.
7. **Detected outliers in `TotalPrice`** using the IQR method (Q1 - 1.5×IQR to Q3 + 1.5×IQR).
8. **Built a correlation matrix** for `Quantity`, `UnitPrice`, `TotalPrice`, and `ItemsInCart`, and visualized it as a heatmap.
9. **Visualized distributions** using a boxplot and histogram (with KDE) of `TotalPrice`.
10. **Summarized key observations** in a final EDA report.

##  Key Findings

| Metric | Value |
|---|---|
| Total orders | 1,200 |
| Mean TotalPrice | $1,053.97 |
| Median TotalPrice | $823.62 |
| Mean Quantity | 2.95 |
| Median Quantity | 3.00 |

**Top 3 Products by Revenue:**
1. Chair — $195,620.11
2. Printer — $195,612.61
3. Laptop — $192,126.56

**Order Status Distribution (Top 3):**
- Cancelled: 250 orders
- Returned: 247 orders
- Pending: 237 orders

**Outliers:**
- 8 outliers detected in `TotalPrice` (0.67% of the dataset) using the IQR method.

**Correlations:**
- TotalPrice vs Quantity: **0.62** (moderate positive correlation)
- TotalPrice vs UnitPrice: **0.72** (strong positive correlation)

##  Insight
`TotalPrice` is right-skewed (mean > median), meaning a small number of high-value orders pull the average upward. This is confirmed visually by the histogram and boxplot, and is a key reason why the median is a more robust "typical order value" metric than the mean for this dataset.

##  Deliverables
- EDA notebook with statistical summaries, outlier detection, correlation analysis, and visualizations.

##  Key Skill Demonstrated
Descriptive statistics, outlier detection (IQR method), correlation analysis, and data storytelling.
