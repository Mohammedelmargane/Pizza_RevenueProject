Total_Revenue querie 
```
    select sum(total_price) as Total_Revenue
    from pizza_sales
```
    
Average_Order_Value 
``` 
    select sum(total_price) / COUNT(DISTINCT order_id) AS AVG_OrderValue
    from pizza_sales
```

Total_Pizza_Sold
```
    select sum(quantity) as Total_Pizza_Sold
    from pizza_sales
```
  
Total_Orders
```
    select COUNT(DISTINCT ORDER_ID) AS Total_Orders
    From pizza_sales
```
  
Average_PizzaPerOrder
```
    select CAST(CAST(SUM(quantity) AS decimal(10,2)) / CAST(Count(Distinct Order_id) AS decimal(10,2)) AS decimal(10,2)) AS Average_PizzaPerOrder 
    from pizza_sales
```
  
Total_Orders_PER Day
```
    Select DATENAME(DW, order_date) as Order_day , COUNT(Distinct order_id) as  Total_Orders
    From pizza_sales
    Group by DATENAME(DW, order_date)
```

Total_Orders_PER Month
```
    Select DATENAME(MONTH, order_date) as Month_Name ,COUNT(Distinct order_id) as Total_Orders
    From pizza_sales
    Group by DATENAME(MONTH, order_date)
    ORDER By Total_Orders DESC
```

PCT OF Pizza_Category
```
    Select pizza_category ,CAST(sum(total_price)as decimal(10,2)) as Total_Sales, Sum(total_price) * 100 / (select sum(total_price) from pizza_sales) AS PCT
    From pizza_sales
    Group By pizza_category
```

PCT OF Pizza_Size
```
Select pizza_size ,CAST(sum(total_price)as decimal(10,2)) as Total_Sales,Cast(Sum(total_price) * 100 / (select sum(total_price) from pizza_sales)AS decimal(10,2)) AS PCT
From pizza_sales
Group By pizza_size
Order By PCT DESC
```

Top_Pizzas By Revenue 
```
select top 5 pizza_name , sum(total_price) as Total_Sales From pizza_sales
Group By pizza_name
Order by Total_Sales Desc
```

Buttom_Pizzas By Revenue 
```
select top 5 pizza_name ,Cast(sum(total_price)as decimal(10,2)) as Total_Sales From pizza_sales
Group By pizza_name
Order by Total_Sales ASC
```

TOP_Pizzas By Quantity
```
select top 5 pizza_name ,Cast(sum(quantity)as decimal(10,2)) as Total_Quantity From pizza_sales
Group By pizza_name
Order by Total_Quantity Desc
```

Buttom_Pizzas By Quantity
```
select top 5 pizza_name ,Cast(sum(quantity)as decimal(10,2)) as Total_Quantity From pizza_sales
Group By pizza_name
Order by Total_Quantity ASC
```

TOP_Pizzas By Orders
```
select top 5 pizza_name ,COUNT(DISTINCT Order_id) as Total_Orders From pizza_sales
Group By pizza_name
Order by Total_Orders DESC
```

BUTTOM_Pizzas By Orders
```
select top 5 pizza_name ,COUNT(DISTINCT Order_id) as Total_Orders From pizza_sales
Group By pizza_name
Order by Total_Orders ASC
```
