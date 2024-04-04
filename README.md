# Pizza_RevenueProject

## Pizza Revenue Analysis
This project involved an in-depth analysis of pizza sales data to uncover insights into revenue, orders, and item popularity. SQL queries were utilized to extract key metrics from the raw data, which were then visualized in Power BI dashboards to highlight trends and patterns. The goals of the analysis were to understand sales performance, optimize menu offerings, and identify opportunities to boost revenue.

**Data Overview**

The pizza sales data included details on each order such as order date, order total, pizza type, size, quantity, and price. This transaction-level data enabled detailed analysis of revenue, order volume, item-level performance, and temporal trends.

**Analysis Approach**

SQL queries were first written to calculate metrics like total revenue, average order value, total orders, average pizzas per order, and breakdowns by day and month. These key numbers established an overall picture of sales and revenue. Further SQL queries identified top and bottom-selling pizzas by revenue, quantity, and order frequency. These uncovered the most and least popular menu items. Finally, percentage contribution queries revealed insights into pizza categories, sizes, and proportional sales mix.

First Total_Revenue querie 
    ```select sum(total_price) as Total_Revenue from pizza_sales ```
    
Average_Order_Value 
    ``` select sum(total_price) / COUNT(DISTINCT order_id) AS AVG_OrderValue from pizza_sales ```

Total_Pizza_Sold
  ```select sum(quantity) as Total_Pizza_Sold from pizza_sales```
  
Total_Orders
  ```select COUNT(DISTINCT ORDER_ID) AS Total_Orders From pizza_sales```
  
Average_PizzaPerOrder
  ```select CAST(CAST(SUM(quantity) AS decimal(10,2)) / CAST(Count(Distinct Order_id) AS decimal(10,2)) AS decimal(10,2)) AS Average_PizzaPerOrder from pizza_sales```
  
Total_Orders_PER Day
  ```Select DATENAME(DW, order_date) as Order_day , COUNT(Distinct order_id) as  Total_Orders From pizza_sales Group by DATENAME(DW, order_date) ```

Total_Orders_PER Month

```Select DATENAME(MONTH, order_date) as Month_Name , COUNT(Distinct order_id) as Total_Orders 
From pizza_sales
Group by DATENAME(MONTH, order_date)
ORDER By Total_Orders DESC ```







**Dashboards**

![alt text](https://github.com/Mohammedelmargane/Pizza_RevenueProject/blob/785f840eee1f34d78cbd6a44e885efc8a6dc696b/Images/Screenshot%202023-09-30%20195100.png)

Visualizations in Power BI transformed the SQL query output into dynamic dashboards. Key charts included total revenue over time, revenue by day of week, top selling items, and sales by category and size. Slicers enabled filtering the data on various dimensions. The dashboards provided an interactive vizual interface to explore results.

**Outcomes**

The analysis yielded actionable insights for the pizza company. Low-selling pizzas were identified as candidates to remove from the menu. Popular items and sizes were highlighted to feature more prominently. Slow days of the week were revealed as opportunities for promotional campaigns to drive orders. In summary, the project enabled data-driven decision making to maximize revenue. The SQL queries and Power BI dashboards created can be easily adapted for ongoing analytics.

![](https://github.com/Mohammedelmargane/Pizza_RevenueProject/blob/785f840eee1f34d78cbd6a44e885efc8a6dc696b/Images/Screenshot%202023-09-30%20195633.png)


