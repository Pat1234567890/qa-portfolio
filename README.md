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

=======
Welcome to my QA portfolio. This repo contains:

- **Sample Bug Reports** (`sample-bugs.md`) with embedded screenshots  
- **Test Case Templates** (`test-case-templates.md`) for manual testing  
- **API Test Collection** (`api-tests.postman_collection.json`) for Postman  
- **SQL Snippets** (`sql-snippets.md`) demonstrating data-verification queries  

Feel free to browse each file for detailed QA deliverables.


