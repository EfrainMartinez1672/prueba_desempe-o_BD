# Inventory Management Database
This repository contains the PostgreSQL schema designed for an inventory and supply chain management system.

# Overview
The database tracks products, suppliers, warehouses, and the movement of orders. It is designed to manage complex relationships between locations, categorized inventory, and transactional movements.

# Key Tables
riwi_product: Stores product information, including pricing, creation/update timestamps, and category mapping.

riwi_category: Defines categories to organize products.

riwi_supplier: Maintains supplier contact details linked to specific cities.

riwi_ware_house: Manages warehouse locations linked to specific cities.

order: Represents high-level purchase orders connecting suppliers to specific warehouses.

order_details: Contains specific line items for orders, linking products to quantities and movement types.

movement_type: Defines the nature of inventory movements.

riwi_city: A lookup table for city names used by both suppliers and warehouses.

# Relationships
Products: Linked to categories via id_category.

Suppliers & Warehouses: Located in specific cities via id_city.

Orders: Coordinate the relationship between a riwi_supplier and a riwi_ware_house.

Movements: Detailed order tracking is facilitated through order_details, which references both the order and the specific movement_type.