# Display Measures

This document contains DAX measures that format growth metrics with upward (▲) and downward (▼) indicators, making KPI cards easier to read and interpret.

---

## 1. Sales Growth Display

```DAX
Sales Growth Display =
IF(
    [Sales Growth %] >= 0,
    "▲ " & FORMAT([Sales Growth %], "0.0%"),
    "▼ " & FORMAT([Sales Growth %], "0.0%")
)
```

**Description:** Displays the Sales Growth percentage with an upward (▲) or downward (▼) indicator based on year-over-year performance.

---

## 2. Profit Display

```DAX
Profit Display =
IF(
    [Profit Growth %] >= 0,
    "▲ " & FORMAT([Profit Growth %], "0.0%"),
    "▼ " & FORMAT([Profit Growth %], "0.0%")
)
```

**Description:** Displays the Profit Growth percentage with a visual trend indicator.

---

## 3. Profit Margin Display

```DAX
Profit Margin Display =
IF(
    [Profit Margin Growth %] >= 0,
    "▲ " & FORMAT([Profit Margin Growth %], "0.0%"),
    "▼ " & FORMAT([Profit Margin Growth %], "0.0%")
)
```

**Description:** Displays the Profit Margin Growth percentage with an up/down indicator to highlight changes in profitability.

---

## 4. Quantity Display

```DAX
Quantity Display =
IF(
    [Quantity Growth %] >= 0,
    "▲ " & FORMAT([Quantity Growth %], "0.0%"),
    "▼ " & FORMAT([Quantity Growth %], "0.0%")
)
```

**Description:** Displays the Quantity Growth percentage with a directional indicator.

---

## 5. Order Display

```DAX
Order Display =
IF(
    [Order Growth %] >= 0,
    "▲ " & FORMAT([Order Growth %], "0.0%"),
    "▼ " & FORMAT([Order Growth %], "0.0%")
)
```

**Description:** Displays the Order Growth percentage with an up/down indicator for quick performance analysis.

---

## 6. AOV Display

```DAX
AOV Display =
IF(
    [AOV Growth %] >= 0,
    "▲ " & FORMAT([AOV Growth %], "0.0%"),
    "▼ " & FORMAT([AOV Growth %], "0.0%")
)
```

**Description:** Displays the Average Order Value (AOV) Growth percentage with an upward or downward indicator.
