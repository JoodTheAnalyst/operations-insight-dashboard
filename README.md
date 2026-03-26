# Retail Growth Intelligence: Automated Multi-Branch Profitability Analysis
---

### 📊 [View Live Interactive Dashboard](https://docs.google.com/spreadsheets/d/1xVoaPTUtM-UiwLkYp12r315T9y42ycurUFRofyWhjsk/edit?usp=sharing)

---

This project engineered a high-performance BI engine to analyze a massive ₦4.04 Billion sales portfolio across 20 Nigerian states. By automating data transformation, the analysis uncovered that Delta (₦290.4M) and Imo (₦277.9M) are the undisputed regional powerhouses, outperforming all other states in both gross revenue and net profit, driven primarily by the high-volume success of Keyboards and Tablets.

## Business Question
Which Nigerian branches and product categories are the primary drivers of net profit, and how can we identify the specific regional leaders within a multi-billion naira electronics portfolio?

## Dataset
- Source: Internal sales export (Multi-branch retail electronics dataset).
- Size: 500 rows × 9 columns (Cleaned).
- Time period: 2023 – 2025.
- Total Portfolio Value: ₦4,040,261,271.
  
## Key fields:
- State: Geographical branch location in Nigeria (20 States tracked).
- Total Sales: Gross revenue per transaction.
- Profit: Net gain after accounting for unit costs.
- Product: Electronic category (8 Categories tracked).

## Tools Used
- Google Sheets / Excel: Data hosting, cleaning, and dashboard engine.
- Advanced Formulas: Utilized FILTER, QUERY, and INDEX/MATCH for dynamic data slicing.
- Data Validation: Implemented dropdown-based validation rules for interactive reporting.

## Key Findings
- Top Tier Performers: Out of 20 states, Delta and Imo emerged as the primary revenue drivers, generating ₦290,454,223 and ₦277,914,354 respectively.

- Profit Leadership: Delta and Imo did not just lead in volume; they also generated the highest net profit across the entire organization, proving the efficiency of these regional branches.

- Product Dominance: Across the board, Keyboards and Tablets outperformed the other 6 product categories, maintaining the highest sales velocity and total revenue contribution.

## Visualizations
This interface serves as the primary BI command center, featuring a dynamic breakdown of the ₦4.04 Billion portfolio. It allows stakeholders to toggle seamlessly between specific States and Product Categories while utilizing a custom Date Range Filter. By toggling between specific start and end dates, users can isolate performance trends within narrow timeframes or analyze the entire two-year trajectory of revenue and profitability shifts.

## How to Reproduce
- Clone this repo: git clone https://github.com/JoodTheAnalyst/operations-insight-dashboard
- Open the data/cleaned/ folder to view the source dataset.
- Review notebooks/analysis-walkthrough.md to understand the formula logic and cleaning steps.
- click on this link to interact with the live dashboard [View Live Interactive Dashboard](https://docs.google.com/spreadsheets/d/1xVoaPTUtM-UiwLkYp12r315T9y42ycurUFRofyWhjsk/edit?usp=sharing

## What I'd Do Next
- Underperformer Analysis: Investigate why the bottom-performing states are lagging and if a "Sales Channel" shift (e.g., more Online focus) could mirror Delta's success.

- Time-Series Forecasting: Apply seasonal trending to predict when the next ₦4 Billion milestone will be reached.
