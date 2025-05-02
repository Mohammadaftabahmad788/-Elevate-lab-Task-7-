# Elevate-Task-7

📊 SQLite Sales Analysis with Pandas and Jupyter


 Tools & Technologies Used

- **Jupyter Notebook**
- **Python 3**
- **SQLite (via `sqlite3` module)**
- **Pandas**
- **Matplotlib**
- **SQL**

---

 Files Included

- `sales_data.db` – SQLite database file
- `sales_chart.png` – Output image of revenue chart
- `Sales_Analysis.ipynb` – Jupyter Notebook with full code and explanation

---

 What I Did

1. **Connected to SQLite** using Python's `sqlite3` module
2. **Created a `sales` table** (if not already present)
3. **Inserted sample product sales data** into the table
4. **Executed SQL query** to calculate:
   - Total quantity sold per product
   - Total revenue (`quantity * price`) per product
5. **Loaded query results into a pandas DataFrame**
6. **Plotted a bar chart** of revenue using `matplotlib`
7. **Saved the chart** as a PNG image (`sales_chart.png`)

---

 SQL Query Used

```sql
SELECT 
    product, 
    SUM(quantity) AS total_qty, 
    SUM(quantity * price) AS revenue 
FROM sales 
GROUP BY product;
```

---

### 📊 Output Example

| product | total_qty | revenue |
|---------|-----------|---------|
| Apple   | 15        | 225     |
| Banana  | 35        | 175     |
| Orange  | 8         | 80      |

---

 Bar Chart

Revenue per product is displayed in a simple bar chart using Matplotlib.
