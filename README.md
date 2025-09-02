# Adidas-Sales-Performance-Dashboard

<img width="2434" height="1361" alt="image" src="https://github.com/user-attachments/assets/14f6d2d4-3003-4543-85f2-d66fe215c8f9" />

This dashboard analyses Adidas retail performance across channels, products, retailers and geographies, with a timeline spanning January 2020 to July 2021. Core headline KPIs show 2.0M orders, $900M revenue, $332M profit and $568M cost, giving a ~36.9% gross margin.
Dashboard view: https://app.powerbi.com/view?r=eyJrIjoiMTRiYzk5OTktNzZlOC00MTBlLThkYTYtZDNlODIyMDAxYTYxIiwidCI6ImJlODMyOWE3LTcyMTgtNDlhMy05YWMxLWQ3Yjk1NDU2M2YzOSIsImMiOjEwfQ%3D%3D

# Project Overview

This project analyses supply chain and sales operations for a retail business from 2014 to 2017. It tracks delivery time, on-time performance, returns, product discount impact, and regional profitability to surface operational bottlenecks and growth opportunities.

# Dataset Structure:
Transactional sales with fields and slicers for:

Date (Start of Month), Region, Product (page-level slicers).

Retailer (e.g., West Gear, Foot Locker, Sports Direct, Kohl’s, Amazon, Walmart).

Geography (Revenue by State visual).

Sales Method (In-store, Outlet, Online) with mix shares visualised.

Product Matrix with #Units and Revenue by product groups.
 
# Steps to Reproduce

Connect & model: Load Orders/Products/Retailers/Geography/Methods; add a Date table linked by Order/Invoice Date.

Core measures:

Revenue = SUM(Sales[Revenue]), Cost = SUM(Sales[Cost]), Profit = [Revenue]-[Cost]

Orders = DISTINCTCOUNT(Sales[OrderID]), Profit Margin = DIVIDE([Profit],[Revenue])

# KPI & Derived Metrics

Totals: Revenue $900M, Profit $332M, Cost $568M, Orders 2.0M.

Profit Margin ~36.9%, AOV ~ $450, Profit/Order ~ $166, Cost/Order ~ $284.

Channel Mix (rev share): In-store ~40%, Outlet ~33%, Online ~28%.

Retailer Contribution (of $900M): West Gear $243M (~27%), Foot Locker $220M (~24%), Sports Direct $182M (~20%), Kohl’s $102M (~11%), Amazon $78M (~9%), Walmart $75M (~8%).

Indicative ASPs (Units/Revenue):

Men’s Street Footwear: 593,320 / $208.83M → ~$352

Men’s Athletic Footwear: 435,526 / $153.67M → ~$353

Women’s Apparel: 433,827 / $179.04M → ~$413

Women’s Street Footwear: 392,269 / $128.00M → ~$326

# Exploratory Analysis

- Business Health

Monthly revenue peaks near ~$80M; margin band ~35–45%, suggesting stable structure with headroom for mix/pricing gains.

Revenue concentration: top two retailers (West Gear + Foot Locker) ≈ 51% combined.

- Channel / Method

In-store is the largest slice (~40%); Outlet is second (~33%), Online (~28%).

Method time-series supports seasonal read-outs and promo impact checks (e.g., Outlet spikes).

- Product

Revenue leaders: Men’s Street Footwear ($208.8M), Women’s Apparel ($179.0M), Men’s Athletic Footwear ($153.7M), Women’s Street Footwear ($128.0M).

Product margin bands span ~20–60% → discount policy and mix materially drive profitability.

ASP dispersion (e.g., ~$413 vs. ~$326) implies different elasticity by category.

- Geography & Retailers

State-level revenue highlights under-penetrated areas for each key account.

Priority partners: West Gear and Foot Locker (together ~51% of revenue).

- Insights & Recommendations

Key accounts: Deepen JBP with West Gear & Foot Locker—seasonal exclusives in Men’s Street/Athletic Footwear, end-cap commitments, weekly sell-through & service-level scorecards.

Channel mix: Protect In-store while scaling online profitably (test free-ship thresholds, bundles). Track the contribution profit by channel monthly.

Assortment & pricing: Footwear dominates—align inventory to winners, manage ASP ladders, tighten discounts where margins are thin.

Reporting hygiene: Fix mixed currency across visuals to prevent misreads.

Next analytics: Add Retailer×Region and Method×Region matrices; extend MoM/YoY on margin to separate mix vs. pricing vs. cost effects.

# Summary

From 2020–2021, the business delivered $900M revenue and $332M profit on 2.0M orders (~36.9% margin). Performance is retailer-concentrated and store-weighted; footwear is the engine with wide margin variance. Biggest levers: strengthen top-account programs, grow Online without margin drag, refine price/discount ladders, and standardize currency for clean decision-making.
