# Data Description

This dataset contains five tables: Customer, Date, Product, Region, and Orders. Together, these tables provide information about customers, products, order transactions, dates, and geographical locations. This data can be used in Power BI to analyze sales performance, profit, customer behavior, product performance, regional sales, and delivery operations.

## 1. Customer Table

* **Customer_ID:** Unique ID assigned to each customer.
* **Customer_Name:** Name or identifier of the customer.
* **Segment:** Customer category, such as Consumer or Corporate.
* **Customer_Age_Group:** Age group of the customer, such as 18–25, 26–40, 41–60, or 60+.
* **Gender:** Gender of the customer, such as Male or Female.
* **Loyalty_Status:** Customer loyalty level, such as Bronze, Silver, or Gold.
* **Join_Date:** Date when the customer joined the business.

## 2. Date Table

* **Date_ID:** Date key used to connect orders with calendar information.
* **Year:** Calendar year.
* **Month:** Month number, from 1 to 12.
* **Quarter:** Quarter of the year, from Q1 to Q4.
* **Day_Name:** Name of the day, such as Monday or Sunday.
* **Week_Number:** Week number within the year.
* **Is_Weekend:** Indicates whether the date falls on a weekend (TRUE or FALSE).
* **Financial_Year:** Financial year associated with the date, such as FY23.

## 3. Product Table

* **Product_ID:** Unique ID assigned to each product.
* **Category:** Main product category, such as Furniture, Technology, or Office Supplies.
* **Sub_Category:** Specific product group, such as Chairs, Binders, Storage, or Phones.
* **Brand:** Brand associated with the product.
* **Product_Name:** Name or identifier of the product.
* **Unit_Price:** Price of one unit of the product.
* **Launch_Year:** Year in which the product was launched.

## 4. Region Table

* **Region_ID:** Unique ID assigned to each geographical record.
* **Region:** Geographical region, such as North, South, East, or West.
* **City:** City associated with the record.
* **State:** State code associated with the location.
* **Country:** Country where the location is situated.
* **Zone:** Location classification, such as Tier1, Tier2, or Tier3.
* **Pin_Code:** Postal code associated with the location.

## 5. Orders Table

* **Order_ID:** Unique ID assigned to each order.
* **Customer_ID:** Identifies the customer who placed the order.
* **Product_ID:** Identifies the product included in the order.
* **Region_ID:** Identifies the geographical location associated with the order.
* **Date_ID:** Identifies the order date.
* **Sales:** Sales amount recorded for the order.
* **Quantity:** Number of units ordered.
* **Profit:** Profit earned from the order.
* **Discount:** Discount applied to the order, represented as a decimal (for example, 0.06 means 6%).
* **Cost_Price:** Cost price associated with the product or order.
* **Selling_Price:** Selling price associated with the product or order.
* **Shipping_Cost:** Cost incurred to ship the order.
* **Order_Priority:** Priority level of the order, such as Low, Medium, or High.
* **Delivery_Days:** Number of days taken to deliver the order.

## Purpose of the Dataset

The Orders table acts as the central transaction table and connects with the Customer, Product, Region, and Date tables using their respective IDs. These tables can be used together in Power BI to create an interactive sales dashboard.

The dashboard can help analyze:

* Total sales, total profit, quantity sold, and average discount.
* Sales and profit by product category, sub-category, and brand.
* Customer distribution by segment, gender, age group, and loyalty status.
* Sales trends by month, quarter, year, and financial year.
* Regional performance by region, city, state, and zone.
* Order priority, shipping costs, and delivery time.
* Products and regions generating higher or lower profits.



