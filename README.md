SELECT date_trunc('month', order_date) AS month,
       COUNT(DISTINCT customer_id) AS unique_customers,
       COUNT(DISTINCT order_id) AS total_orders,
       SUM(order_total) AS total_revenue
FROM orders
GROUP BY month
ORDER BY month ASC;

