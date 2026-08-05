# Adventure Works Sales Analytics Dashboard
# About this project
This is a Power BI dashboard I built using the Adventure Works dataset as part of my Master of Data Analytics coursework/portfolio. I wanted to go beyond a single-page dashboard and actually practice the full workflow — cleaning data in Power Query, writing DAX measures, fixing a few tricky bugs along the way, and putting together something that tells a real business story across multiple pages instead of just one chart-dump.

The dashboard covers three areas: an executive-level overview, a deeper look at sales performance, and a customer-focused page.

## Dashboard Preview 
## Executive Dashboard
<img width="1131" height="768" alt="Page 1 Executive Dashboard" src="https://github.com/user-attachments/assets/3b2ea3e2-dc5c-422f-83e0-37ea13c22107" />
## Sales Performance
<img width="1330" height="769" alt="Page 2 Sales Performance" src="https://github.com/user-attachments/assets/712c19e9-dd9f-4ff9-a8f1-807a4f4083cb" />
## Customer Insights
<img width="1399" height="732" alt="Page 3 Customer Insights" src="https://github.com/user-attachments/assets/7a1414a7-9fae-4e52-8790-0fa21151fd49" />
## Tools Used

- Power BI Desktop
- Power Query (data cleaning, column extraction)
- DAX (measures and calculated columns)
- Adventure Works dataset (sales, product, customer, reseller, and date tables)
  ## Technologies

- Power BI Desktop
- Power Query
- DAX
- Data Modeling
- Star Schema
- KPI Design
- Interactive Dashboards
- Business Intelligence Reporting

## Data Model

The dashboard follows a star schema consisting of:

Fact Tables
- Sales
- Sales Order

Dimension Tables
- Customer
- Product
- Date
- Sales Territory
- Reseller

Relationships were optimized to ensure accurate filtering across all report pages.

## Key Features

- Interactive slicers
- Dynamic KPI cards
- Drill-down capability
- Cross-filtering visuals
- Customer segmentation
- Multi-page dashboard

## Business Objectives

This dashboard answers business questions such as:

- Which products generate the highest revenue?
- Which territories perform best?
- Which sales channel contributes the most?
- Who are the top customers?
- How are customers distributed across regions?
- How is the customer base segmented?

## Dashboard pages
## 1. Executive Dashboard

The high-level summary page. Six KPI cards up top (Total Sales, Profit Margin %, Total Profit, Total Orders, Total Products, Total Customers), then:

Sales by Month (trend line)
Sales by Category
Sales by Country (treemap)
Top 10 Products by Sales
Profit by Country
Slicers for Fiscal Year, Country, Category, and Reseller

## 2. Sales Performance

This page digs into product and channel-level detail:

Sales by Subcategory and Category
Top 10 Products by Profit
Sales by Territory (treemap)
Sales by Channel — Reseller vs. Direct (donut)
Sales vs. Profit (scatter plot, one dot per product)
Monthly Sales Heatmap (fiscal year × month grid)

## 3. Customer Insights

Focused on individual customer behavior:

Top 10 Customers by Sales
Top 10 Customers by Order Count
Customer Sales by Country-Region (treemap)
Customer Count by Country-Region
Average Sale per Line Item by Country-Region
Customer Segmentation by Value (Low / Medium / High, donut)
What I actually found in the data

## Sample DAX Measures

- Total Sales
- Total Profit
- Profit Margin %
- Total Customers
- Total Orders
- Customer Sales
- Average Sale per Line Item
- Reseller Sales
- Direct Sales

A few honest takeaways from building this, not just generic BI-speak:

Bikes account for approximately 86% of total revenue, making the business highly dependent on a single product category.

Resellers, not direct customers, drive most of the business. About 73% of total revenue comes through the reseller network, and only 27% is direct-to-customer. I didn't expect the split to be that lopsided until I built the channel chart.

The United States contributes the largest share of total sales, significantly outperforming all other regions and generating approximately five times more revenue than Canada, the second-highest performing country.

Most individual customers are low-value. When I built the segmentation chart, about 68% of customers fell into the "Low Value" tier and only a small slice landed in "High Value." So a lot of the customer base is occasional/one-off buyers rather than repeat high spenders — that's a different story than I assumed going in.

One thing worth calling out honestly: the dataset tracks order line items, not full customer orders (there's no order-header-level key, only a line-item key). So metrics like "Average Sale per Line Item" reflect that granularity — they're not the same as a true "average order value" you'd get from a dataset with a proper order table.

## Technical Skills Demonstrated
- Data modeling and relationships (including tracking down a broken one-to-many relationship that was silently returning wrong numbers)
- Power Query cleanup (removing duplicates, extracting month/quarter/year fields)
- DAX from basic SUM/DISTINCTCOUNT measures up to CALCULATE with KEEPFILTERS for correct row-level filtering
-KPI and dashboard layout design
Choosing the right chart type for the question being asked (bar vs. treemap vs. scatter vs. heatmap vs. donut) instead of defaulting to bar charts everywhere

## Possible future improvements
- Add a forecasting page for future sales trends
- Add drill-through pages for individual product/customer detail
- Connect to a live SQL Server source instead of a static file
- Publish to Power BI Service for a shareable live link
## How to Open

1. Download the repository.
2. Open the PBIX file using Power BI Desktop.
3. Refresh the dataset if necessary.

## Conclusion

This project demonstrates an end-to-end Power BI workflow, including data preparation, data modeling, DAX development, dashboard design, and business insight generation. It showcases the ability to transform transactional sales data into interactive dashboards that support data-driven decision making.

Adventure-Works-Sales-Analytics/
│
├── Adventure Works Sales Analytics Dashboard.pbix
├── README.md
└── Screenshots/
    ├── Executive Dashboard.png
    ├── Sales Performance.png
    └── Customer Insights.png

## Author

Neerupama Dwarapu Master of Data Analytics Student, University of Niagara Falls Canada GitHub: github.com/DwarapuNeerupama

## License

This project is for educational and portfolio purposes.
