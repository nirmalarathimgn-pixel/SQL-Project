# 🛒 E-Commerce SQL Analytics Project

## 📌 Overview

This project analyzes e-commerce data using SQL to generate insights related to customer behavior, revenue trends, and product performance.

---

## 🧱 Database Structure

### Tables:

* customers → customer details
* orders → order details
* order_items → product-level data

---

## 🎯 Objectives

* Calculate total revenue
* Identify top customers
* Analyze product categories
* Detect inactive users
* Perform customer segmentation
* Track monthly revenue trends
* Analyze customer order frequency
* Calculate average order value

---

## 🔍 SQL Concepts Used

* JOIN
* GROUP BY
* ORDER BY
* Aggregation (SUM, COUNT)
* CASE WHEN
* LEFT JOIN

---

## 📊 Key Insights

* 💰 Revenue shows overall business performance
* 👤 Few customers contribute most of the revenue
* 📦 Electronics category dominates sales
* ⚠️ Some customers are inactive (churn risk)
* 🧠 Customer segmentation helps target high-value users
* 📈 Monthly trend shows growth pattern
* 🔁 Frequent buyers indicate loyal customers
* 💸 Average order value shows spending behavior
* 💎 High-priced products contribute more revenue

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
* DB Fiddle
* Visual Studio Code

---

## 📌 Conclusion

This project demonstrates how SQL can be used to analyze structured data, generate business insights, and support decision-making in an e-commerce environment.

---
