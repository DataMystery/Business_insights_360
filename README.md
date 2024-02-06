# Business_insights_360
# Project overview

AtliQ Hardware is undergoing rapid growth in recent years, leading them to initiate the implementation of data analytics using Power BI for the first time. The primary objective is to surpass competitors in the market and streamline data-driven decision-making processes. This project is dedicated to delivering extensive insights to stakeholders across diverse domains, encompassing finance, sales, marketing, and supply chain management.

This project was meticulously crafted utilizing the data available from Codebasics, and through it, a comprehensive Power BI report was generated. 

## Tech Stack

- SQL
- Power BI Desktop
- Excel
- DAX language
- Project charter file

## Power BI Techniques Learned

- What are all the questions should be asked before staring the project
- Creating calculated columns
- creating measure using DAX language
- Data modeling
- Using Bookmarks to switch between two visuals
- Page navigation with buttons
- Using divide function to prevent zero division errors
- creating date table using m language
- Dynamic titles based on the applied filters
- Using KPI indicators
- Conditional formatting the values in visuals using icons or background color
- Data validation techniques
- PowerBi services
- Publishing reports to PowerBi services
- Setting up personal gateway to set up the auto refresh of data
- PowerBi App creation
- Collaboration, workspace, access permissions in PowerBi services
- And more 🧐

## Business related terms

- Gross price
- Pre-invoice deductions
- Post-Invoice deductions
- Net Invoice sale
- Gross Margin
- Net sales
- Net profit
- COGC - cost of goods sold
- YTD - Year to Date
- YTG - Year to Go
- Direct
- Retailer
- Distributors
- Consumer

## Company’s back ground

"AtliQ Hardware is a rapidly expanding global company specializing in the sale of computers and computer accessories. Operating through three primary channels:-
- Retailers
- Direct sales
- Distributors
the company has established a significant presence in the market."


In response to unexpected losses from opening a store in America, coupled with competitors boasting robust analytics teams, AltiQ Hardware recognizes the imperative to establish its own analytics team. This strategic move aims to leverage data-driven insights for enhanced decision-making and industry survival. 

During the project kick-off session, the focus will be on clarifying the project's purpose, defining its objectives, establishing scope, identifying key stakeholders, setting a timeline, allocating resources, addressing potential risks, and creating a communication plan. This comprehensive approach ensures a clear understanding of the project's goals and sets the foundation for successful implementation and industry resilience.

## Questions to ask before starting with dashboard
- What is the objective of building this PowerBi dashboard?
- In what terms the success of this project will be measured?
- What will be time dead-line of the project?
- do the stakeholders expecting pre-view before the actual release?
- What are all the hopes stakeholders have out of this project?
- what are all fears the stakeholder have in terms of building this dashboard?
- Who are all will be using this dashboard and for what purpose?
- what are all expectation the stakeholders have, by the completion of this project?
- What can go wrong while building this project?
- what are all the resources/ data needed to build this dashboard?
- is there any inputs from stakeholders in terms of design and views of the dashboard?

  
With the collected data from Codebasics in hand, we're ready to initiate the data cleaning and transformation process in Power BI. This crucial step involves preparing the data for analysis by addressing inconsistencies, errors, and missing values. By utilizing Power BI's robust capabilities, we'll refine the data into a usable format that aligns with our analytical goals. Let's begin this essential phase to ensure our subsequent analysis is based on accurate and reliable data.🤠

## Dataset Understanding
Understanding the available data is crucial before analysis. We'll explore the dataset to identify key variables, assess data quality, and determine the best analytical approaches. This upfront understanding ensures accurate insights and actionable outcomes. Let's start by examining the dataset thoroughly

Dimension table : It will have the static data like details of customer and products

Fact table : It will have the data about the transactions

* gdb041:
   * dim_customer
      + 27 distinct markets (ex India, USA, spain)
      + 75 distinct customers thorough out the market
      + 2 types of platforms
         + Brick & Motors - Physical/offline store
         + E-commerce - Online Store (Amazon, flipkart)
      + Three channels
         + Retailer
         + Direct
         + Distributors
   * dim_market
     + 27 distinct markets (ex India, USA, spain)
     + 7 sub-zones
     + 4 regions
        + APAC
        + EU
        + NaN
        + LATAM
   * dim_product
     + Divisions
        + P & A
        + Peripherals
        + Accessories
     + PC
       + Notebook
       + Desktop
     + N & S
       + Networking
       + Storage
* There are 14 different categories, Like Internal HDD, keyboard
* There are different variants available for the same product
     * fact_forecast_monthly
        + This table is used to forecast the customer’s need in advance, which can help in
          + Higher customer satisfaction
          + Reduced cost in warehouses for storage purpose
        + The table is denormalized by data engineering team, as it is a data warehouse which is aimed to be used for analytical work.
        + All the date of the month will be replaced by the start date of the month
        + It will have all the column names and in the end it will have the forecast quantity need of the customer
     * fact_sales_monthly
       + This table is more or less is same as fact_forecase_monthly table, but the last column has the value of sold quantity instead of forecast value.

* gdb056
  * freight_cost
     + This table has details of travel cost and other cost for each market with fiscal year
  * gross_price
    + Has the details of gross prices with product code
  * manufacturing_cost
    + Has the details of manufacturing cost with product code with year
  * Pre_invoice_dedutions
    + Has the details of pre invoice deductions percentage for each cutomer with year
  * Post_invoice_deductions
    + Post invoice deductions and other deductions details
   
## Importing data into PowerBi

To import datasets from MySQL to Power BI, we'll need to provide the necessary database access credentials.Once these credentials are provided, Power BI can establish a connection to the MySQL database and import the datasets directly into our Power BI 

## Data  Model


* Data modeling is fundamental, acting as the cornerstone of reports. Every visualization is constructed based on this framework. Substandard data modeling directly impacts the overall performance of the report.
+ In this report, I have implemented the snowflake schema, which is visually represented in the figure below:

![https://github.com/DataMystery/Business_insights_360/blob/main/report_insights/Data%20Model.jpg!](https://github.com/DataMystery/Business_insights_360/blob/main/report_insights/Data%20Model.jpg)

## Power Bi report designing

## Home Page
Within the Home view, users will find buttons for accessing various views. Clicking on a specific button will direct the user to the corresponding view page.
+ Info
+ Finance View
+ Sales View
+ Marketing View
+ Supply chain View
+ Executive View
+ Products
+ Support

![https://github.com/DataMystery/Business_insights_360/blob/main/report_insights/home.png!](https://github.com/DataMystery/Business_insights_360/blob/main/report_insights/home.png)

## Info

![https://github.com/DataMystery/Business_insights_360/blob/main/report_insights/info.png!](https://github.com/DataMystery/Business_insights_360/blob/main/report_insights/info.png)

## Finance view

![https://github.com/DataMystery/Business_insights_360/blob/main/report_insights/finance%20view.png!](https://github.com/DataMystery/Business_insights_360/blob/main/report_insights/finance%20view.png)

## Sales view

![https://github.com/DataMystery/Business_insights_360/blob/main/report_insights/finance%20view.png!](https://github.com/DataMystery/Business_insights_360/blob/main/report_insights/finance%20view.png)

## Marketing view

![https://github.com/DataMystery/Business_insights_360/blob/main/report_insights/marketing%20view.png!](https://github.com/DataMystery/Business_insights_360/blob/main/report_insights/marketing%20view.png)

## SupplyChain view

![https://github.com/DataMystery/Business_insights_360/blob/main/report_insights/supply%20chain%20view.png!](https://github.com/DataMystery/Business_insights_360/blob/main/report_insights/supply%20chain%20view.png)

## Executive view

![https://github.com/DataMystery/Business_insights_360/blob/main/report_insights/executive%20view.png!](https://github.com/DataMystery/Business_insights_360/blob/main/report_insights/executive%20view.png)

### For more information
 You can find the full POWER BI report by clicking this [REPORT](https://app.powerbi.com/view?r=eyJrIjoiNzBmNDkxNWYtYjcyOC00NmIxLTg2N2ItZDFiNDc3YzYyN2Q2IiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)

 ## Project Outcome
 
By leveraging this report, decisions can be made using data, while also providing insights to address numerous "why" questions in various situations.







































