Demand Forecasting & Supply Planning Model
A simple, formula-driven Excel model that forecasts product demand and plans purchase/stock
decisions around it — built for the Intern, Materials role at Eaton's Global Supply Chain
Center of Excellence (Pune, India).
Sample data covers 5 electrical products (circuit breakers, contactors, relays, terminal blocks,
switch disconnectors) over 24 months. No ML, no advanced statistics — just the same simple,
explainable formulas a real materials/supply planning team uses day to day.
📊 Key Results
Metric
Result
Average Forecast Accuracy (MAPE-based)
93.6%
Products flagged for reorder
2 of 5 (40%)
Average Inventory Turnover
7.4x / year
Formulas in the workbook
700+
Sheets
7

Raw ERP-style export (wide, messy)
        │  Power Query: remove columns, unpivot
        ▼
Clean Demand History (long format, 24 months x 5 products)
        │  Moving Average + Weighted Moving Average
        ▼
Demand Forecast + Forecast Accuracy (MAPE)
        │  Safety Stock, Reorder Point, EOQ
        ▼
Supply Plan per product
        │  Order-up-to (s,S) policy
        ▼
3-Month Purchase Plan
        │
        ▼
KPI Dashboard (charts, alerts, live SKU lookup)
Tools & Skills Used
Excel Tables — auto filter/sort, structured references
XLOOKUP — dynamic, name-based lookups across sheets
Power Query — cleaning and unpivoting raw wide-format data into analysis-ready rows
Conditional Formatting — automatic red/green stock-status alerts, data bars
Data Validation — dropdown-restricted SKU picker
Core SCM formulas — Moving Average, Weighted Moving Average, MAPE, Safety Stock (max-min
method), Reorder Point, Economic Order Quantity (EOQ), Inventory Turnover
Formula Reference
Concept
Formula (plain English)
Moving Average Forecast
Average of the last 3 months' actual demand
Weighted Moving Average
(oldest × 1 + middle × 2 + newest × 3) / 6
Forecast Accuracy %
1 − MAPE (average absolute % error vs. actual)
Safety Stock
(Max month demand − Avg month demand) × Lead Time
Reorder Point
(Avg month demand × Lead Time) + Safety Stock
EOQ
√( 2 × Annual Demand × Ordering Cost ÷ Holding Cost )
Inventory Turnover
Annual Demand ÷ Current Stock
⚠️ Assumptions
All demand history, lead times, ordering costs, holding costs, and current stock levels are
illustrative sample data, generated for this project — not real Eaton figures. Every
assumed input cell is shown in blue in the workbook, with a comment explaining what it
represents, so it's easy to swap in real data.
👤 About
Built by [Sandeep Kumar Sharma] as a self-directed practice project to demonstrate applied Excel and
supply-chain planning skills relevant to a Materials/Supply Chain.
