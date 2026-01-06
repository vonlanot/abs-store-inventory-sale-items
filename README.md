# abs-store-inventory-sale-items

ABS Store Inventory and Sale Items



Project Overview

This project provides an analysis of the Alcoholic Beverage Services (ABS) in Montgomery County, Maryland, a government agency running state-controlled liquor stores. By transforming raw government data into an interactive Power BI dashboard, the project enables stakeholders to monitor stock levels, analyze pricing tiers, and identify inventory gaps across thousands of SKUs.



This project also involves daily data collection. Once a full month of daily data is compiled, we can take a deeper look at the data.



Data Source: https://catalog.data.gov/dataset/abs-store-inventory-and-sale-items

Format: Live JSON API

Endpoint: https://data.montgomerycountymd.gov/api/views/ib5t-5ncy/rows.json?accessType=DOWNLOAD



Methodology and Data Constraints

1. Because the source data provides daily inventory snapshots without a "Units Sold" or "Purchases/Restock" column, daily sales are not accurate. What we could monitor is the daily net inventory decrease/increase.
2. The calculation represents a conservative estimate and it does not account for restocking, e.g. if an item is restocked and sold on the same day, true quantity sold may be higher.
3. Missed data collection on December 25-26, 2025. :(



ETL

Implemented an ETL process to convert unstructured JSON data into a format suitable for analysis.



Additional columns added not included in JSON

1. Availability - Out of Stock / In Stock
2. Pricing Tier - Budget (<$20) to Luxury(>$1000)



Removed 1 SKU in Power BI because Code is null but daily csv unchanged:

 	Code null

 	Category AUSTRALIAN

 	Description PENFOLDS BIN 8 CAB/SHZ - 750ML

 	Size 750ML

 	Total Inventory 0

 	Price 22.99



Features and Insights

* Interactive Slicers - Allows users to toggle between InStock and OutofStock items
* Pricing Landscape - Analyzes distribution of inventory across price points
* Inventory Health KPIs - Real-time tracking of total SKUs and stock rates
* Outlier Detection - Scatter plot correlating stock levels with unit prices to identify high-capital risk items



Tools Used

* Power BI
* Power Query
* Excel
