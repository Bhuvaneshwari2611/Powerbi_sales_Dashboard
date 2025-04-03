Sales-Dashboard

Problem Statement

This Sales Dashboard helps businesses analyze their sales performance effectively. It provides insights into key sales metrics, revenue trends, and customer behavior. By understanding sales patterns, companies can identify areas for improvement and optimize their strategies to increase profitability. The dashboard also includes KPI tracking, helping businesses monitor their goals and make data-driven decisions.

Since the total revenue and profit margins fluctuate across different regions and product categories, businesses must focus on enhancing their sales strategies and identifying key revenue-driving products.

Steps Followed

Step 1 : Loaded sales data (CSV format) into Power BI Desktop.

Step 2 : Opened Power Query Editor and checked column quality, distribution, and profile.

Step 3 : Ensured column profiling was based on the entire dataset.

Step 4 : Identified and handled null or incorrect values in columns like Sales Amount, Profit, and Discount.

Step 5 : Created calculated columns and measures using DAX for KPI tracking.

Step 6 : Applied visual filters (slicers) for fields like Region, Product Category, Customer Segment, and Sales Channel.

Step 7 : Designed the dashboard layout using Power BI visualizations such as bar charts, line charts, and card visuals.

Step 8 : Created a sales performance KPI section with calculated metrics.

Step 9 : Inserted branding elements like the company logo, title, and tagline.

Step 10 : Published the report to Power BI Service for sharing and collaboration.

DAX Calculations

1. Total Revenue

Total Revenue = SUM(SalesData[Sales Amount])

2. Total Profit

Total Profit = SUM(SalesData[Profit])

3. Profit Margin (%)

Profit Margin = DIVIDE([Total Profit], [Total Revenue]) * 100

4. Total Orders

Total Orders = COUNT(SalesData[Order ID])

5. Average Order Value (AOV)

Average Order Value = DIVIDE([Total Revenue], [Total Orders])

6. Customer Count

Total Customers = DISTINCTCOUNT(SalesData[Customer ID])

7. Sales Growth (%)

Sales Growth =
VAR PreviousPeriod = CALCULATE([Total Revenue], DATEADD(SalesData[Order Date], -1, YEAR))
RETURN IF(PreviousPeriod = 0, BLANK(), ([Total Revenue] - PreviousPeriod) / PreviousPeriod * 100)

Key Insights

1. Sales Performance

Total Revenue: $10M

Total Profit: $1.2M

Profit Margin: 11.9%

Total Orders: $5k

2. Revenue Distribution by Region

Highest revenue is generated in Ontario

Lowest revenue is observed in Nunavut

3. Sales Growth Trend

Sales grew by **15% **compared to the previous year.

The highest sales were recorded in January, while the lowest was in July.

Dashboard Snapshots

Power BI Desktop Report

Sales Dashboard Snapshot - Desktop
![Image](https://github.com/user-attachments/assets/26c425b2-7af1-4cbf-99ef-04b607b58e9d)
![Image](https://github.com/user-attachments/assets/c6e4d06b-031a-422d-b635-b16dff25f902)
![Image](https://github.com/user-attachments/assets/c23d56ca-34ae-4045-9b92-8a822de62303)
![Image](https://github.com/user-attachments/assets/86405afd-f3f4-4051-8c94-52e65f9dbe5e)
![Image](https://github.com/user-attachments/assets/5107cf53-3ad1-4b48-b276-b1c465d0bc49)
![Image](https://github.com/user-attachments/assets/17132572-ad72-47d8-996e-a19cbecd26d0)
![Image](https://github.com/user-attachments/assets/dc2c4daa-8bcb-416f-bb6f-50137788db72)



Conclusion

The Sales Dashboard provides an in-depth analysis of sales trends, customer behavior, and profitability. Businesses can leverage this data to improve their marketing strategies, optimize pricing, and enhance customer retention. Future improvements can include predictive analytics for forecasting sales and AI-powered recommendations for targeted marketing campaigns.

Developed Using: Power BI | DAX | Data Analytics

