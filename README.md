# Uptrail-Week-2
Sales and customer behaviour analysis — data cleaning, feature engineering in Python and Q2 business insights for a fictional e-commerce business

**Project Overview**

Analysis of Q2 2025 sales and customer behaviour data for Uptrail, a fictional SaaS business. Three raw datasets were cleaned, merged into a master table and analysed to answer five business questions around revenue, discounting, customer loyalty and delivery performance.
**Headline figures**:

1,421 total orders | £116,962 total revenue | £82.31 average order value
Only 41.4% of orders delivered on time


**Files**

customer_info.csv — raw customer data including region, loyalty tier and signup date
sales_data.csv — raw transactional data including orders, delivery status and discounts
product_info.csv — raw product data including category, price and launch date
Week_2_Project.ipynb — full Python notebook covering cleaning, feature engineering and visualisation
Week_2_Report.docx — business insights report with findings and recommendations


**Cleaning & Preparation**

All three datasets contained quality issues addressed before analysis:

Inconsistent casing and misspellings across delivery_status, loyalty_tier, gender and payment_method — standardised using .str.strip(), .str.title() and .replace()
Missing region values filled with "Unknown" to preserve records
Missing customer IDs filled via interpolation based on sequential ID pattern
Negative unit_price values checked and validated
Duplicate emails and customer IDs investigated and resolved
Quantities recorded as words ("three", "five") converted to integers


**Feature Engineering**

Four new columns derived to support analysis:

revenue — unit price adjusted for discount applied
is_late — binary flag for delayed deliveries
price_band — Low / Medium / High grouping based on unit price
discount_pct — discount expressed as a percentage for cleaner visualisation


**Key Findings**

Cleaning products drove 42.5% of total revenue and were the top category across every region
Discounts showed no meaningful impact on order volume — correlation of -0.02 between discount and quantity, with a negative correlation between discount and revenue suggesting margin is being eroded for no return
Gold-tier customers account for 54% of orders but their average order value is only £2.47 higher than Bronze — frequency drives the gap, not basket size
Delivery performance is a business-wide issue — fewer than half of all orders arrived on time across all regions


**Recommendations**

Review the discounting strategy — it is not driving volume and is actively reducing revenue
Treat delivery performance as urgent — a 41.4% on-time rate is a significant operational risk
Focus retention efforts on Bronze customers — their spend per order is already close to Gold, making frequency the primary lever


**Tools Used**

Python (pandas, seaborn, matplotlib) — cleaning, feature engineering, visualisation
Excel — supplementary data sampling and sense-checking
Sonnet 4.6
