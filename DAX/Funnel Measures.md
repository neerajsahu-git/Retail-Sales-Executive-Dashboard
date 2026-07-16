# Funnel Measures

This document contains DAX measures used to build the sales conversion funnel, tracking customer progression from visitors to completed orders.

---

## 1. Orders

```DAX
Orders =
DISTINCTCOUNT(Fact_Sales[OrderID])
```

**Description:** Counts the total number of unique customer orders.

---

## 2. Customers

```DAX
Customers =
DISTINCTCOUNT(Dim_Customer[CustomerID])
```

**Description:** Counts the total number of unique customers.

---

## 3. Quantity Sold

```DAX
Quantity Sold =
SUM(Fact_Sales[Quantity])
```

**Description:** Calculates the total quantity of products sold.

---

## 4. Visitors

```DAX
Visitors =
ROUND([Orders] / 0.248, 0)
```

**Description:** Estimates the total number of website visitors based on an assumed 24.8% order conversion rate.

> **Note:** This is an estimated metric derived from a predefined conversion rate, not an actual visitor count.

---

## 5. Add To Cart

```DAX
Add To Cart =
ROUND([Visitors] * 0.40, 0)
```

**Description:** Estimates the number of visitors who added products to their cart using an assumed 40% add-to-cart rate.

> **Note:** This is an estimated metric based on a predefined conversion assumption.

---

## 6. Checkout

```DAX
Checkout =
ROUND([Add To Cart] * 0.72, 0)
```

**Description:** Estimates the number of customers who reached the checkout stage using an assumed 72% checkout rate.

> **Note:** This is an estimated metric based on a predefined conversion assumption.
