# abs-store-inventory-sale-items

ABS Store Inventory and Sale Items



Project Overview

This project provides an analysis of the Alcoholic Beverage Services (ABS) in Montgomery County, Maryland, a government agency running state-controlled liquor stores. By transforming raw government data into an interactive Power BI dashboard, the project enables stakeholders to monitor stock levels, analyze pricing tiers, and identify inventory gaps across thousands of SKUs.



Data Source: https://catalog.data.gov/dataset/abs-store-inventory-and-sale-items

Format: Live JSON API

Endpoint: https://data.montgomerycountymd.gov/api/views/ib5t-5ncy/rows.json?accessType=DOWNLOAD



ETL

Implemented an ETL process to convert unstructured JSON data into a format suitable for analysis.



Additional columns added not included in JSON

1. Availability - Out of Stock / In Stock
2. Pricing Tier - Budget (<$20) to Luxury(>$1000)



Removed 1 SKU in Power BI because Code is null but daily csv unchanged:

&nbsp;	Record ID 4439

&nbsp;	Code null

&nbsp;	Category AUSTRALIAN

&nbsp;	Description PENFOLDS BIN 8 CAB/SHZ - 750ML

&nbsp;	Size 750ML

&nbsp;	Total Inventory 0

&nbsp;	Price 22.99



Features and Insights

* Interactive Slicers - Allows users to toggle between InStock and OutofStock items
* Pricing Landscape - Analyzes distribution of inventory across price points
* Inventory Health KPIs - Real-time tracking of total SKUs and stock rates
* Outlier Detection - Scatter plot correlating stock levels with unit prices to identify high-capital risk items



Tools Used

* Power BI
* Power Query
* Excel
