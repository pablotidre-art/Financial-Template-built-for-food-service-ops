# Financial Model - Intelligent Financial Management for Food Service

This repository contains a comprehensive spreadsheet-based financial ecosystem designed specifically for the operational and strategic management of food service businesses (Pizzerias). The model integrates everything from real-time inventory tracking to advanced scenario-based decision making.

## 📊 Key Features

* **Profit & Loss (P&L) & Balance Sheet:** Complete financial structure to monitor revenue, costs, operational expenses, and net margins.
* **Receivables & Multi-channel Reconciliation:** Dedicated modules to track fiscal revenue and platform-specific payouts (iFood and PagSeguro).
* **Strict Inventory Control:** Historical month-over-month inventory tracking to calculate true COGS (Cost of Goods Sold) and variances.
* **Cash Flow & Fixed Expenses Management:** Detailed tracking of operational outflows, fixed costs, and short-term cash predictability.
* **Pricing & Scenario Analysis:** Dynamic tools to calculate optimal menu pricing and simulate the financial impact of strategic business decisions.

## 🧮 Formula Architecture & Automation Logic

The model relies heavily on advanced Excel functions to ensure data integrity, eliminate manual inputs, and keep the spreadsheet dynamic:

* **`SUMIFS` & `COUNTIFS`:** Used across the P&L and Cash Flow tabs to automatically aggregate multi-channel revenues (iFood, PagSeguro, Fiscal) and expenses by matching them to specific months and categories from raw ledgers.
* **`XLOOKUP` & `VLOOKUP`:** Power the pricing and inventory modules. They dynamically pull item costs, unit measurements, and historical supplier prices into the recipe costing sheets, ensuring menu margins update instantly when ingredient costs change.
* **`IF` & Nested Logic:** Drive the scenario analysis (`SCENARIOS`) and pricing tiers, automatically calculating delivery commission cuts, variable taxes, and conditional break-even points based on changing fixed costs or sales volume.
* **Inventory Variances:** Automates true COGS calculation using the classic accounting formula integrated via cell logic: `Beginning Inventory + Purchases - Ending Inventory = COGS`, which isolates waste and theft from regular consumption.

## 🛠️ Tech Stack & Concepts
* Microsoft Excel / Advanced Dynamic Array Formulas
* Corporate Finance Data Structuring
* Food Service Unit Economics
