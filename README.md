📊 Project Overview

This project is a professional **Business Performance Dashboard** built with **Microsoft Power BI** to provide a clear overview of sales performance, customer activity, retention, customer value, and business growth.

The dashboard transforms raw business data into interactive KPIs and visual insights that help users monitor performance and compare current results with previous periods.

---

🎯 Project Objectives

The main objectives of the dashboard are to:

- Monitor overall sales performance.
- Track customer activity and growth.
- Analyze customer retention and churn.
- Measure customer value and purchasing behavior.
- Compare current performance with previous periods.
- Identify monthly and seasonal sales trends.
- Provide an interactive executive-level overview of business performance.

---

 🗂️ Dashboard Sections

The dashboard covers the following analytical areas:

1. Sales Performance
- Total Sales
- MTD Sales
- QTD Sales
- YTD Sales
- Previous YTD (PYTD)
- YOY Growth
- MOM Growth
- 4-Month Rolling Sales

2. Customer Activity
- Active Customers
- Previous Month Active Customers
- Customer Growth Rate

3. Retention & Churn
- Churn Rate
- Customer Growth Rate

4. Customer Value
- Average Customer Lifespan (ACL)
- Average Purchase Frequency (APF)
- Average Purchase Value (APV)
- Average Revenue Per Customer (ARPC)
- Customer Lifetime Value (CLV)

5. Growth & Trend Analysis
- YOY Sales Growth
- MOM Sales Growth
- Monthly Sales Trend
- 4-Month Rolling Sales Trend
- Previous Year comparisons

---

🔄 Data Preparation Workflow

The project follows a structured data preparation process:

Raw Data → Data Profiling → Cleaning → Transformation → Normalization → Data Modeling → DAX Measures → Dashboard**

1. Data Collection
The source data is imported into Power BI for analysis.

2. Data Profiling
The data is reviewed to understand:
- Columns and data types
- Missing values
- Duplicate records
- Invalid values
- Relationships between business entities
- Date fields and transaction fields

3. Data Cleaning
Power Query is used to:
- Remove unnecessary columns.
- Handle missing and null values.
- Remove duplicate records where appropriate.
- Correct data types.
- Standardize values and formats.
- Validate dates and numeric fields.

4. Transformation & Normalization
The data is transformed into an analytical structure that separates business entities and transaction information.

Typical dimensions include:
- Customer
- Product
- Date
- Other relevant business dimensions

The transactional data is kept as the central fact table.

5. Data Modeling
A structured relational model is created in Power BI, following a **star-schema approach** where possible.

The model separates:
- Fact tables:transactional/business events.
- Dimension tables:descriptive attributes used for filtering and analysis.

A dedicated Date dimension is used for time intelligence calculations.

---

🧮 DAX Measures

The dashboard uses DAX measures for KPI calculations and time-based analysis.

Main Measures

text
[Total Sales]
[Total Order]
[Active Customers]
[Prev-Month Active Customers]
[Churn Rate]
[Customer Growth Rate]
[PYTD]
[YOY Growth]
[MOM Growth]
[MTD Sales]
[QTD]
[YTD]
[4-Month Rolling Sales]
[ACL (Months)]
[APF]
[APV]
[ARPC]
[CLV]

The existing DAX measure names and calculation logic are preserved. The dashboard design focuses on presenting these measures clearly through KPI cards and interactive visuals.

📈 Time Intelligence

The dashboard uses a dedicated Date table to support period comparisons and time-based calculations such as:

Month-to-Date (MTD)
Quarter-to-Date (QTD)
Year-to-Date (YTD)
Previous Year-to-Date (PYTD)
Year-over-Year (YOY)
Month-over-Month (MOM)
Rolling-period analysis

Example:

PYTD =
CALCULATE(
    [CYTD],
    SAMEPERIODLASTYEAR(Dim_date[Date])
)
🎨 Dashboard Design

The dashboard uses a modern dark professional theme designed for executive reporting.

Design Characteristics
Dark teal/green background
High-contrast KPI cards
Turquoise accent borders
Green positive-growth indicators
Red negative-growth indicators
Clear section headers
Consistent spacing and alignment
Interactive slicers
SVG-based KPI cards for custom visual design
Main Color Palette
Element	Color
Background	#071317
Card	#111A20
Header	#063B36
Border	#21404A
Primary Green	#32D583
Bright Turquoise	#00E6D2
Main Text	#F5F7FA
Secondary Text	#9AAAB5
Muted Text	#71838E
Negative Growth	#F04438
🖼️ Custom SVG KPI Cards

Custom SVG measures are used to create a more flexible and professional KPI-card design than standard Power BI cards.

The SVG cards can display:

KPI titles
Main values
Previous-period values
Growth percentages
Trend indicators
Section icons
Custom borders
Custom headers
Consistent dashboard branding

The SVG visuals are designed to work with the existing DAX measures without changing their underlying business logic.

🎛️ Interactivity

The dashboard includes interactive filtering to allow users to analyze the business from different time periods.

Examples include:

Year selection
Month filtering
KPI interaction
Cross-filtering between visuals
Dynamic KPI updates

The Date slicer/filter controls the time period shown across the dashboard.

📊 Main Visuals

The dashboard includes visualizations such as:

KPI cards
Sales trend line chart
Rolling sales trend
Customer KPI cards
Retention & churn KPIs
Customer value KPIs
Growth indicators
Time-period comparison cards
Interactive slicers
🔍 Business Questions Answered

The dashboard helps answer questions such as:

What are the current total sales?
How are sales performing compared with the previous year?
How are sales changing month over month?
What are the current MTD, QTD, and YTD sales?
How many active customers do we have?
How has the active customer base changed?
What is the current churn rate?
What is the customer growth rate?
How frequently do customers purchase?
What is the average purchase value?
How much revenue does each customer generate?
What is the estimated customer lifetime value?
What is the current monthly sales trend?
Is current performance improving compared with previous periods?
🛠️ Tools & Technologies
Microsoft Power BI
Power Query
DAX
Data Modeling
SVG
Star Schema
Time Intelligence
🚀 Project Workflow
1. Import Raw Data
        ↓
2. Profile the Data
        ↓
3. Clean the Data
        ↓
4. Transform & Normalize
        ↓
5. Build Data Model
        ↓
6. Create Date Dimension
        ↓
7. Create DAX Measures
        ↓
8. Build KPI Cards
        ↓
9. Build Charts & Slicers
        ↓
10. Apply Dashboard Theme
        ↓
11. Validate KPIs
        ↓
12. Final Dashboard
✅ Data Validation

Before finalizing the dashboard, KPI results should be validated against the underlying data.

Validation areas include:

Total sales reconciliation
Order count reconciliation
Customer count validation
Date filtering validation
Previous-period comparison validation
YOY and MOM calculation validation
Churn calculation validation
Customer value KPI validation
📁 Recommended Project Structure
Business-Performance-Dashboard/
│
├── README.md
├── PowerBI/
│   └── Business_Performance_Dashboard.pbix
│
├── Data/
│   └── Source_Data/
│
├── Documentation/
│   └── Dashboard_Documentation.pdf
│
└── Screenshots/
    └── Dashboard.png
📌 Key Takeaway

This project demonstrates an end-to-end Power BI workflow, starting from raw business data and progressing through data cleaning, transformation, normalization, data modeling, DAX development, time intelligence, interactive visualization, and professional dashboard design.

The final dashboard provides a centralized view of sales, customers, retention, customer value, and growth, making complex business data easier to understand and monitor.

👤 Author - **Sameh Mohamed Elaraby** 

Business Performance Dashboard – Power BI Project

Built using Microsoft Power BI, Power Query, DAX, Data Modeling, and SVG-based custom visuals.


path = Path("/mnt/data/README.md")
path.write_text(readme, encoding="utf-8")
print(f"Created: {path}")
