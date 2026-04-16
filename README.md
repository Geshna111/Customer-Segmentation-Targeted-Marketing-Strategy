# Customer Segmentation & Targeted Marketing Strategy

> Built a customer segmentation system using RFM analysis and clustering to identify distinct customer groups and design targeted marketing strategies to maximize revenue and retention.

## Problem Statement
Businesses often treat all customers the same, leading to inefficient marketing spend and missed revenue opportunities. 
This project aims to segment customers based on purchasing behavior and design targeted strategies to improve engagement, retention, and overall profitability.

## Dataset
- Source: UCI Machine Learning Repository (Online Retail Dataset)
- Records: ~500,000 transactions
- Features: Transactional data including customer ID, purchase quantity, price, and date

Performed data cleaning by removing missing customer IDs, filtering cancelled transactions, and eliminating invalid entries to ensure accurate behavioral analysis.

## RFM Analysis
RFM (Recency, Frequency, Monetary) analysis was used to quantify customer behavior:

- Recency: Days since last purchase
- Frequency: Number of transactions
- Monetary: Total spending

This transformation converts raw transactional data into meaningful customer-level insights.

## Customer Segments Identified

### 🟢 High Value Customers
- Very recent purchases, high frequency, and extremely high spending

### 🔵 Loyal Customers
- Regular buyers with strong engagement and consistent spending

### 🟡 Potential Customers
- Moderate engagement with opportunity for growth

### 🔴 At Risk Customers
- Low activity, infrequent purchases, and high likelihood of churn

## Segment Distribution & Revenue Contribution

- High Value Customers → 0.3% of customers, contributing ~18.6% of total revenue  
- Loyal Customers → 4.7% of customers, contributing ~29.1% of total revenue  
- Potential Customers → 70.4% of customers, contributing ~46.6% of total revenue  
- At Risk Customers → 24.6% of customers, contributing ~5.8% of total revenue  

This highlights strong revenue concentration, where a small percentage of high-value and loyal customers contribute a disproportionately large share of total revenue.

This indicates a strong Pareto distribution, where a small fraction of customers drive a majority of revenue, making targeted retention and upselling strategies critical for maximizing profitability.

## Key Visualizations

### Customer Segment Distribution
<img src="https://github.com/user-attachments/assets/31ed92ef-6fc9-45c4-97a2-84fe60373c43" width="500"/>

### RFM Distribution
<img src="https://github.com/user-attachments/assets/beb9152d-4da9-4056-a462-7edce330ac49" width="500"/>

## Modeling Approach
- Applied K-Means clustering on scaled RFM features
- Optimal clusters determined using Elbow Method
- Segments labeled based on behavioral patterns and business interpretation
- Features were standardized before clustering to ensure equal contribution across Recency, Frequency, and Monetary dimensions.

## Business Strategies

### High Value Customers
- Loyalty rewards, VIP benefits, early access offers  
→ Goal: Maximize lifetime value  

### Loyal Customers
- Upselling, product bundling, loyalty incentives  
→ Goal: Increase average order value  

### Potential Customers
- Personalized campaigns, repeat purchase incentives  
→ Goal: Convert to loyal customers  

### At Risk Customers
- Reactivation campaigns, targeted discounts, reminders  
→ Goal: Reduce churn and recover customers  

## Business Impact
Segment-based marketing allows businesses to allocate resources more efficiently, prioritize high-value customers, and design targeted interventions that directly impact revenue and retention.

By focusing on high-value and at-risk segments, companies can:
- Increase retention rates
- Improve marketing efficiency
- Drive higher revenue from existing customers

## Future Improvements
- Use advanced clustering techniques (DBSCAN, Hierarchical)
- Incorporate customer demographics and behavioral data
- Deploy as a real-time recommendation or marketing system

## Tech Stack
Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
