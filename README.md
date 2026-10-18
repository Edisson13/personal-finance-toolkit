# Personal Finance & Net Worth Suite

A client-side suite of personal finance engines designed for multi-asset investing, cost-of-living budgeting, liability elimination, holistic net worth projection, retirement independence, and real estate decision-making.

---

## Architectural Philosophy: Standalone Single Files

Every application in this repository is built as an independent, self-contained `.html` file. 

* **No Shared Dependencies:** Style sheets (`<style>`) and JavaScript runtimes (`<script>`) are embedded directly into each file.
* **Portable & Serverless:** Open any file via the `file://` protocol simply by double-clicking it on your computer. No Node.js, npm, bundlers (Webpack, Vite), local HTTP servers, or build pipelines required.
* **Zero Remote Requests:** Visual charts are generated using standard HTML5 Canvas without remote CDNs or external fonts. Everything works 100% offline.
* **Independent Distribution:** You can copy a single file onto a flash drive, send it as an email attachment, or run it on any device with a modern web browser.

---

## Included Tools

| Application File | Core Focus | Key Metrics & Features |
| :--- | :--- | :--- |
| **`index.html`** | Central Hub, Net Worth Command Center & CSV Inspector | Step-by-step user guide, interactive Net Worth & Future Projector (syncs CSVs from Investing, Debt, Cost of Living & Mortgage modules), and universal CSV inspector. |
| **`networth-tracker.html`** | Monthly Reality Log & Progress Tracker | Dedicated historical log tracker (enforces 1 entry per month). Maintains your permanent net worth timeline, uploads planned scenarios from the Net Worth hub or single modules, and benchmarks actual reality vs. plan. |
| **`savings-calculator.html`** | Multi-Asset Investing & Portfolio | $N$-asset modeling (Index Funds, ETFs, HYSA, Crypto, Bonds), custom compounding frequencies, portfolio weighting bar. |
| **`cost-of-living.html`** | Cost of Living & Cash Flow Budgeter | Essential Needs vs. Discretionary Wants, 50/30/20 rule benchmarks, category-specific inflation, location cost multiplier, and investable surplus tracking. |
| **`debt-payoff.html`** | Liability Elimination | Avalanche vs. Snowball comparison, minimum rollover acceleration, debt-free date modeling. |
| **`mortgage-calculator.html`** | Real Estate Debt | P&I, property tax, insurance, HOA, synchronized loan terms, full annual/monthly amortization schedule. |
| **`retirement-fire.html`** | Financial Independence | Safe Withdrawal Rates (SWR), Lean/Regular/Fat/Coast FIRE targets, asset drawdowns up to age 90. |
| **`emergency-runway.html`** | Capital Preservation | Lean Survival, Moderate Comfort, and Full Current Spend burn rates with bridge income support. |
| **`rent-vs-buy.html`** | Opportunity Cost | Compares buyer home equity vs. renter market-invested down payment to identify the breakeven year. |

---

## Planning Tools vs. Historical Reality Tracker

* **Planning Engines (`index.html`, `savings-calculator.html`, etc.):** Used for **forward-looking scenario modeling**, projecting compound interest, amortizing debt, and calculating hypothetical net worth trajectories into the future.
* **Monthly Reality Tracker (`networth-tracker.html`):** Used strictly for **logging actual historical records** (one entry per calendar month). It computes all-time wealth change, monthly savings pace, and plots your real-world net worth dots against your uploaded planned scenario curve.
* **File Separation:** Historical Tracker CSVs should only be loaded inside `networth-tracker.html`. Scenario planning CSVs can be loaded across the respective planning calculators and the Net Worth Command Center.

---

## Data Portability (Bi-Directional CSV & Net Worth Sync)

Every engine supports localized data persistence:
* **Export CSV:** Exports complete scenario configurations and year-by-year schedules with UTF-8 BOM encoding for compatibility with Microsoft Excel, Apple Numbers, and Google Sheets.
* **Load CSV:** Re-imports previously exported CSV files directly into the calculator to restore inputs, charts, and schedules without sending data to an external server.
* **Cross-Module Net Worth Sync:** Load exported CSVs from `savings-calculator.html`, `debt-payoff.html`, `cost-of-living.html`, and `mortgage-calculator.html` directly into the **Net Worth Command Center** on `index.html` to compute current net worth, model automatic debt-to-investment rollovers, and export/reload a master Net Worth CSV.

---

## Getting Started

1. Clone or download this repository.
2. Double-click `index.html` to open the central suite in your default web browser.
3. Follow the 4-step Quick-Start Guide at the top of the landing page to model your modules, export CSVs, and project your total net worth.
4. Launch `networth-tracker.html` to record your monthly snapshots, maintain your historical log, and track real progress against your plan.