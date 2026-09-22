**Part 1 — Data Preparation**

Before creating visuals:<br>
Check the data types of all columns.<br>
Convert Date into Date data type.<br>
Convert Age into Whole Number.<br>
Convert Amount into Whole Number/Decimal Number.<br>
Convert Qty into a numeric column.<br>
Replace One with 1 and Two With 2.<br>
Check the values in Gender.<br>
For example: Women and W should be standardized if they represent the same gender.<br>
Check for blank values and duplicate records.<br>


**Part 2 — Create Charts**

1. Total Sales by Category
2. Sales by Channel
3. Orders by Channel
4. Sales by Gender
5. Sales by Size
6. Quantity Sold by Category
7. Sales by State
8. Sales by City
9. Order Status Analysis
10. Sales by Month

**Part 3 — Create DAX Measures**

1. Total Sales
Total Sales = SUM(Sales[Amount])

2. Total Quantity
Total Quantity = SUM(Sales[Qty])

5. Total Orders
Total Orders = DISTINCTCOUNT(Sales[Order ID])

7. Total Customers
Total Customers = DISTINCTCOUNT(Sales[Cust ID])

9. Average Order Value
Average Order Value = DIVIDE([Total Sales], [Total Orders])

11. Maximum Order Amount
Maximum Order Amount = MAX(Sales[Amount])

13. Minimum Order Amount
Minimum Order Amount = MIN(Sales[Amount])

14. Male Customer Count
Male Customers = CALCULATE(COUNTROWS(Sales),Sales[Gender] = "Men")

16. Female Customer Count
Female Customers = CALCULATE(COUNTROWS(Sales), Sales[Gender] = "Women" )

17. Create a measure to calculate the total sales amount for Delivered orders only.
Delivered Sales = CALCULATE( [Total Sales], Sales[Status] = "Delivered")

18. Create a calculated column named Age Group using IF.
Age < 25 → "Young"
Age ≥ 25 → "Adult"

Age Category = IF(Sales[Age] < 25,  "Young", "Adult" )

19. Create a calculated column named Age Group using SWITCH.
Classify customers as:
Age below 25 → "Young"
Age from 25 to 45 → "Adult"
Age above 45 → "Senior"

Age Group =
SWITCH(
    TRUE(),
    Sales[Age] < 25, "Young",
    Sales[Age] <= 45, "Adult",
    "Senior"
)

20. Create a measure to calculate the total quantity sold for customers whose Age is greater than 50 using FILTER.
Quantity Sold Above 50 = CALCULATE(SUM(Sales[Qty]),
    FILTER(Sales,Sales[Age] > 50))

Using CALCULATE and FILTER, calculate the total sales for Delivered orders where Amount is greater than ₹500

Delivered Sales Above 500 =
CALCULATE(SUM(Sales[Amount]),
    FILTER( Sales, Sales[Status] = "Delivered" && Sales[Amount] > 500
    )
)

Question : Create a calculated column named Channel Type using Nested IF and SWITCH.

Amazon → "Marketplace"
Flipkart → "Marketplace"
Myntra → "Fashion Platform"
Ajio → "Fashion Platform"
Meesho → "Marketplace"
Others → "Other"

Task:
Create Channel_Type using Nested IF.
Create Channel_Type1 using SWITCH.
