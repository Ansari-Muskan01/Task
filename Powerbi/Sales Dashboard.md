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

1. Total Sales<br>
Total Sales = SUM(Sales[Amount])<br>

2. Total Quantity<br>
Total Quantity = SUM(Sales[Qty])<br>

5. Total Orders<br>
Total Orders = DISTINCTCOUNT(Sales[Order ID])<br>

7. Total Customers<br>
Total Customers = DISTINCTCOUNT(Sales[Cust ID])<br>

9. Average Order Value<br>
Average Order Value = DIVIDE([Total Sales], [Total Orders])<br>

11. Maximum Order Amount<br>
Maximum Order Amount = MAX(Sales[Amount])<br>

13. Minimum Order Amount<br>
Minimum Order Amount = MIN(Sales[Amount])<br>

14. Male Customer Count<br>
Male Customers = CALCULATE(COUNTROWS(Sales),Sales[Gender] = "Men")<br>

16. Female Customer Count<br>
Female Customers = CALCULATE(COUNTROWS(Sales), Sales[Gender] = "Women" )<br>

17. Create a measure to calculate the total sales amount for Delivered orders only.<br>
Delivered Sales = CALCULATE( [Total Sales], Sales[Status] = "Delivered")<br>

18. Create a calculated column named Age Group using IF.<br>
Age < 25 → "Young"
Age ≥ 25 → "Adult"<br>

Age Category = IF(Sales[Age] < 25,  "Young", "Adult" )<br>

19. Create a calculated column named Age Group using SWITCH.<br>
Classify customers as:<br>
Age below 25 → "Young"<br>
Age from 25 to 45 → "Adult"<br>
Age above 45 → "Senior"<br>

Age Group =
SWITCH(
    TRUE(),
    Sales[Age] < 25, "Young",
    Sales[Age] <= 45, "Adult",
    "Senior"
)

20. Create a measure to calculate the total quantity sold for customers whose Age is greater than 50 using FILTER.<br>
Quantity Sold Above 50 = CALCULATE(SUM(Sales[Qty]),FILTER(Sales,Sales[Age] > 50))<br>

Using CALCULATE and FILTER, calculate the total sales for Delivered orders where Amount is greater than ₹500<br>

Delivered Sales Above 500 =
CALCULATE(SUM(Sales[Amount]),
    FILTER( Sales, Sales[Status] = "Delivered" && Sales[Amount] > 500
    )
)

Question : Create a calculated column named Channel Type using Nested IF and SWITCH.<br>

Amazon → "Marketplace"
Flipkart → "Marketplace"
Myntra → "Fashion Platform"
Ajio → "Fashion Platform"
Meesho → "Marketplace"
Others → "Other"

Task:
Create Channel_Type using Nested IF.
Create Channel_Type1 using SWITCH.
