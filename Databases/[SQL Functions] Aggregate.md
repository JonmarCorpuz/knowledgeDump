# Aggregate Function Overview

Aggregate functions are specialized functions that perform calculations on sets of rows and return a single result for each group of rows

```SQL
SELECT function(argument) FROM table_name GROUP BY column;
```

| Agregate Function | Purpose |
| --- | --- |
| `AVG()` | **Computes the average value** of a numeric column for each group |
| `SUM()` | **Calculates the total sum** of a numeric column for each group |
| `COUNT()` | **Counts the number of rows** in each group (Ignores NULL values) |
| `MAX()` | **Finds the maximum value** of a numeric column for each group |
| `MIN()` | **Finds the minimum value** of a numeric column for each group |
| `STDDEV()` | **Computes the standard deviation** of a numeric column for each group (Ignores NULL values) |
| `VARIANCE()` | **Computes the variance** of a numeric column for each group (Ignores NULL values) |

<br>