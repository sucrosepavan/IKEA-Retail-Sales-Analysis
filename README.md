# 🛍️ IKEA Retail Sales Analysis — SQL Case Study

> End-to-end retail transaction analysis using MySQL and Python to uncover customer behaviour, product performance, revenue trends, and business insights.

---

## 📌 Project Overview

This project simulates how a retail analytics team would use raw transaction data to answer real business questions:

- **When** do customers shop?
- **Who** are the most valuable customers?
- **Which products** drive revenue vs. volume?
- **How much revenue** is lost due to returns?
- **Can we identify** VIP customers worth retaining?

---

## 🧱 Dataset

Transactional retail data with the following schema:

| Column | Description |
|---|---|
| `invoiceno` | Unique order identifier |
| `date` | Purchase date |
| `time` | Purchase time |
| `stockcode` | Product code |
| `description` | Product name |
| `quantity` | Units purchased (negative = return) |
| `unitprice` | Price per unit |
| `custid` | Customer ID |
| `country` | Customer location |

---

## 🧹 Data Cleaning

Pre-processing performed using **Python (Pandas)** before importing into MySQL:

- Split `InvoiceDate` → separate `Date` and `Time` columns
- Converted European date format → MySQL-compatible format
- Handled `NULL` and blank values during import
- Fixed datatype mismatches (`InvoiceNo` stored as `VARCHAR` due to cancellation codes)
- Flagged and handled negative quantities (returns)

---

## 📊 Key Business Insights

### 🕒 Customer Shopping Behaviour
- Sales peak during specific hours of the day
- Weekdays generate higher revenue than weekends
- Evening hours contribute disproportionately high order counts

### 👤 Customer Analytics
- Segmented customers into **High / Medium / Low** value tiers
- Identified **Top 5% VIP customers** using percentile ranking with window functions
- Detected **one-time buyers** and **churned customers**
- Computed **repeat purchase cycle** using purchase gap analysis

### 🛒 Product Performance
- Top products by **revenue** differ significantly from top products by **quantity**
- Some items sell frequently but generate low revenue
- Premium items sell rarely but contribute disproportionate profit

### 🔁 Returns & Revenue Loss
- Returns detected via negative quantity and cancellation invoice codes
- Identified products with **disproportionately high return rates**
- Quantified total **revenue lost due to returns**

### 🌍 Geographic Trends
- Revenue contribution varies significantly by country
- Different regions show distinct product preferences

---

## 🧠 Advanced Analytics

| Technique | Purpose |
|---|---|
| RFM Analysis (Recency, Frequency, Monetary) | Customer value scoring |
| Customer Segmentation | Tier-based grouping |
| Repeat Purchase Cycle Detection | Retention timing insights |
| Cohort Identification | Customer group behaviour |
| Pareto (80/20) Rule | Identify top revenue-driving customers |
| Order Pattern Analysis | Basket and behaviour patterns |
| Time-based Sales Analysis | Hourly and daily trends |

---

## 🛠️ Tech Stack

| Tool | Usage |
|---|---|
| **MySQL 8** | Core data analysis and querying |
| **Python (Pandas)** | Pre-processing and data formatting |
| **SQL Window Functions** | Advanced behavioural analytics |

---

## 📂 Project Structure

```
IKEA-Retail-SQL-Analysis/
│── ikea.zip
│   └── ikea/
│   └── ikea_updated/
│── Cleaning.ipynb       # Data pre-processing notebook
│── ikea.sql             # All SQL queries and analysis
│── README.md
```

---

## 🚀 What I Learned

- Handling messy, real-world retail datasets at scale
- Writing analytical SQL beyond basic `SELECT` queries
- Using **window functions** for customer behavioural analysis
- Translating raw data into actionable business decisions

---

## 📈 Business Value

This project demonstrates how a retail company can use transaction data to:

- Optimise inventory based on product performance
- Improve marketing targeting through customer segmentation
- Identify and retain high-value customers
- Reduce product returns through pattern detection
- Predict repeat purchase timing

---

## 👤 Author

**Pavan Kumar Reddy** — [LinkedIn](https://linkedin.com/in/p-pavan) | [Medium](https://medium.com/)

> *B.Tech in Electrical & Electronics Engineering | Aspiring Data Analyst*
