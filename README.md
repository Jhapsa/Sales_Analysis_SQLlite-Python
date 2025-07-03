# 🛒 Basic Sales Summary Using SQLite and Python

This project demonstrates how to use **SQLite** within a **Python (Jupyter)** environment to extract and visualize basic sales data.

---

## 📂 Dataset

A small, in-memory SQLite database is created with a `sales` table that contains:

- `product` (e.g., Laptop, Mouse)
- `quantity` sold
- `price` per unit

---

## 🧰 Tools & Libraries Used

- Python (Jupyter Notebook or `.py` script)
- `sqlite3` – lightweight SQL database engine built into Python
- `pandas` – for data querying and display
- `matplotlib` – for basic visualization

---

## 🧪 Process Overview

1. Create SQLite database and `sales` table
2. Insert mock product sales data
3. Run SQL query to calculate:
   - Total quantity sold per product
   - Total revenue per product (`quantity * price`)
4. Load SQL results into pandas DataFrame
5. Print the result
6. Plot a bar chart of revenue by product

---

## 💡 SQL Used

```sql
SELECT 
    product,
    SUM(quantity) AS total_qty,
    ROUND(SUM(quantity * price), 2) AS revenue
FROM sales
GROUP BY product
ORDER BY revenue DESC;
```

---

## 📜 Files Included

- `sales_data.db` — SQLite database file
- `sales_summary.py` — Python script to generate analysis
- `sales_chart.png` — Bar chart of product revenue

---

## 👤 Author

**Biswarup Das**  
July 2025

---

## 📄 License

This project is licensed under the [MIT License](LICENSE)
