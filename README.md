# Business-Insights-360

AtliQ Hardware is growing rapidly in recent years and has decided to implement data analytics using Power BI to surpass its competitors and make data-driven decisions. This project aims to answer stakeholder questions in all aspects, including finance, sales, marketing, and supply chain.

[[Live Report Link](#)](https://app.powerbi.com/groups/70a5283e-123c-4f1c-8991-ce373ae8b08f/reports/eaeec658-f3a9-435e-bafe-2e1acdf4d75e/a8e3066ec645e602725d?experience=power-bi)

### Tech Stack
- **SQL**
- **Power BI Desktop**
- **Excel**
- **DAX language**
- **DAX Studio** (for optimizing the report)

### Power BI Techniques Learned
- Questions to ask before starting the project
- Creating calculated columns
- Creating measures using DAX language
- Data modeling
- Using Bookmarks to switch between visuals
- Page navigation with buttons
- Using the divide function to prevent zero division errors
- Creating a date table using M language
- Dynamic titles based on applied filters
- Using KPI indicators
- Conditional formatting in visuals using icons or background color
- Data validation techniques

### Power BI Services
- Publishing reports to Power BI services
- Setting up personal gateway for auto-refresh of data
- Power BI App creation
- Collaboration, workspace, access permissions in Power BI services

### GitHub
- Uploading large files using GitHub LFS
- Tracking specific file extensions for LFS

### Business Terms
- **Gross price**
- **Pre-invoice deductions**
- **Post-invoice deductions**
- **Net invoice sale**
- **Gross margin**
- **Net sales**
- **Net profit**
- **COGS** - Cost of Goods Sold
- **YTD** - Year to Date
- **YTG** - Year to Go
- **Direct, Retailer, Distributors, Consumer**

## Company Background
AtliQ Hardware has grown significantly in recent years, expanding globally. The company sells computers and accessories through three channels:

- Retailers
- Direct
- Distributors

Recently, the company faced a significant loss by opening a store in America based on surveys, intuition, and some Excel analysis. Meanwhile, competitors have robust analytics teams for data-driven decisions. Hence, AtliQ Hardware decided to build its analytics team for better insights and future decisions.

## Project Kick-Off

### Questions to Ask Before Starting the Dashboard
- What is the objective of building this Power BI dashboard?
- How will the success of this project be measured?
- What is the project deadline?
- Are stakeholders expecting a preview before the actual release?
- What are the stakeholders' hopes for this project?
- What fears do stakeholders have regarding this dashboard?
- Who will use this dashboard and for what purpose?
- What are the stakeholders' expectations by the project's completion?
- What can go wrong during this project?
- What resources/data are needed to build this dashboard?
- Are there any inputs from stakeholders regarding the dashboard design and views?

After the project kick-off meetings, the data engineering team provided the necessary data for the data analytics team. Let's explore the datasets.

## Dataset Understanding

Understanding the available data is crucial for effective analysis. Before starting the analysis, it's important to grasp the available data.

### Dimension Tables
- **dim_customer**: Static data like customer and product details
  - 27 distinct markets (e.g., India, USA, Spain)
  - 75 distinct customers across the market
  - 2 types of platforms: Brick & Mortar (offline) and E-commerce (online)
  - Three channels: Retailer, Direct, Distributors

- **dim_market**
  - 27 distinct markets (e.g., India, USA, Spain)
  - 7 sub-zones
  - 4 regions: APAC, EU, nan, LATAM

- **dim_product**
  - Divisions: P & A (Peripherals & Accessories), PC (Notebook, Desktop), N & S (Networking, Storage)
  - 14 different categories (e.g., Internal HDD, keyboard)
  - Various product variants

### Fact Tables
- **fact_forecast_monthly**
  - Used to forecast customer needs, aiding in higher satisfaction and reduced storage costs
  - Denormalized for analytical purposes, with all dates replaced by the month's start date
  - Contains forecast quantity

- **fact_sales_monthly**
  - Similar to fact_forecast_monthly but contains sold quantity instead of forecast value

- **gdb056**
  - **freight_cost**: Travel and other costs for each market with fiscal year
  - **gross_price**: Gross prices with product codes
  - **manufacturing_cost**: Manufacturing costs with product codes and years
  - **pre_invoice_deductions**: Pre-invoice deduction percentages for each customer with years
  - **post_invoice_deductions**: Post-invoice deductions and other details

## Importing Data into Power BI
- Import datasets from MySQL to Power BI by providing database access credentials.
