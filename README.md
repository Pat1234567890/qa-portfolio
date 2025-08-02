# SQL Snippets for Data Verification

## 1. Count Unique Vehicles
```sql
SELECT COUNT(DISTINCT vehicle_id) AS total_vehicle_count
FROM cabs;
SELECT company_name,
       COUNT(DISTINCT vehicle_id) AS fleet_size
FROM cabs
GROUP BY company_name
HAVING COUNT(DISTINCT vehicle_id) < 100
ORDER BY fleet_size DESC;
SELECT order_id, user_id
FROM orders
WHERE order_date IS NULL;
SELECT customer_id,
       SUM(total_amount) AS lifetime_value
FROM orders
GROUP BY customer_id
HAVING SUM(total_amount) > 10000;


