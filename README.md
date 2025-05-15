# Analyzing Customer Purchases for Key Insights
## 📌 Project Overview

This project was completed as part of my internship, focusing on analyzing real-world customer transaction data from an online retail store. The dataset includes detailed information on purchases, customers, and invoice records. The primary objective was to uncover actionable business insights, segment customers using clustering techniques, estimate Customer Lifetime Value (CLV) through RFM analysis, and explore possibilities for predicting future purchase behavior.

---

## 📁 Dataset

- **Source**: [UCI Machine Learning Repository - Online Retail Dataset](https://archive.ics.uci.edu/ml/datasets/online+retail)
- **Size**: ~500K transactions
- **Columns**: InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country

---

## 📊 Task Breakdown

### 1. 🔧 Data Cleaning
- Removed rows with missing CustomerID values
- Removed duplicate records
- Filtered out rows where Quantity ≤ 0 or UnitPrice ≤ 0 (invalid transactions)
- Converted InvoiceDate to datetime format
- Extracted new columns from `InvoiceDate`:`Month`,`Day`,`Year`,`Hour`
  

### 2. 🔄 Data Transformation
- Added new features: `TotalPrice`, `InvoiceMonth`, `Weekday`, `Hour`
- Aggregated customer-level data for analysis(e.g., total spend, purchase frequency, repeat customer count, etc.)

### 3. 📈 Exploratory Data Analysis (EDA)
- Summary statistics of customer behavior
- Most popular products by frequency & revenue
- Monthly sales trends and peak sales hours

### 4. 🧠 Customer Segmentation (K-Means)
- Applied RFM (Recency, Frequency, Monetary) analysis
- Performed K-Means clustering to identify 3 distinct customer groups
- Identified top-value and at-risk customer segments

### 5. 📦 Customer Lifetime Value (CLV)
- Estimated CLV using simple RFM metrics
- Labeled customers with RFM scores (e.g., 333 = best)
- Recommended retention and reactivation strategies

### 6. 🔮 Predictive Modeling 
- Built binary classification models to predict likelihood of a repeat purchase
- Used Logistic Regression, Random Forest, and XGBoost
- Random Forest performed best based on F1-score

---

## 🖼️ Visualizations

- Histograms of customer spending
- Bar charts for most popular products
- Line plots showing sales trends over time
- Scatter plots for customer clusters
- Confusion matrix for model performance

---

## 📊 Key Insights Summary
🛒 Top-Selling Products
- **JUMBO BAG RED RETROSPOT leads in sales with over 43,000 units sold.**

Other high performers include:

- **WORLD WAR 2 GLIDERS ASSTD DESIGNS**
- **WHITE HANGING HEART T-LIGHT HOLDER**
- **ASSORTED COLOUR BIRD ORNAMENT**

Common traits: small, decorative, low-cost — appealing for gifts and impulse buys.

📆 Monthly Sales Trends
Highest Revenue Months: 
- **🟢 November, December, October**

Lowest Revenue Months: 
- **🔴 February, April, January**

📌 Likely due to seasonal shopping surges in Q4 and drops post-holidays.

📅 Daily Sales Patterns
Best Performing Days: 
- **Thursday, Tuesday, Wednesday**

Least Performing Days: 
- **Saturday, Sunday**

📌 Indicates B2B or workweek shopping patterns.

⏰ Hourly Sales Patterns
Peak Hours:

- **🕛 12 PM (highest)**
- **🕙 10 AM**
- **🕐 1 PM**

Off-Peak Hours: Early morning (6–7 AM), late evening (post 4 PM)

📌 Suggests mid-day shopping spikes.

👥 Customer Segmentation (K-Means Clustering)**
- **Cluster 0: 50.5% of total revenue, low repeat purchases — high-value one-time buyers**
- **Cluster 2: 30.9% revenue, highest average repeat purchases (~73)**
- **Cluster 1: 18.6% revenue, moderate loyalty**

🔁 Recommendations
- **🧊 Boost sales in low months via seasonal campaigns and targeted offers.**
- **📅 Activate weekends with flash sales or exclusive online events.**
- **⏰ Spread sales efforts beyond peak hours with timed discounts or automated reminders.**
- **💎 Engage high-spending Cluster 0 with loyalty perks to drive retention.**
- **🤝 Upsell to loyal Clusters 1 & 2 to increase order value.**
---

## 🧰 Tech Stack

- **Python**
- **Jupyter Notebook**
- **Pandas, NumPy**
- **Matplotlib, Seaborn**
- **Scikit-learn**
- **XGBoost (optional)**

---

## 🚀 How to Run

```bash
# 1. Clone the repo
git clone https://github.com/your-username/online-retail-analysis.git

# 2. Navigate into the folder
cd online-retail-analysis

# 3. Open Jupyter Notebook and run the `.ipynb` file
jupyter notebook# CustomerPurchaseReport
