# Product Performance View (`product_perf`) Documentation

## Purpose

Gives the business team a quick view of how each product is performing:
units sold, number of orders, and number of states it reached, without
needing to join multiple tables manually.

## Column Definitions

- product_id: unique identifier for each product
- product_name: name of the product
- product_category: product category (e.g. Bottle, Case)
- product_price: listed price of the product
- total_product_sold: total units sold (sum of quantity across orders)
- total_product_orders: number of distinct orders that included the product
- total_states: number of distinct states the product was shipped to

## Changes in the Second Challenge

The business team wanted to know the geographic reach of each product.
Added a join with the customers table and a new column, total_states
(COUNT(DISTINCT c.state)), to count unique states per product.
