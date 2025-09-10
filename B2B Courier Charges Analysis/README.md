## 📌 Problem Statement

ABC Company, an e-commerce platform, needed to verify the accuracy of courier charges billed by their partners. They wanted to compare their internal calculations of order weight and delivery zone with the courier companies' invoices and identify discrepancies in billing amounts.

## 🛠️ Approach Followed

The analysis was carried out in the following steps:

### Data Loading and Inspection

Loaded the provided datasets (Website Order Report, SKU Master, Pincode Mapping, Courier Invoice, and Courier Company Rates) into pandas DataFrames.

Performed initial inspection and handled missing or irrelevant columns.

### Data Merging

Merged the datasets to consolidate relevant information for each order, including order details, product weights, and pincode-to-zone mappings.

### Weight Calculation and Slab Determination

Calculated the total weight of each order based on the SKU master and order quantity.

Rounded the calculated weights up to the nearest 0.5 kg to determine the weight slab as per ABC's logic.

### Zone Mapping

Determined the delivery zone for each order based on the warehouse and customer pincodes using the provided mapping.

### Expected Charge Calculation

Calculated the expected courier charge for each order based on the calculated weight slab, delivery zone, and the courier company's rate card.

Applied the fixed and additional charges for the relevant zone and shipment type (Forward or Forward + RTO).

### Comparison and Analysis

Merged the calculated expected charges with the actual billing amounts from the courier invoices.

Calculated the difference between the billed amount and the expected charge to identify overcharges, undercharges, and correctly charged orders.

### Summary and Visualization

Summarized the findings by counting the number of orders in each category (correctly charged, overcharged, undercharged).

Calculated the total monetary amounts associated with each category.

Visualized the proportion of orders in each category using a pie chart.

## ✅ Outcome

The analysis provided a clear picture of the billing accuracy of the courier companies.

Identified the total number of orders that were correctly charged, overcharged, and undercharged.

Quantified the total monetary amount associated with overcharges and undercharges, enabling ABC Company to recover potential overbilled amounts.

Helped ABC Company in auditing courier invoices, ensuring fair billing practices, and optimizing logistics costs.
