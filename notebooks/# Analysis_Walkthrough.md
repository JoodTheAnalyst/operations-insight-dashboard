# Analysis Methodology & Logic Walkthrough

## Data Acquisition & Initial Assessment
The raw dataset (electronics_messy_sales_dataset.csv) was audited to identify structural and data integrity issues. The following inconsistencies were uncovered:

- Missing Values: Significant "null" entries in the Customer Name and Sales Channel columns.

- Inconsistent Casing: Product names were a mix of proper case (Laptop) and upper case (HEADPHONES). State names were inconsistently capitalized (e.g., "rivers" vs "Rivers").

- Data Type Mismatches: The Units Sold column contained empty strings where numerical values were expected, and Unit Price lacked standardized currency formatting.

- Redundancy: The Order ID (UUID format) provided unique identification but required no transformation for the scope of this BI dashboard.

## Data Transformation (Cleaning Log)
The following steps were taken in the "RawData" sheet of the Excel workbook to reach the "Cleaned" state:

- Standardization: Used PROPER() functions or manual overrides to ensure all States and Products followed a uniform naming convention.

- Null Handling: Empty Customer Name cells were filled with "Not Provided" to ensure pivot tables and filters remained accurate. Missing Sales Channel entries were categorized similarly.

- Calculated Columns:  Total Sales: Calculated using [`Units Sold`] * [`Unit Price`] 

- Profit: Calculated by applying ([`Unit Price`] - [`Unit Cost`]) * [`Units Sold`]

- Formatting: Converted Sale Date to a standard Date localized for Nigeria and set financial columns to Currency format.

## Dynamic Filtering Logic
To power the dashboard without manual updates, a dedicated Filtering_RawData sheet was created.

The "Engine" (Cell A2): The dashboard utilizes a complex FILTER function. It is designed to pull data from the "Raw Data" sheet based on two primary criteria:

**State Selection: Linked to the dashboard's State dropdown.** 

**Product Selection: Linked to the dashboard's Product dropdown.**

Logic: The formula uses a wildcard or "All" logic (e.g., IF(Dashboard!$B$4="All States", ...)). If a user selects a specific state, the data shrinks to that state; if they select "All," the engine pulls the entire dataset.

## Dashboard Architecture & KPIs
The Dashboard sheet acts as the final BI interface. It utilizes the filtered data to generate real-time insights 

### Key Metrics (KPIs)
- Total Sales & Profit: Calculated using SUM(Filtering_RawData!...) on the dynamic ranges in the filtering sheet.

- Profit Margin: A calculated ratio showing the efficiency of sales.

- Automated Narratives: High-level summaries (e.g., "The highest performing branch is...") are generated using string concatenation (&) and tieing it to specific cells with validation dropdowns in place to provide instant verbal context to the numbers.

### Visual Components
- Regional Performance: A chart (or map) visualizing sales by State, allowing for immediate identification of high-margin regions.
- Sales Channel Analysis: A breakdown of the various sales channels and their revenue shares
- Product Breakdown: Bar or Pie charts showing which products drive the most volume.

