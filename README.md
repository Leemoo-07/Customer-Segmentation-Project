# Customer Segmentation & Retention Analytics

## Project Overview
It is significantly more expensive to acquire a new customer than to retain an existing one. This project analyzes a transactional dataset of over 500,000 records to identify distinct customer purchasing behaviors and segment them using machine learning. The goal is to allow businesses to launch targeted marketing campaigns and identify at-risk customers before they churn.

## Tech Stack
* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Machine Learning:** Scikit-Learn (K-Means Clustering, StandardScaler)
* **Visualization:** Plotly (Interactive 3D), Matplotlib, Seaborn

## Methodology
1. **Data Cleaning:** Filtered out anonymous users, cancellations, and pricing errors from a raw dataset of 525,461 transactions.
2. **Feature Engineering:** Calculated **RFM (Recency, Frequency, Monetary)** scores to quantify customer behavior.
3. **Data Transformation:** Applied Log Transformation and Standardization to handle extreme monetary outliers ("whales") and normalize features.
4. **Machine Learning:** Deployed **K-Means Clustering** to segment 4,312 unique customers into distinct behavioral profiles.
5. **Inference Pipeline:** Built an interactive prompt that accepts new customer data and predicts their segment in real-time.

## Business Insights (The Clusters)
The algorithm successfully identified three distinct customer profiles:
* **VIP Customers:** High frequency, massive total spend, purchased very recently. *(Action: Reward programs, early access to new products)*
* **Average Customers:** Moderate spend and frequency, purchased within the last few months. *(Action: Upsell campaigns, seasonal discounts)*
* **At-Risk Customers:** Very low spend, single purchases, haven't returned in over 5 months. *(Action: Aggressive win-back emails, heavy discounts)*
