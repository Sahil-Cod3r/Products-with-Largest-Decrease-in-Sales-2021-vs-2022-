# Products with Largest Decrease in Sales (2021 vs 2022)

## 📊 Project Objective
The Sales Team wants to identify products that experienced the biggest drop in sales between 2021 and 2022. This project aggregates total sales (`qty_ordered`) grouped by `sku_name` for each year, computes the difference between the two years, and identifies the **top 10 products with the largest decrease**. Results are visualized using a bar chart to highlight declining product performance.

## 🧮 Calculated Fields
```
Sales_2021 = CASE WHEN YEAR(order_date) = 2021 THEN qty_ordered ELSE 0 END
Sales_2022 = CASE WHEN YEAR(order_date) = 2022 THEN qty_ordered ELSE 0 END
Sales_Decrease = SUM(Sales_2021) - SUM(Sales_2022)
```

## 🗂️ Dataset
**File:** `Sales_Data_2021_2022_SKU`

**Columns used:**
| Column | Description |
|---|---|
| `sku_name` | Name of the product |
| `order_date` | Date of the order (used to determine year) |
| `qty_ordered` | Quantity ordered |
| `category` | Product category |

## 📈 Chart Details
- **Chart type:** Bar chart
- **Dimension:** `sku_name`
- **Metric:** `Sales_Decrease`
- **Sort:** Descending by Sales_Decrease
- **Display:** Top 10 (Others grouping disabled)

## 📷 Chart Screenshot
![Top 10 Products with Largest Sales Decrease]("D:\Elevance skills\Task 5\Products_with_Largest_Sales_Decrease_(2021_vs_2022).pdf")

## 🔍 Key Insight
**Skipping Rope** and **Hair Oil** experienced the largest drop in sales from 2021 to 2022, followed by **Power Bank**, **Yoga Mat**, and **Cotton T-Shirt**. These products may need attention from the sales and marketing teams to understand the cause of decline — whether due to demand shift, competition, or stock issues.

## 🔗 Live Report
**Looker Studio Report:** [Sales Decline 2021 vs 2022](https://datastudio.google.com/reporting/3461f654-6e69-4291-8911-50e56e125d93)

## 🛠️ Tools Used
- Google Sheets (data source)
- Looker Studio (visualization)

---
*Report Name: Sales_Decline_2021_vs_2022*

## 👤 Author
**Sahil Kumar**
