# Power BI Project Task – Fashion E-Commerce Sales Analysis

## Project Overview

You are working as a Data Analyst for a fashion e-commerce business. The company sells products such as Kurtas, Sets, Tops, and Western Dresses through multiple online shopping channels.

Your task is to clean and transform the provided dataset, analyze sales performance, and create an interactive Power BI dashboard to understand customer demographics, product sales, order status, and channel performance.

## 1. Data Preprocessing and Data Cleaning

Perform the following operations using Power Query Editor.

1. Load the provided dataset into Power BI.
2. Identify and remove unnecessary columns, if required.
3. Check for and remove duplicate records where appropriate.
4. Identify and handle missing or blank values.
5. Check and correct data types for all columns.
6. Convert the `Date` column into the Date data type.
7. Standardize the values in the `Gender` column, such as `W` and `Women`.
8. Standardize the values in the `Qty` column, such as `One` and `1`.
11. Check the `Amount` column for invalid or negative values.
12. Check the `Age` column for invalid values.
13. Verify the consistency of `Order ID` and `Cust ID`.
14. Check whether `ship-postal-code` contains missing or invalid values.
15. Check the `B2B` column and ensure it contains consistent Boolean values.
16. Create a new column named `Year` by extracting the year from the `Date` column.
17. Create a new column named `Month Name` by extracting the month name from the `Date` column.
18. Create a new column named `Age Group` by categorizing customers into suitable age groups.
19. Review the final dataset and ensure it is ready for analysis.

## 2. DAX Questions

Create the required calculated columns and measures using DAX.

### A. Basic Measures

1. Calculate Total Sales.
2. Calculate Total Quantity Sold.
3. Calculate Total Orders.
4. Calculate Total Customers.
5. Calculate Average Order Value.
6. Calculate Maximum Order Amount.
7. Calculate Minimum Order Amount.
8. Calculate Total Delivered Orders.
9. Calculate Total Cancelled Orders.
10. Calculate the Delivery Rate as a percentage of total orders.

### B. Calculated Columns

11. Create a new column by combining `Order ID` and `Category`.
12. Extract the year from the `Date` column.
13. Extract the month number from the `Date` column.
14. Extract the month name from the `Date` column.
15. Create an age group column using the `Age` column.
16. Create a column that classifies orders as B2B or B2C using the `B2B` column.

### C. Advanced Measures

17. Calculate Total Sales for the Amazon channel.
18. Calculate Total Sales for the Myntra channel.
19. Calculate the percentage contribution of each channel to total sales.
21. Calculate the percentage of orders by status.
23. Calculate the average sales amount by category.
24. Calculate the sales difference between the selected month and the previous month.
25. Calculate the percentage change in monthly sales compared with the previous month.

## 3. Dashboard and Visualization Questions

Create an interactive Power BI report using the cleaned dataset.

### Page 1 – Sales Overview

1. Create a Card showing Total Sales.
2. Create a Card showing Total Orders.
3. Create a Card showing Total Customers.
4. Create a Card showing Total Quantity Sold.
5. Create a Card showing Average Order Value.
6. Create a clustered column chart showing Total Sales by Channel.
7. Create a bar chart showing Total Sales by Category.
8. Create a donut chart showing Orders by Status.
9. Create a line chart showing Monthly Sales Trends.
10. Create a slicer for Channel, Category, and Date.

### Page 2 – Customer and Product Analysis

1. Create a donut chart showing customer distribution by Gender.
2. Create a column chart showing Total Sales by Age Group.
3. Create a bar chart showing Total Quantity Sold by Size.
4. Create a treemap showing Sales by Category and SKU.
5. Create a matrix showing Channel, Category, Total Sales, and Total Orders.
6. Create a chart comparing Total Sales for B2B and B2C orders.
7. Create a slicer for Gender, Age Group, and Category.

### Page 3 – Location and Order Analysis

1. Create a filled map or map visual showing Total Sales by State.
2. Create a bar chart showing the Top 10 Cities by Total Sales.
3. Create a stacked column chart showing Order Status by Channel.
4. Create a matrix showing State, City, Total Orders, and Total Sales.
5. Create a chart showing Total Sales by Month and Year.
6. Create a slicer for State, City, and Order Status.

## 4. Tooltip Questions

Create report tooltips to display additional information when users hover over visuals.

1. Create a tooltip for the Channel Sales chart showing Channel Name, Total Sales, Total Orders, and Average Order Value.
2. Create a tooltip for the Category Sales chart showing Category Name, Total Sales, Quantity Sold, and Average Sales Amount.
3. Create a tooltip for the Order Status chart showing Order Status, Number of Orders, and Percentage of Orders.
4. Create a tooltip for the State Sales map showing State Name, Total Sales, Total Orders, and Unique Customers.
5. Create a tooltip for the SKU sales visual showing SKU, Category, Size, Quantity Sold, and Total Sales.
6. Create a tooltip for the Monthly Sales chart showing Month, Total Sales, Total Orders, and Month-over-Month Sales Growth.

