# Average Price and Product Count by Category

This project is a SQL practice exercise that demonstrates how to use aggregate functions together with `GROUP BY`. The query groups products based on their category and calculates the average price of products in each category using `AVG()`, rounds the average price up to the nearest whole number using `CEIL()`, and counts the total number of products in each category using `COUNT(*)`.

## SQL Query

```sql
SELECT category,
       CEIL(AVG(price)) AS Average_Price,
       COUNT(*) AS Total_Products
FROM product
GROUP BY category;
```

## Concepts Practiced

* `SELECT`
* `AVG()`
* `CEIL()`
* `COUNT()`
* `GROUP BY`
* Column aliases using `AS`
* Aggregate functions

## What the Query Does

* **`category`** → Groups the products by their category.
* **`AVG(price)`** → Calculates the average price within each category.
* **`CEIL()`** → Rounds the average price upward to the next whole number.
* **`COUNT(*)`** → Counts how many products belong to each category.
* **`GROUP BY category`** → Makes the calculations separately for each category.

## Example Output

```text
+----------+---------------+---------------+
| category | Average_Price | Total_Products|
+----------+---------------+---------------+
| Drinks   |          7500 |             3 |
| Clothing |         25000 |             4 |
| Stationery|         5000 |             2 |
+----------+---------------+---------------+
```

## Language

* SQL
* MySQL

# Grouping Products and Filtering with HAVING

This project is a SQL practice exercise that demonstrates how to combine aggregate functions, `GROUP BY`, and `HAVING` to analyze product data. The query groups products by category, calculates the average price for each category, rounds the average price upward using `CEIL()`, counts the total number of products in each category, and then filters the grouped results to only show categories containing more than 10 products.

## SQL Query

```sql
SELECT category,
       CEIL(AVG(price)) AS Average_Price,
       COUNT(*) AS Total_Products
FROM product
GROUP BY category
HAVING Total_Products > 10;
```

## Concepts Practiced

* `SELECT`
* `AVG()`
* `CEIL()`
* `COUNT()`
* `GROUP BY`
* `HAVING`
* Column aliases using `AS`
* Aggregate functions
* Filtering grouped results

## What the Query Does

* **`category`** → Groups products based on their category.
* **`AVG(price)`** → Calculates the average product price within each category.
* **`CEIL()`** → Rounds the average price upward to the nearest whole number.
* **`COUNT(*)`** → Counts the number of products in each category.
* **`GROUP BY category`** → Creates one result row for each category.
* **`HAVING Total_Products > 10`** → Only keeps categories that contain more than 10 products.

