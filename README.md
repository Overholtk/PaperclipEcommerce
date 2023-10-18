# PaperclipEcommerce
Database and front end managemant for Patty's Bulk Paperclips

## Entity Relationship Diagram
![image](https://github.com/Overholtk/PaperclipEcommerce/assets/71245955/a159ff83-7ca6-4026-b2dd-32c14e8e4418)


## Explanation of Tables:
- **Customer:** Contains all current customers
- **Order:** Contains the ID of the customer it belongs to, it's own ID, and the items in the order
- **Order Item:** Links the Order and Item tables by ID, determining which order contains which items. Links the order table to the Inventory table, allowing the orders to update the quantity of items in the inventory.
- **Item:** Contains of all availible item types availible for purchase
- **Inventory:** Contains all items currently availible in the inventory and their quantity

## Explanation of Relationships:
- **Customer Table**
  - One to many relationship with the order table: One customer may have many orders
- **Order Table**
  - One to many relationship with order item table: one order may have many items
- **Order Item Table**
  - Many to one relationship with item table: one order may have many kinds of items
  - Many to one relationship with the Inventory table: one order item may effect many items in the inventory
- **Item Table**
  - Many to one relationship with inventory table: the inventory may carry many types of items
