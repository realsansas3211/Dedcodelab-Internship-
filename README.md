DecodeLabs Data Analytics Internship Projects 1–4
Batch 2026 | Powered by DecodeLabs
Portfolio of the first three industrial training projects completed during the DecodeLabs Data Analytics Internship.

Project | Focus | Status |
Project 1
Data Cleaning & Preparation | Completed
Project 2
Exploratory Data Analysis (EDA) | Completed
Project 3
SQL Data Analysis | Completed |
Dataset Overview
Rows: 1,200 orders  
Columns: 14  
Time span: January 2023 – June 2025  
Unique customers: 1,189  
Key columns:
`OrderID`, `Date`, `CustomerID`, `Product`, `Quantity`, `UnitPrice`, `ShippingAddress`, `PaymentMethod`, `OrderStatus`, `TrackingNumber`, `ItemsInCart`, `CouponCode`, `ReferralSource`, `TotalPrice`

Data quality notes (from Project 1 & 2):
`CouponCode` contained 309 null/blank values (≈25.75%) replaced with 'No Coupon'.
TotalPrice = Quantity × UnitPrice holds for all rows
No duplicate `OrderID`s
All other fields complete

Project 1 – Data Cleaning & Preparation
Goal: Transform a raw, messy dataset into a reliable source of truth.
Key tasks performed:
Identified and handled missing / null values (primarily `CouponCode`)
Checked for and removed duplicates
Validated data types and formats (dates, numeric fields, categoricals)
Verified business rules (e.g. `TotalPrice = Quantity × UnitPrice`)
Produced a clean table ready for analysis (1,200 rows × 14 columns)

Project 2 – Exploratory Data Analysis (EDA)

Goal: Uncover patterns, distributions, trends, outliers, and business signals using statistical and visual methods.

Methodology:
Followed DecodeLabs Forensic EDA Framework + IPO model
Descriptive statistics, distribution shape (skewness/kurtosis), IQR & Z-score outlier detection
Correlation analysis, categorical breakdowns, time-series aggregation
Visualizations with matplotlib / seaborn

Key findings:
Total Revenue: $1,264,762  
Average Order Value: $1,053.97 (Median: $823.62) right-skewed distribution  
High cancellation + return rate: 41.4% of orders (Cancelled 20.8% + Returned 20.6%) ~$520k revenue at risk  
Top revenue products: Chair, Printer, Laptop
Instagram is the strongest referral channel
High-value orders (>$3,000) are almost exclusively 5-unit purchases of premium items; several of these were Cancelled or Returned  
Deliverable: `EDA_Project2_Report.pdf`

Project 3 – SQL Data Analysis
Goal: Extract actionable business insights using pure SQL.
Skills demonstrated:
SELECT,WHERE,GROUP BY,ORDER BY
Aggregations:COUNT,SUM,AVG,MIN,MAX
HAVING for post-aggregation filtering
Logical query execution order: `FROM → WHERE → GROUP BY → HAVING → SELECT → ORDER BY`
Sample insights from the 16 queries:
Overall: 1,200 orders, 1,189 unique customers, $1.26M revenue, AOV $1,053.97
Product ranking by revenue (Chair / Printer / Laptop lead)
Order status distribution highlighting the 41.4% cancellation + return problem
High-value order analysis (all top orders are 5-unit premium items)
Coupon, payment method, and referral source performance. 
