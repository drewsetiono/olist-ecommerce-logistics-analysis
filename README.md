# Olist E-Commerce Analytics: Diagnosing a Logistics Crisis

## 📌 Executive Summary
Olist, a Brazilian e-commerce platform, boasts a phenomenal checkout pipeline with a remarkably low **0.63% cancellation rate**. However, customer trust is actively being eroded by a hidden logistics crisis. 

This Exploratory Data Analysis (EDA) uncovered an **8.11% average late delivery rate**, which masked catastrophic regional failures (nearly 30% late in Maceió) and a historical supply chain collapse (21.4% failure rate in March 2018). Most critically, the data proves that these shipping delays are artificially suppressing the reviews of high-volume product categories, creating "trap products" that damage brand reputation.

## 🏢 The Business Problem
Stakeholders noticed fluctuating customer satisfaction scores but could not pinpoint the root cause. This project was initiated to answer a critical business question: **Are promised delivery dates costing the company trust, and if so, where is the operational bottleneck?**

## 🛠️ Skills & Tech Stack
* **Language:** Python
* **Data Manipulation:** Pandas (Cleaning, Feature Engineering, Aggregation)
* **Data Visualisation:** Matplotlib, Seaborn (Storytelling, Correlation Mapping)
* **Database Management:** SQL via SQLAlchemy & PyMySQL (Handling Cartesian Joins and Deduplication)

## 🔬 Methodology
1. **Data Integrity & Cleaning:** Diagnosed and resolved revenue-duplicating bugs caused by split-payment Cartesian products in the SQL database. 
2. **Feature Engineering:** Calculated real-world delivery times versus estimated delivery dates to isolate late shipments.
3. **Anomaly Detection:** Grouped data by time, geography, and product category to find true statistical outliers.
4. **Data Storytelling:** Built professional, executive-ready visualisations to prove the correlation between logistics failures and low customer reviews.

## 📊 Results & Visualizations

### 1. The Timeline of a Crisis (March 2018)
Anomaly detection flagged a massive 21.4% late delivery rate in March 2018 (nearly 3x the baseline). This data maps perfectly to a real-world historical event: the nationwide Brazilian postal strike. 

<img width="1184" height="584" alt="image" src="https://github.com/user-attachments/assets/cc048c9c-350f-405f-8425-f64cc61e795c" />

### 2. The Geographic Bottleneck
By filtering for cities with high order volumes, we identified that the logistics network in Maceió is completely failing, with nearly 30% of all packages arriving late. This proves the issue is a regional routing failure, not a company-wide standard.

<img width="984" height="584" alt="image" src="https://github.com/user-attachments/assets/5b895c2f-d2b7-4374-a121-08c9568c752b" />

### 3. The "Trap Product" Effect
By mapping the late delivery rate against the average review score for high-volume categories, we found a clear negative correlation. Categories with the worst shipping times (like Office Furniture and Babies) are heavily penalised in customer reviews, proving that slow shipping actively destroys product ratings.

<img width="980" height="584" alt="image" src="https://github.com/user-attachments/assets/3e55c13a-fb5f-4e1e-8b39-44356902927f" />

## 🚀 Business Recommendations & Next Steps
While this analysis identifies the macro-level bottlenecks, further investigation is required to solve them. If granted access to warehouse-level data and carrier Service Level Agreements (SLAs), the next steps would be:
1. **Drill down into "Office Furniture":** Isolate specific high-delay SKUs to check for dimension/weight correlations that are slowing down carriers.
2. **Audit Regional Carriers:** Analyse courier performance routed specifically into Maceió and São Gonçalo to determine if the delay is a third-party carrier failure or an internal warehouse processing failure.
