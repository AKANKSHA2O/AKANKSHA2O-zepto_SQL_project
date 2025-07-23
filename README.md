# 🛒 Zepto Inventory Analytics Dashboard

A powerful SQL-driven e-commerce data analysis project simulating real-world inventory insights for **Zepto** — one of India’s fastest-growing quick-commerce startups. This project uncovers **pricing inefficiencies**, **stock insights**, and **discount-driven opportunities** using SQL queries and structured data storytelling.

---

## ✨ Project Purpose

The **Zepto Inventory Analytics Project** is a comprehensive **SQL-based case study** that simulates real-world e-commerce problem solving. The goal is to explore patterns in:

- Product pricing and discounts
- Inventory availability
- Category-level performance
- Revenue optimization

Ideal for aspiring data analysts seeking hands-on experience with business-focused data exploration.

---

## ⚙️ Tech Stack

| Purpose               | Tools Used                        |
|-----------------------|------------------------------------|
| Database              | 🗃️ PostgreSQL                     |
| GUI / Data Import     | 🖥️ pgAdmin                        |
| Query Language        | 📈 SQL (Structured Query Language) |
| Dataset Format        | 📄 CSV (UTF-8 Encoded)             |
| (Optional) Visualization | 📊 Power BI / Excel             |

---

## 📂 Data Source

- **Dataset**: Zepto Inventory Dataset (scraped from Zepto)
- **Hosted On**: Kaggle
- **Size**: ~20,000+ rows
- **Format**: CSV

### 📌 Columns in the Dataset:
- `sku_id` – Unique Product ID  
- `name` – Product Name  
- `category` – Product Category (e.g., Fruits, Dairy, Snacks)  
- `mrp`, `discountPercent`, `discountedSellingPrice` – Pricing Fields  
- `availableQuantity`, `outOfStock` – Stock Information  
- `weightInGms`, `quantity` – Product Size Metrics  

---

## 🔍 Project Highlights

### 🧩 Business Problem
Zepto’s listings have inconsistencies: duplicate SKUs, invalid prices, stock-out confusion. Business users need **data visibility** to make better decisions.

---

### 🎯 Project Objectives
Use SQL to:
- Clean and standardize raw inventory data  
- Discover patterns in stock health, pricing, and discounting  
- Identify high-opportunity product categories  
- Simulate a **real-world e-commerce analysis workflow**

---

## 🧠 Key Insights and Queries

### 📦 Inventory Health
- Segmented stock into **In-stock vs Out-of-stock**
- Grouped weights into **Low / Medium / Bulk**

### 💰 Pricing Insights
- Converted pricing from paise to ₹  
- Calculated **price per gram** to identify value products  
- Flagged overpriced SKUs (e.g., MRP > ₹500, no discount)

### 🛍️ Discount & Revenue Analysis
- Top 10 products by **discount %**
- Categories with **highest average discount**
- Estimated **revenue potential** per category

---

### 📌 Sample Query: Top Discounted Categories

```sql
SELECT category, ROUND(AVG(discountPercent), 2) AS avg_discount
FROM zepto
GROUP BY category
ORDER BY avg_discount DESC
LIMIT 5;


📸 Screenshots / Demos
<h2 align="center">📊 Zepto Dashboard – Power BI Visualization</h2>

<p align="center">
  <img src="Zepto Dashboard.png" width="1000">
</p>

