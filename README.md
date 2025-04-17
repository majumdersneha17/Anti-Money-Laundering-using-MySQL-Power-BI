# Anti-Money-Laundering-using-MySQL-Power-BI
This project focuses on detecting potential money laundering patterns using MySQL as the primary analytical tool. The goal is to explore how SQL-based logic can be applied to uncover unusual fund movements and transactional behavior, leveraging synthetic financial data.
 
# 🕵️ Anti-Money Laundering (AML) Analysis using MySQL & Power BI

## 📌 Project Summary

This project presents an end-to-end Anti-Money Laundering (AML) analysis framework, built using **MySQL** for data modeling and **Power BI (Import Mode)** for interactive visualizations. The solution is designed to identify suspicious financial activities such as:

- Structuring (Smurfing)
- Multi-hop money flows
- High-risk customer transactions
- Cross-location anomalies

The system leverages **SQL views, recursive logic**, and **configurable risk parameters** to simulate and visualize real-world AML detection scenarios.

---

## 🧱 Database Design

### 🗂️ Core Tables

- **Customers_final**: Stores KYC-verified customer information.
- **Transactions**: Records all financial transactions (SenderID, ReceiverID, Amount, Date, Mode, Location).
- **Risk_Parameters**: Configurable thresholds for defining suspicious activities (e.g., smurfing limits, transaction caps).

### ⚙️ Optimization

- Indexes applied on `CustomerID`, `SenderID`, `ReceiverID`, and `Date` for performance in query execution.
- Time-based simulation included to spread data uniformly across the last 12 months for trend analysis.

---

## 🔍 AML Detection Logic (SQL Views)

### 1️⃣ **Suspicious_Transactions**
Flags transactions with amounts between **$9,000–$9,999**, indicating attempts to evade reporting thresholds.

### 2️⃣ **High_Risk_Customers**
Identifies customers whose total transactions exceed **$2,500,000** over the observed period.

### 3️⃣ **Smurfing_Detection**
Detects structuring behavior by identifying:
- >3 transactions within 30 days
- Cumulative total exceeding **$150,000**

### 4️⃣ **Multi_Hop_Transactions**
Recursive CTE logic to trace money flow through multiple accounts:
- Identifies transactions that return to the original sender within **±20%** of the initial value
- Useful for detecting layering behavior in complex fraud networks

### 5️⃣ **Cross_Location_Transactions**
Analyzes geographic anomalies by flagging transactions conducted from locations that differ from the customer's registered location.

---

## 📊 Power BI Integration

The SQL views were **imported into Power BI using Import Mode** for optimized performance and full DAX functionality. Visuals were built around these views to create an interactive AML dashboard:

- Suspicious Transactions with slicers, mode breakdown, and trend line
- High-Risk Customers with total transaction values and customer risk profiling
- Smurfing Patterns with frequency maps and threshold-based detection
- Multi-Hop Transactions visualized via Sankey chart
- Cross-Location analysis with maps, tables, and bar charts

Each section of the dashboard highlights behavior flagged under AML guidelines and supports visual drilldown for deeper insights.

---

## 🔑 Key Findings

- Multiple transactions clustered around reporting thresholds (~$9,000–$9,999) suggest potential evasion attempts.
- High-risk customers transacted over $100,000 in short windows — indicating placement or layering behavior.
- Smurfing patterns observed in accounts with frequent small transactions aggregating above regulatory thresholds.
- Multi-hop transaction loops detected where money flows back to the origin within ±20% value — a classic laundering red flag.
- Cross-location anomalies identified transactions initiated from locations inconsistent with customer registrations, raising questions around identity misuse or proxy access.

---

## 👩‍💼 Analyst Role Description

**Role**: AML Data Analyst (Enterprise Simulation)

**Responsibilities**:
- Develop SQL logic for rule-based AML detection
- Monitor smurfing, layering, and geographic red flags
- Import and model data in Power BI for advanced reporting
- Create executive-level dashboards to communicate key risk insights
- Recommend remediation or review based on analytical findings

**Tech Stack**:  
`MySQL` | `Power BI (Import Mode)` | `DAX` | `Sankey/Map Visuals` | `SQL Views`


---

## ✅ Conclusion

This AML project simulates an enterprise-grade risk monitoring solution using open-source SQL and Power BI. The analysis surfaces hidden behavioral risks using a combination of rule-based thresholds and recursive transaction tracing.

Designed for financial analysts, auditors, and AML compliance teams, the system demonstrates how robust data modeling and visualization can support fraud prevention, due diligence, and regulatory reporting.

---

> Developed by: Sneha 👩‍💻 | April 2025  
> ### Note: This project uses synthetic data for demonstration purposes only.*



### Contributions 🤝 
This is a personal project. 

## Powe BI Project Link --> https://tinyurl.com/37yxc4cb
