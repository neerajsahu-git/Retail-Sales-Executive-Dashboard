# KPI Measures

## 1. Total Sales

```DAX
Total Sales = SUM(Fact_Sales[GrossSales])
```

**Description:** Calculates the total gross sales.

---

## 2. Total Profit

```DAX
Total Profit = SUM(Fact_Sales[Profite])
```

**Description:** Calculates the total profit.

---

## 3. Total Quantity

```DAX
Total Quantity = SUM(Fact_Sales[Quantity])
```

**Description:** Calculates the total quantity sold.

---

## 4. Total Orders

```DAX
Total Orders = DISTINCTCOUNT(Fact_Sales[OrderID])
```

**Description:** Counts the total number of unique orders.

---

## 5. Profit Margin

```DAX
Profit Margin =
DIVIDE([Total Profit], [Total Sales], 0)
```

**Description:** Calculates the profit margin percentage.

---

## 6. Average Order Value (AOV)

```DAX
Average Order Value =
DIVIDE([Total Sales], [Total Orders], 0)
```

**Description:** Calculates the average revenue generated per order.
