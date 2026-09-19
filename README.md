# 📊 Business Performance Dashboard

An end-to-end **Business Intelligence and Analytics project** built with **Power BI** to analyze sales performance, customer activity, retention & churn, customer value, and business growth through an interactive executive dashboard.

**Developed by:** [Sameh Mohamed](https://github.com/samehmohamed2610)

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![Power Query](https://img.shields.io/badge/Power%20Query-217346?style=flat)
![DAX](https://img.shields.io/badge/DAX-Data%20Analysis-blue?style=flat)
![Data Modeling](https://img.shields.io/badge/Data%20Modeling-Star%20Schema-purple?style=flat)
![SVG](https://img.shields.io/badge/SVG-Custom%20Visuals-orange?style=flat)

---

## 📌 Overview

Most business dashboards focus on a single KPI or a single department. This project brings multiple business perspectives together in one interactive Power BI report.

The dashboard provides a centralized view of:

- Sales performance
- Customer activity
- Orders performance
- Retention and churn
- Customer value
- Growth trends
- Monthly and yearly comparisons
- Rolling sales performance

The project follows an end-to-end analytics workflow, starting from raw business data and continuing through data cleaning, transformation, normalization, data modeling, DAX development, visualization, and final dashboard design.

---

# ⚙️ Data Preparation & Modeling

## A. Data Profiling

The source data was reviewed before building the analytical model.

The profiling process focused on:

- Understanding available tables and columns
- Identifying data types
- Checking missing and null values
- Detecting duplicate records
- Reviewing date and transaction fields
- Understanding relationships between business entities
- Identifying fields required for KPI calculations

---

## B. Transformation and Cleaning — Power Query

Power Query was used to prepare the raw data for analysis.

| Step | What it does |
|---|---|
| Data Type Validation | Ensures numeric, text, and date fields use the correct data types |
| Missing Values | Identifies and handles blanks where required |
| Duplicate Checks | Reviews duplicate records and maintains data consistency |
| Column Filtering | Removes unnecessary fields to keep the model focused |
| Data Transformation | Reshapes and prepares source data for analytical modeling |
| Standardization | Keeps values and formats consistent across the model |

---

## C. Normalization

The raw business data was transformed into a structured analytical format.

Business entities and transactional information were separated where appropriate to support a cleaner model and more flexible analysis.

The final structure follows a **star-schema approach**, with transactional data supported by descriptive dimensions.

This structure improves:

- Filtering
- Relationships
- DAX calculations
- Time intelligence
- Dashboard performance
- Analytical flexibility

---

## D. Data Modeling

A dedicated Date dimension was used to support time-based analysis.

The model was designed to support calculations such as:

- Monthly performance
- MTD
- QTD
- YTD
- PYTD
- YOY Growth
- MOM Growth
- 4-Month Rolling Sales

---

# 📊 Dashboard Features

The report uses a dark professional theme with custom KPI cards, turquoise accents, interactive filters, and SVG-based visual elements.

## 💰 Sales Performance

Tracks the main sales KPIs and period comparisons.

Includes:

- Total Sales
- MTD Sales
- QTD Sales
- YTD Sales
- PYTD
- YOY Growth
- MOM Growth
- 4-Month Rolling Sales

The Sales Performance section provides a quick view of current performance and how it compares with previous periods.

---

## 📈 Sales Trend

A monthly sales trend visual compares:

- Total Sales
- 4-Month Rolling Sales

The rolling measure helps provide a smoother view of the underlying sales trend and reduces the impact of short-term fluctuations.

---

## 👥 Customer Activity

Monitors changes in the active customer base.

Includes:

- Active Customers
- Previous Month Active Customers
- Customer Growth Rate
- Monthly Customer Growth

This section helps identify whether customer activity is increasing or declining over time.

---

## 🛒 Orders Performance

Provides a view of overall transaction activity through:

- Total Orders
- Order Volume

Orders are analyzed alongside sales performance to provide additional context around business activity.

---

## 🔄 Retention & Churn

Analyzes customer retention and churn behavior.

Includes:

- Churn Rate
- Customer Growth
- Customer Retention

Dynamic growth indicators highlight positive and negative changes in customer activity.

---

## 💎 Customer Value

Measures the economic value and purchasing behavior of customers.

Key metrics include:

| KPI | Description |
|---|---|
| ACL | Average Customer Lifespan |
| APF | Average Purchase Frequency |
| APV | Average Purchase Value |
| ARPC | Average Revenue Per Customer |
| CLV | Customer Lifetime Value |

These metrics provide a deeper understanding of customer contribution and long-term value.

---

# 🧮 DAX & Time Intelligence

DAX was used to create dynamic KPIs and period-based calculations.

Main measures include:

```text
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
```

The measures dynamically respond to the selected date and dashboard filters.

Example time-intelligence calculation:

```DAX
PYTD =
CALCULATE(
    [CYTD],
    SAMEPERIODLASTYEAR(Dim_date[Date])
)
```

---

# 🎨 Dashboard Design

The dashboard was designed with a modern dark executive-style interface.

### Design Features

- Dark teal background
- Turquoise borders and accents
- Green positive-growth indicators
- Red negative-growth indicators
- Custom SVG KPI cards
- Structured section headers
- Interactive slicers
- Consistent spacing and alignment
- Clear KPI hierarchy
- Responsive visual storytelling

Custom SVG visuals were used to create flexible KPI cards while keeping the existing DAX measures and business logic intact.

---

# 🛠️ Tools and Technologies

| Tool / Technology | Purpose |
|---|---|
| **Power BI** | Data modeling, visualization, and dashboard development |
| **Power Query** | Data cleaning and transformation |
| **DAX** | KPI calculations and time intelligence |
| **Star Schema** | Analytical data modeling |
| **Date Dimension** | Time-based analysis |
| **SVG** | Custom KPI card visuals |
| **Data Visualization** | Business insight presentation |

---

# 📂 Repository Structure

```text
Business-Performance-Dashboard/
│
├── screenshots/
│   ├── dashboard-overview.png
│   ├── dashboard-filtered-1.png
│   └── dashboard-filtered-2.png
│
├── Business_Performance_Dashboard.pbix
│
├── README.md
│
└── Documentation/
    └── Dashboard_Documentation.pdf
```

---

# ▶️ How to Use

### 1. Clone the repository

```bash
git clone https://github.com/samehmohamed2610/Business-Performance-Dashboard.git
```

### 2. Install Power BI Desktop

Download and install **Power BI Desktop**.

### 3. Open the PBIX file

Open:

```text
Business_Performance_Dashboard.pbix
```

### 4. Refresh the data

If the source data is included separately, update the data-source path from:

**Home → Transform data → Data source settings**

Then refresh the report.

### 5. Explore the dashboard

Use the available slicers and filters to analyze different periods and compare business performance dynamically.

> **Note:** Dashboard values may change depending on the selected filters and the underlying source data.

---

# 💡 Business Questions Answered

The dashboard helps answer questions such as:

- How are total sales performing?
- How does current sales compare with previous periods?
- Is sales growth positive or negative?
- How many active customers do we currently have?
- How is the customer base changing?
- What is the current churn rate?
- How many orders were generated?
- What is the average purchase value?
- How frequently do customers purchase?
- How much revenue is generated per customer?
- What is the estimated customer lifetime value?
- What is the monthly sales trend?
- How does rolling sales performance compare with monthly sales?

---

# 🚀 Future Improvements

### 🔮 Predictive Sales Forecasting
Develop predictive models to estimate future sales and identify expected growth patterns.

### 👤 Customer Churn Prediction
Use machine-learning models to identify customers with a higher probability of churn.

### 🎯 Customer Segmentation
Apply RFM analysis and clustering to group customers according to purchasing behavior and value.

### ⚡ Automated KPI Alerts
Integrate Power BI with Power Automate to trigger notifications when important KPIs reach predefined thresholds.

### 🧪 What-If Analysis
Introduce scenario parameters to simulate changes in sales, customer growth, retention, and other business drivers.

### 💎 Advanced CLV Forecasting
Extend the current CLV analysis with predictive customer behavior and long-term revenue forecasting.

### 🔎 Drillthrough Analysis
Add deeper drillthrough pages for customer, product, order, and transaction-level analysis.

---

# 📌 Final Outcome

The final solution provides a centralized **Business Performance Dashboard** that combines sales, customers, orders, retention, customer value, and growth analysis in one interactive reporting environment.

The project demonstrates an end-to-end Power BI workflow:

**Data Preparation → Data Modeling → DAX → Time Intelligence → Visualization → Custom SVG Design → Interactive Dashboard**

The result is a professional analytical solution that transforms raw business data into clear, interactive, and actionable business insights.

---

# 👤 Author

**Sameh Mohamed**

Power BI & Data Analytics

🔗 **GitHub:** [@samehmohamed2610](https://github.com/samehmohamed2610)

⭐ If you find this project useful, feel free to explore the repository and give it a star.
