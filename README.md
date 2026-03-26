# 🛒 E-Commerce SQL Analytics Project

## 📌 Overview

This project analyzes an e-commerce dataset using SQL to extract meaningful business insights such as customer behavior, revenue trends, and product performance.

---

## 🧱 Database Structure

### Tables Used:

* **customers** → Customer details (ID, Name, City)
* **orders** → Order details (Order ID, Customer ID, Date)
* **order_items** → Product-level details (Product, Category, Quantity, Price)

---

## 🎯 Objectives

* Analyze total revenue
* Identify top customers
* Find most popular product categories
* Detect inactive customers
* Perform customer segmentation

---

## 🔍 Key SQL Concepts Used

* JOIN (Multiple tables)
* GROUP BY
* ORDER BY
* Aggregation (SUM, COUNT)
* CASE WHEN (Segmentation)
* Filtering (WHERE, HAVING)

---

## 📊 Key Insights

* 💰 **Revenue Analysis**: Total revenue helps evaluate overall business performance
* 👤 **Top Customers**: A small group of customers contributes most of the revenue
* 📦 **Product Trends**: Electronics category dominates sales
* ⚠️ **Inactive Customers**: Some customers have not placed any orders (potential churn)
* 🧠 **Segmentation**: Customers classified into High and Low value groups

---

## 🚀 Sample Query

```sql
SELECT c.customer_id, c.name,
SUM(oi.quantity * oi.price) AS total_spent
FROM customers c
JOIN orders o ON c.customer_id = o.customer_id
JOIN order_items oi ON o.order_id = oi.order_id
GROUP BY c.customer_id, c.name
ORDER BY total_spent DESC;
```

---

## 🛠 Tools Used

* MySQL Workbench
* DB Fiddle (for testing)
* Visual Studio Code

---

## 📌 Conclusion

This project demonstrates how SQL can be used to solve real-world business problems by analyzing structured data and generating actionable insights.

---
