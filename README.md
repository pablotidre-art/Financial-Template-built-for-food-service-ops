 Restaurant Financial Management Model

A working financial system for food service operations — monthly P&L, controller-level KPIs, cash position tracking, scenario forecasting, inventory-driven COGS, and menu pricing.

Built and operated by **Pablo Tidre**, who spent 12 years running the financial operations of restaurant businesses. This is the infrastructure I designed, used daily, and relied on to make pricing, staffing, and cash decisions.

> **Note on data:** All figures in this workbook are **illustrative**. They are sample values built to demonstrate the model's structure and logic, and do not represent the actual financial results of any business.

---

## What's in the model

| Sheet | What it does |
|---|---|
| **Executive Summary** | One-page business snapshot: headline metrics, value drivers, and risk factors. |
| **Controller Dashboard** | Management P&L by month with restaurant KPIs — food cost %, prime cost %, EBITDA margin. |
| **Monthly P&L** | Detailed monthly profit & loss by expense category, with net margin and total owner benefit. |
| **Cash Position** | Daily liquidity tracking across bank, cash on hand, and payment-processor receivables. |
| **Scenario Forecast** | Six volume scenarios modeling revenue, staffing, cost structure, and resulting margin. |
| **Balance Sheet & Inventory** | Inventory movement, true COGS calculation, capital position, and revenue by customer type. |
| **Menu Pricing** | Item-level pricing by size, derived from ingredient cost and target margin. |

---

## Accounting approach

**Accrual basis.** Revenue and costs are recognized in the period they occur, with a separate cash-basis view (Cash Position) for liquidity management. This separation matters in food service, where payment processors and delivery platforms settle on a lag — reported performance and available cash are rarely the same number in the same week.

**True COGS from inventory movement.** Food cost is not taken from purchase invoices. It is calculated as:

```
Beginning Inventory + Purchases − Ending Inventory = COGS
```

This isolates actual consumption from purchase timing, and surfaces waste, spoilage, and shrinkage that a purchase-based number would hide.

**Prime cost as the control metric.** Food cost and labor are tracked together as prime cost — the single number that determines whether a restaurant is viable. Individually, either can look acceptable while the combination quietly sinks the business.

**Owner economics separated from business economics.** Owner's draw is broken out so that Adjusted EBITDA (pre-draw) reflects what the business generates, while net income reflects what it retains. Both are needed to evaluate the operation honestly.

---

## Formula architecture

Every calculated figure is a live formula — no hardcoded results. Change an input and the model recalculates end to end.

- **`SUMIFS` / `COUNTIFS`** — aggregate multi-channel revenue and expenses from raw transaction ledgers, matched by month and category.
- **`XLOOKUP` / `VLOOKUP`** — pull ingredient costs, unit measures, and supplier prices into the recipe and pricing sheets, so menu margins update the moment an input cost changes.
- **`IF` and nested logic** — drive scenario analysis, platform commission tiers, variable tax treatment, and conditional break-even points.
- **Cross-sheet linking** — the P&L, dashboard, and inventory sheets reference a single source, so there is one version of each number.

**Reading convention:** blue text = manual input · black text = formula · green text = link to another sheet.

---

## Capabilities demonstrated

Month-end close structure · Balance sheet and bank reconciliation · Accounts payable tracking · Accrual-basis treatment · Multi-channel revenue recognition · Variance analysis · Cash flow forecasting · Inventory control and true COGS · Unit economics and pricing · KPI reporting for ownership

---

## Scope note

This repository presents the **core structure** of the model. The production version in daily use spans 40+ interlinked sheets, including transaction-level revenue and expense ledgers, monthly physical inventory counts, and payment-processor reconciliation. The portfolio version here keeps the architecture and logic while remaining readable.

---

## Tech

Microsoft Excel / Google Sheets · Advanced formula architecture · Corporate finance data structuring · Food service unit economics

---

**Pablo Tidre**
[LinkedIn](https://linkedin.com/in/pablo-tidre) · pablotidre@gmail.com
