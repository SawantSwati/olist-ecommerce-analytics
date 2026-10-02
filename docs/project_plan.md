# Project plan

## Problem statement
Olist is a Brazilian online marketplace. This project analyses its sales, delivery performance and customer behaviour (Oct 2016 - Aug 2018) to find where revenue comes from, where deliveries are late, and what to improve.

## What one row means (grain)
Each row is one order item joined to one payment. An order with 2 items or 2 payments appears on several rows, so summing price or payment_value on raw rows counts money more than once. I will remove duplicates first (95,128 orders, 108,640 order items, 99,329 payments).

## KPIs
- Revenue = sum of price (item grain)
- Orders = distinct order_id
- Average order value = revenue / orders
- Late delivery % = orders delivered after the estimated date / orders
- Average delivery days = delivered date - purchase date
- Repeat customer % = customers with more than 1 order / customers

## Limits of this file
No review scores, only 7 canceled orders, about 3% repeat customers, and almost no data in late 2016. I will not claim churn or satisfaction results.