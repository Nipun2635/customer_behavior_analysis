🛍️ Customer Shopping Behavior Analysis

📘 Overview
This project focuses on analyzing "customer shopping behavior" using transactional data from "3,900 purchases" across multiple product categories.
The goal is to uncover patterns in "spending habits, product preferences, and subscription trends" to provide data-driven business insights and strategic recommendations.

🧾 Dataset Summary
* Total Rows: 3,900
* Columns: 18

Key Features
* Customer Demographics: Age, Gender, Location, Subscription Status
* Purchase Details: Item Purchased, Category, Purchase Amount, Season, Size, Color
* Shopping Behavior: Discount Applied, Promo Code Used, Previous Purchases, Frequency, Review Rating, Shipping Type

Missing Data
* 37 missing values in the "Review Rating" column, imputed using "median ratings per category".

🧰 Tools & Technologies
| Tool / Technology                               | Purpose                              |
| Python (Pandas, NumPy, Matplotlib, Seaborn)     | Data loading, cleaning, and EDA      |
| PostgreSQL                                      | SQL-based business analysis          |
| Power BI                                        | Visualization and dashboard creation |
| Jupyter Notebook                                | Development and documentation        |

⚙️ Project Workflow
1. Data Loading & Preparation (Python)
* Imported dataset using `pandas`.
* Inspected data with `.info()` and `.describe()`.
* Renamed columns to "snake_case" for consistency.
* Imputed missing values in `review_rating` with median by product category.
* Created new derived features:
  * `age_group` – Binned age values into ranges.
  * `purchase_frequency_days` – Time-based purchase frequency metric.
* Checked redundancy between `discount_applied` and `promo_code_used` (dropped promo code).
* Loaded the cleaned dataset into "PostgreSQL" for SQL analysis.

2. Data Analysis (PostgreSQL SQL Queries)
Performed structured business analysis to extract actionable insights:
| Business Question               | SQL Objective                                             |
| Revenue by Gender               | Compare total revenue by male vs. female customers        |
| High-Spending Discount Users    | Find customers using discounts but spending above average |
| Top 5 Products by Rating        | Identify highest-rated products                           |
| Shipping Type Comparison        | Compare average spend between Standard & Express shipping |
| Subscribers vs. Non-Subscribers | Compare total revenue & purchase frequency                |
| Discount-Dependent Products     | Find products most affected by discounts                  |
| Customer Segmentation           | Classify customers into New, Returning, and Loyal         |
| Top 3 Products per Category     | Identify best-sellers within each category                |
| Repeat Buyers & Subscriptions   | Analyze if frequent buyers tend to subscribe              |
| Revenue by Age Group            | Evaluate contribution by age segments                     |

3. Dashboard (Power BI)
An "interactive Power BI dashboard" was created to visualize and summarize findings:
* Revenue breakdown by "gender, age group, and subscription status".
* "Category-wise performance" of products.
* "Top-rated and most-purchased products".
* Insights into "discount impact" and "shipping preferences".

💡 Key Insights & Business Recommendations
1. Boost Subscriptions: Highlight exclusive benefits to encourage sign-ups.
2. Customer Loyalty Programs: Reward repeat buyers to move them into the “Loyal” segment.
3. Review Discount Strategy: Rebalance discounts to maintain margins.
4. Product Positioning: Promote top-rated and high-revenue products.
5. Targeted Marketing: Focus campaigns on high-spending age groups and express-shipping customers.

🚀 How to Run the Project
1. Clone the Repository
"git clone https://github.com/yourusername/customer-shopping-behavior-analysis.git
cd customer-shopping-behavior-analysis"

2. Install Required Libraries
"pip install -r requirements.txt"

3. Run the Notebook
"jupyter notebook customer_behavior_analysis.ipynb"

4. SQL Analysis
* Import cleaned dataset into PostgreSQL.
* Execute queries from `business_queries.sql` file.

5. Dashboard
* Open `Customer_Shopping_Dashboard.pbix` in "Power BI".
* Interact with visuals and filters to explore insights.

📦 Deliverables
* `customer_behavior_analysis.ipynb` → Python code for cleaning & EDA
* `business_queries.sql` → SQL queries for business analysis
* `Customer_Shopping_Dashboard.pbix` → Power BI dashboard
* `Customer_Shopping_Report.pdf` → Summary report
