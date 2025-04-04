# Anti-Money-Laundering-using-MySQL-Power-BI
This project focuses on detecting potential money laundering patterns using MySQL as the primary analytical tool. The goal is to explore how SQL-based logic can be applied to uncover unusual fund movements and transactional behavior, leveraging synthetic financial data.

💼 Anti-Money Laundering (AML) Analysis Using MySQL
 ### Project Overview 📌
This project demonstrates a robust, SQL-based Anti-Money Laundering (AML) detection system, built from scratch using MySQL and synthetically generated financial data. The goal was to simulate real-world banking behavior and apply AML regulations to uncover suspicious activities such as smurfing, multi-hop transactions, high-risk customers, and unusual geographic flows.

⚠️ Note: The data used in this project was synthetically created using ChatGPT assistance, ensuring privacy and regulatory safety. As a result, time-bound queries may not yield real-time trends.

 ### Objectives 🎯
✅ Detect suspicious transactions and structuring behavior (smurfing)

✅ Identify high-risk customers based on transaction patterns

✅ Analyze cross-location and multi-hop transactions to detect laundering networks

✅ Build dynamic, efficient SQL queries using advanced concepts like CTEs, aggregations, and window functions

### Database Schema 🧱
customers_final – Contains customer details (ID, location, etc.)

transactions – Holds transactional data including sender, receiver, amount, and date

risk_parameters – Stores thresholds for flagging suspicious behavior

Indexed on CustomerID, SenderID, ReceiverID, and Date for optimized query performance.

### Key AML Analyses 📊 
🔹 Suspicious Transactions
Transactions just under the regulatory threshold (₹9000–₹9999) flagged using dynamic parameters.

Helps identify intentional structuring to avoid scrutiny.

🔹 High-Risk Customers
Aggregated total transaction amount per customer.

Customers exceeding ₹100,000 flagged as high-risk.

🔹 Smurfing Detection
Detects small, frequent transactions summing over ₹150,000 in a rolling 30-day window.

Implemented using window functions to simulate time-based tracking.

🔹 Cross-Location Transfers
Flags large transactions (>₹80,000) where sender and receiver are in different locations.

Reveals possible cross-border laundering activity.

🔹 Multi-Hop Transaction Detection
Tracks recursive money flows through multiple intermediaries.

Flags cycles where money returns to origin with minimal deviation (±20%).

Implemented via recursive CTEs – ideal for tracing circular laundering schemes.

### Key Insights 💡 
Detected patterns resembling real-world AML threats like smurfing and layering.

Highlighted accounts with disproportionate transaction volumes.

Demonstrated the effectiveness of SQL in modeling AML rules dynamically.

Proved multi-hop tracing can unveil hidden money trails.

### Role Played 🧑‍💼 
Position: AML Data Analyst
Responsibilities:

Designing and writing optimized SQL queries

Generating actionable financial insights

Creating analytical views for stakeholders

Ensuring alignment with AML compliance frameworks

### Key Skills Applied:

SQL (advanced)

Financial risk modeling

Recursive CTEs & window functions

Fraud detection logic

### Project Status 🚧

✅ SQL-based analysis complete
🔄 Power BI dashboard under development (to be uploaded soon)

### What’s Next? 🔮 
-Integration of Power BI dashboards for visualizing:
-Suspicious transaction trends
-Risk scoring heatmaps
-Interactive tracing of fund flows

### Contributions 🤝 
This is an ongoing personal project. 
