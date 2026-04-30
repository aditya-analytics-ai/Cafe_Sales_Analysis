# Cafe Sales Analysis 
– End-to-End Data Analysis Project
A complete data analysis project on a cafe's sales data — covering data cleaning, exploratory analysis, visualizations, and a business dashboard.

# Project Structure
├── Sales.csv                    # Raw (dirty) sales data
├── Sales_Cleaned.csv            # Cleaned data (output of Cleaning.ipynb)
├── Cleaning.ipynb               # Data cleaning notebook
└── Cafe_Sales_Analysis.ipynb    # Analysis & visualization notebook

# Project Overview
This project analyzes transactional sales data from a cafe to uncover business insights around:

Which items generate the most revenue
Which payment methods customers prefer
Which locations perform best
Monthly sales trends and growth rates
Customer segmentation by spending value


# Part 1 – Data Cleaning (Cleaning.ipynb)
The raw Sales.csv dataset contained various quality issues. The following steps were applied to fix them:
StepWhat was doneDirty text removalReplaced "ERROR", "UNKNOWN", "" with NaNPrice imputationFilled missing Price Per Unit using an item-to-price lookup mapItem recoveryRecovered "Unknown" items by reverse-mapping from priceNumeric conversionConverted Quantity, Price Per Unit, Total Spent to numericQuantity imputationDerived missing quantity from Total Spent / Price Per UnitTotal Spent recalculationRecalculated Total Spent = Quantity × Price Per Unit for consistencyCategorical cleanupFilled unknown Payment Method → UPI Payment, unknown Location → Online / UnspecifiedDate parsingConverted Transaction Date to datetime and dropped unparseable rowsFeature engineeringExtracted Year, Month, Month Name, Year_Month columnsDuplicate & validity checksRemoved duplicates and rows with invalid/negative quantities
Output: Sales_Cleaned.csv — a clean, analysis-ready dataset.

# Part 2 – Sales Analysis (Cafe_Sales_Analysis.ipynb)
Key Metrics Computed

Total Sales Revenue
Average Transaction Value
Total Quantity Sold

Item-Level Analysis

Top 10 items by revenue
Top 10 items by quantity sold
Revenue contribution % per item
Pareto Analysis (80–20 Rule)

Payment Method Analysis

Revenue by payment method
Transaction count by payment method
Average bill value per payment method

Location Analysis

Total revenue and quantity by location
Average bill value by location
Location Performance Matrix (Revenue vs Transactions vs Avg Bill Value)

Time-Series Analysis

Monthly sales trend
Monthly growth rate (%)
Year-on-Year comparison
Seasonality / monthly revenue contribution %

Advanced Analysis

Price sensitivity (Price vs Quantity scatter with regression)
Outlier detection using IQR method
Customer segmentation (Low / Medium / High Value)
High-value customer revenue contribution


# Dashboard
A single-page Manager-View Dashboard was built using Matplotlib & Seaborn, showing:

KPI Cards (Total Sales, Avg Transaction, Total Quantity, Top Item)
Monthly Sales Trend
Monthly Growth Rate
Top 10 Items by Revenue
Revenue by Customer Segment


# Key Business Insights

✅ Revenue is quantity-driven — higher volume = higher revenue
✅ Few items dominate overall sales (Pareto principle applies)
✅ Digital payments (UPI, Card) are associated with higher spending
✅ Seasonal demand significantly impacts monthly sales
✅ High-value transactions contribute a major share of total revenue
✅ Location performance varies by footfall and average bill value

# Author
Adityamohan Singh

GitHub: @your-username
LinkedIn: your-linkedin
