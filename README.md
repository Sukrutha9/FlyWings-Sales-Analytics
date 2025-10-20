 # 🛍️ Fly Wings Sales Analysis

1.[Live Report Link](#Live-report-link)                
2.[Project Objective](#project-objective) 
3.[Dataset Background](#dataset-background) 
      - [Data Model](#data-model)        
4.[Methodology](#methodology)
      - [Data Collection](#data-collection)  
      - [Data Preparation & Cleaning](#data-preparation-&-cleaning) 
      - [Data Modelling](#data-modelling)    
5.[Measures (DAX)](#measures)     
6.[Tools used ](#tools-used)    
7.[Dashboard & Analysis](#dashboard-&-analysis) 
8.[Insights Deep Dive](#insights-deep-dive)      
    -[Key Product Performance](#key-product-performance)        
    -[Top Performing Regions](#top-performing-regions)           
9.[Recommendations](#recommendations)



## [Business Insights 360 Live Report Link](##https://www.novypro.com/profile_about/sukrutha-neeradi-?Popup=memberProject&Data=1760955603328x933997276750236900)


## Project Objective

 This project focuses on **analysing 5 months of clothing retail billing data**to uncover **sales performance, customer behaviour, product trends, and sales team efficiency**. The analysis was conducted using **Excel, Power BI, and Power Query**, with the end goal of building an interactive dashboard that supports data-driven decision-making.

---

## Dataset Background

- **Customer Details:**:The dataset includes information about customers, such as unique identifiers, purchase history, net sales amount, and payment modes. Analysing this data helps identify loyal customers, repeat purchase behaviour, and customer contribution to overall sales.  
                   
- **Product Details:** : Contains information about each product, including category, sub-category, brand, size, net quantity sold, and net sales amount. This enables analysis of top-selling products, category contribution, pricing efficiency, and inventory planning.    
              
- **Salesman Details:**: Includes data on sales personnel performance, such as sales amount per employee and transaction counts. This helps evaluate top and low performers and plan targeted training or incentive programs.    
        
- **Date/Time Details:**:Includes transaction dates and times, enabling analysis of sales trends over time, such as month-over-month growth, seasonal spikes, and peak sale days.        

-----

### Data Model




----------

## Methodology

1.**Data Collection**

- Collected 5 months of sales data from the shop’s billing system.  
- Data provided in **5 separate Excel files** (one file per month).  
- Combined all files into a **single dataset using Excel** before importing into Power BI.

2.**Data Preparation & Cleaning**

After loading the dataset into Power BI, I used Power Query to clean and standardize the data:

- Removed blank rows and irrelevant records.(GST columns, Branch code, Branch name, HSN column)	 
- Deleted “Total Bill” rows to avoid aggregation errors.
- Replaced null values in numeric fields with 0.
- Converted Bill Date column to proper Date format.
- Ensured correct data types for numeric columns (Whole Number for quantities, Decimal for amounts).


3.**Data Modelling**

After completing the necessary data transformations, I structured the dataset into a star schema model for better analysis and performance:

- Fact Table – Duplicated the main sales table and kept only transactional columns (e.g., invoice number, date, customer ID, product ID, quantity, sales amount, discounts).
- Customer Dimension – Extracted unique customer details (e.g., customer ID, customer name, customer type).
- Product Dimension – Extracted unique product details (e.g., product ID, product name, category, sub-category, brand, size).
- Date Dimension – Created a date table using DAX in Power Query to enable time-based analysis (year, quarter, month, week, day).
- Established relationships between fact and dimension tables to ensure a proper star schema design.


## Measures (DAX)

To support decision-making, I defined key business measures in Power BI:
- Total Sales – overall revenue generated during the period.
- Net Quantity Sold – actual number of items sold.
- Average Bill Value – typical revenue generated per customer bill.
- Sales Contribution by Product Category – proportion of sales from each category.
- Customer Purchase Frequency – repeat buying behavior of customers.
- Month-over-Month Growth % – sales trend across months.

These measures provided a clear view of performance at product, customer, and time levels.

---------

## Dashboard & Analysis

 ### Sales Analysis

 Business Questions:

- How are sales trending over months?
- Which payment modes dominate?
- When do customers shop the most?
- How efficient are sales in terms of revenue and volume?

**Insights:**

- Monthly Sales Trend(Line Chart): Seasonal spikes, with noticeable growth toward month-end.
- Payment Mode Split (Pie Chart): Majority (~70%) of transactions in cash.
- Day-wise Sales(Line Chart): Weekends and month-end showed clear spikes.
- Sales Efficiency Matrix: Monthly breakdown of sales, quantity, and avg. selling price revealed efficiency gaps.

### Customer Analysis

Business Questions:

- Are we consistently attracting new customers?
- How loyal are repeat customers?
- What is the average spend per customer?
- How can customers be segmented?

**Insights:**

- New vs Repeat Customers: Repeat customers drove ~60% of revenue.
- Retention Rate: ~65%, indicating moderate customer loyalty.
- Average Spend: Varied across months, peaking during festive periods.
- Segmentation: Clear grouping into new, repeated, unique, and retained customers.

### Product Analysis

Business Questions:

- Which products/categories drive the most revenue?
- Are high-volume items also high in profitability?

**Insights:**

- Top 10 Products(Bar Chart).: Small set of products contributed disproportionately to sales.
- Category Contribution(Column Chart).: Apparel dominated; accessories underperformed.
- Quantity vs Avg Price Matrix: Showed trade-off between volume sellers vs. premium items.


--------

## Tools used:

- Excel → Data collection & merging.
- Power Query → Data cleaning & transformation.
- Power BI → Data modelling, measures, and dashboard creation.

--------

## Insights Deep Dive:

1.Sales are increasing steadily month-on-month, but growth rate varies.
2.Cash transactions dominate (~70%), credit sales form ~30%.
3.A few salesmen contribute to the majority of sales → need to balance performance.
4.Retention is decent, but new customer acquisition is low.
5.Certain products drive majority sales; slow movers require discounts/promotions.


-----------

## Recommendations:

- Introduce loyalty programs to increase repeat purchases.
- Promote slow-moving products with discounts and bundle offers.
- Encourage underperforming salesmen through training and incentives.
- Strengthen credit collection process since credit sales are significant.



