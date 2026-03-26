### Data Dictionary: operations_insight_dashboard
**File Name:** `electronics_messy_sales_dataset_cleaned.csv`  
**Project:** Retail Growth Intelligence: A Multi-Branch Retail BI Dashboard

|     Column Name      |      Data Type    |                          Description                                     |
|         ---          |        ---        |                              ---                                         |  
| **Customer Name**    | String            | The name of the individual or entity who made the purchase.              |
| **State**            | String            | The Nigerian state where the transaction occurred (Regional Identifier). |
| **Product**          | String            | The specific electronic item sold (e.g., Laptop, Smartphone).            |
| **Units Sold**       | Integer           | The total quantity of the specific product purchased.                    |
| **Units Price**      | Currency          | The price of a single unit in Naira (₦).                                 |
| **Total Sales**      | Currency          | The gross revenue generated (`Units Sold * Units Price`).                |
| **Profit**           | Currency          | The net gain after deducting the Cost of Goods Sold (COGS).              |
| **Sale Date**        | Date              | The specific day the transaction was recorded.                           |
| **Sales Channel**    | String            | The platform or method used for the sale (e.g., In-Store, Online, POS).  |