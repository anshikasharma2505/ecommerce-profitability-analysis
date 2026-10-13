# Project Methodology

## 1. Project Objective

The objective of this project is to analyze e-commerce profitability, product performance, marketing-channel activity, website sessions, and refunds using Microsoft Excel, Power Query, and Power BI.

## 2. Data Source

The project uses the Maven Fuzzy Factory e-commerce dataset provided by Maven Analytics.

The data includes:
- Orders
- Order items
- Products
- Order item refunds
- Website sessions
- Website pageviews

Source: https://mavenanalytics.io/data-playground/toy-store-e-commerce-database

## 3. Data Preparation

Power Query was used to import and prepare the source tables. The tables were reviewed and organized for analysis, and relationships were established using the available identifiers.

A separate product-category mapping was created to group the four products for comparison. These categories are analyst-defined and are not official categories supplied by the source dataset.

Marketing channels were classified using available session source and referrer fields. These classifications are rule-based and should not be interpreted as verified advertising attribution.

## 4. Data Model

The Power BI model connects the relevant tables using identifiers such as:
- `order_id`
- `order_item_id`
- `product_id`
- `website_session_id`

The relationships support product-level sales analysis, website-session analysis, and refund reporting. Refunds are connected to order items through `order_item_id`.

## 5. KPI Definitions

### Total Revenue
The sum of selling prices recorded for order items.

### Total COGS
The sum of the cost of goods sold recorded for order items.

### Gross Profit
Total Revenue minus Total COGS.

### Gross Profit Margin
Gross Profit divided by Total Revenue, expressed as a percentage.

### Total Refunds
The sum of recorded refund amounts.

### Overall Refund Rate
Total Refunds divided by Total Revenue, expressed as a percentage. This is an overall metric; monthly refund rates should not be interpreted unless the revenue and refund dates are aligned correctly.

## 6. Dashboard Design

### Profitability Overview
Shows revenue, COGS, gross profit, gross profit margin, revenue by product, and gross profit by product.

### Marketing Channel Performance
Shows revenue by marketing channel, website sessions by channel, and website sessions over time. Date and channel slicers allow interactive exploration.

### Refund Analysis
Shows total refunds, overall refund rate, refund amounts by product, and refund trends over time.

## 7. Assumptions and Limitations

- Product categories were created for analytical grouping.
- Marketing-channel categories are based on available source and referrer fields.
- Marketing expenditure is not available; therefore, advertising ROI cannot be calculated.
- Gross profit excludes refunds, marketing costs, shipping, and other operating expenses. It should not be interpreted as net profit.
- Refunds and orders can occur on different dates. Monthly refund amounts do not automatically provide a valid monthly refund rate.

## 8. Tools Used

- Microsoft Excel
- Power Query
- Microsoft Power BI
- DAX
- Git and GitHub
