# ☕ Coffee Shop Sales Performance Analysis
**Tool:** Microsoft Power BI | **Period:** January 2023 – June 2023

## 📌 Project Overview
This project analyzes coffee shop sales performance across different store locations,
product categories, and time brackets. The objective is to identify sales trends,
best-performing products, peak sales periods, and store performance to support 
better business decision-making.

---

## 📊 Dataset
**Source Table:** `Transactions`
**Supporting Table:** `Dim Date` (Date dimension table)
**Supporting Table:** `Dim Store` (Store dimension table)
**Supporting Table:** `Dim Product` (Product dimension table)
**Measure Table:** `Calculation` (all DAX measures stored here)

**Key columns in Transactions:**
| Column | Description |
|--------|-------------|
| `store_location` | Store branch (Hell's Kitchen, Astoria, Lower Manhattan) |
| `product_category` | Category of product (Coffee, Tea, Bakery, etc.) |
| `product_detail` | Specific product name |
| `transaction_qty` | Quantity sold per transaction |
| `unit_price` | Price per unit |
| `Time Bracket` | ⭐ Custom column — Morning / Afternoon / Evening |

---

## ⭐ Custom Column Added
A **Time Bracket** column was created using Power Query to classify each transaction by time of day:
- **Morning** — peak sales period
- **Afternoon** — moderate sales
- **Evening** — lowest sales period

This column enabled time-based sales analysis across visuals.

---

## 🧮 DAX Measures Created (Calculation Table)
| Measure | Purpose |
|---------|---------|
| `Total Sales` | Sum of all revenue |
| `Total Transaction` | Count of all transactions |
| `Average Sales` | Average revenue per transaction |
| `Total product type` | Count of distinct product categories |
| `Total Product Detail` | Count of distinct product names |
| `Total Sold Product(Detail)` | Total quantity of products sold |
| `Previous Month Sales` | Sales from the prior month |
| `Sales Growth %` | Month-over-month growth percentage |

---

## 🗺️ Data Model
The model follows a **Star Schema**:
- `Transactions` (Fact Table) ←→ `Dim Date` (Dimension Table)
 - `Transactions` (Fact Table) ←→ `Dim Store` (Dimension Table)
 - `Transactions` (Fact Table) ←→ `Dim Product` (Dimension Table)
- `Calculation` table holds all DAX measures (no relationships needed)

---

## 📄 Report Pages

### 1. Dashboard
Interactive overview with:
- **KPI Cards:** Total Transaction, Total Sales, Average Sales, Total Product, Sales Growth %
- **Line Chart:** Total Sales by Month (trend over time)
- **Donut Chart:** Total Sales by Store Location
- **Funnel Charts:** Top products by Sales & by Quantity
- **Clustered Column Charts:** Sales by Product Category | Sales by Time Bracket
- **Slicer:** Filter by Time Bracket (Morning / Afternoon / Evening)

### 2. Analysis
Detailed data tables showing:
- Sales by Month
- Sales by Store Location
- Sales by Product Category (with quantity)
- Sales by Product Detail
- Top products by Quantity Sold
- Sales by Time Bracket
- Sales Growth % and Previous Month Sales cards

### 3. Insights
Executive Summary with written key findings and recommendations.

---

## 🔍 Key Insights
1. **Sales Trend:** Consistent upward growth from Jan–June 2023; June had highest sales
2. **Peak Hours:** Morning generated the highest sales (~$0.39M)
3. **Store Performance:** Hell's Kitchen, Astoria, and Lower Manhattan are fairly balanced
4. **Top Category:** Coffee generates the highest revenue, followed by Tea
5. **Product Pareto:** A few products drive most of the revenue
6. **Transactions:** 149K transactions at an average of $4.69 — frequent but small purchases

---

## 💡 Recommendations
- Introduce **evening discounts and combo deals** to boost off-peak sales
- **Bundle low-selling products** with popular coffee items
- Launch **morning loyalty programs** to capitalize on peak traffic
- Ensure **top-selling products** are always in stock
- Consider **new locations or extended hours** given consistent sales growth

---

## 📸 Screenshots
<img width="1920" height="1019" alt="GBADEGESIN MARIAM POWERBI ASSESSMENT 3_28_2026 11_25_10 AM" src="https://github.com/user-attachments/assets/4c9fb415-8160-47cb-a70f-ce0aa04adabe" />
<img width="1920" height="1019" alt="GBADEGESIN MARIAM POWERBI ASSESSMENT 3_28_2026 11_56_11 AM" src="https://github.com/user-attachments/assets/0c1e5d89-117a-4092-a6f4-276d92efe1d4" />
<img width="1920" height="1019" alt="GBADEGESIN MARIAM POWERBI ASSESSMENT 3_28_2026 11_56_23 AM" src="https://github.com/user-attachments/assets/149b3a2c-8cfe-4ac1-99c9-4f5c236a8c97" />
<img width="1920" height="1019" alt="GBADEGESIN MARIAM POWERBI ASSESSMENT 3_28_2026 11_56_38 AM" src="https://github.com/user-attachments/assets/afdb701d-114c-4a02-8569-702c3342c226" />

## 👩‍💻 Author
**Gbadegesin Mariam Omowumi**
