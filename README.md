# Ecommerce-Delivery-Charges-Verification-Project
# Ecommerce Delivery Charges Verification Project

## Overview

This Python project aims to verify the charges levied by courier partners for delivering orders from an ecommerce company in India. The project involves analyzing data from the ecommerce company's order reports and courier company invoices to ensure accuracy in billing.

## Business Scenario

The ecommerce company, referred to as X, receives a large number of orders daily and relies on multiple courier companies for delivery. The charges are dependent on the weight of the product and the distance between the warehouse (pickup location) and the customer's delivery address.

## Input Data

### Left Hand Side (LHS) Data (X’s Internal Data)

1. *Website Order Report*: Contains Order IDs and product details for each order.
2. *SKU Master*: Provides the gross weight of each product to calculate the total weight of each order.
3. *Warehouse Pincode to All India Pincode Mapping*: Used to determine delivery zones.

### Right Hand Side (RHS) Data (Courier Company Invoice)

1. *Invoice in CSV Format*: Includes AWB Number, Order ID, weight of shipment, pickup pincode, delivery pincode, delivery zone, charges per shipment, and type of shipment.
2. *Courier Charges Rate Card*: Specifies charges at weight slab and pincode levels.

## Output Data

### Output Data 1

A resultant CSV/Excel file with the following columns:

- Order ID
- AWB Number
- Total weight as per X (KG)
- Weight slab as per X (KG)
- Total weight as per Courier Company (KG)
- Weight slab charged by Courier Company (KG)
- Delivery Zone as per X
- Delivery Zone charged by Courier Company
- Expected Charge as per X (Rs.)
- Charges Billed by Courier Company (Rs.)
- Difference Between Expected Charges and Billed Charges (Rs.)

### Output Data 2

A summary table containing:

- Count of total orders where X has been correctly charged
- Total invoice amount for correctly charged orders
- Count of total orders where X has been overcharged
- Total overcharging amount
- Count of total orders where X has been undercharged
- Total undercharging amount

## Dependencies

- pandas
- numpy
- matplotlib

## Usage

1. Clone the repository to your local machine.
2. Install the required dependencies using pip install -r requirements.txt.
3. Place the input data files in the designated directory.
4. Run the Python script delivery_charges_verification.py.
5. Find the resultant Excel files in the output directory.

## Contributing
-Rohit Kag https://github.com/Rohit-Kag/Ecommerce-Delivery-Charges-Verification-Project
