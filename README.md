# Customer Segmentation & Retention Analytics

## Project Overview

Customer retention is a critical business problem because retaining existing customers is often more cost-effective than acquiring new ones. This project analyzes over 500,000 transactional records to understand customer purchasing behavior and develop actionable customer segments.

Using **RFM (Recency, Frequency, Monetary)** analysis combined with **K-Means clustering**, 4,312 customers were grouped into distinct behavioral segments. The resulting segments were interpreted from a business perspective to identify high-value, regular, and at-risk customers and recommend appropriate retention strategies.

The project also includes an interactive inference pipeline that assigns a new customer's RFM profile to an existing customer segment.

## Dataset & Data Quality

* **Raw transactions:** 525,461
* **Customer-level records after aggregation:** 4,312
* Anonymous transactions without a Customer ID were removed.
* Cancelled/invalid transactions were excluded.
* Transactions with non-positive quantity or price were filtered out.
* Customer-level RFM features were generated from the cleaned transactional data.

## RFM Feature Engineering

Because RFM variables can be highly skewed, a logarithmic transformation was applied to reduce the influence of extreme values. The transformed features were then standardized before K-Means clustering.

| Feature       | Definition                                     | Business Meaning                      |
| ------------- | ---------------------------------------------- | ------------------------------------- |
| **Recency**   | Days since the customer's most recent purchase | How recently the customer purchased   |
| **Frequency** | Number of distinct orders/invoices             | How frequently the customer purchases |
| **Monetary**  | Total customer spending                        | How valuable the customer is          |

## Tech Stack

* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Machine Learning:** Scikit-Learn (K-Means Clustering, StandardScaler)
* **Visualization:** Plotly (Interactive 3D), Matplotlib, Seaborn

## Business Insights (The Clusters)

K-Means clustering produced three customer segments with distinct purchasing profiles:

* **VIP Customers:** High purchase frequency, high total spend, and very recent purchases. *(Action: Reward programs, early access to new products)*
* **Average Customers:** Moderate spend and purchase frequency, with relatively recent purchasing activity. *(Action: Upsell campaigns, seasonal discounts)*
* **At-Risk Customers:** Very low spend, low purchase frequency, and long periods since their last purchase. *(Action: Aggressive win-back emails, heavy discounts)*
