# CRAZY KITCHEN DATABASE
 
## Introduction: 

Crazy Kitchen is a popular restaurant known for its diverse and innovative cuisine. As the restaurant continues to grow, the need for an efficient and organized data management system becomes increasingly important. Currently, the restaurant faces challenges in managing reservations, inventory, customer orders, and employee data. A well-structured database can address these challenges by centralizing data, streamlining operations, and improving decision-making processes. This project aims to design and implement a comprehensive database system tailored to the specific needs of Crazy Kitchen, enhancing its operational efficiency and customer service.

## Problem Statement:

Crazy Kitchen's existing data management approach relies heavily on manual processes and disparate data storage systems, leading to inefficiencies, errors, and delays. These challenges include:

•	Inefficient Reservation Management: The current system lacks a centralized way to manage reservations, leading to overbooking or double booking.

•	Inventory Control Issues: Inadequate tracking of inventory levels results in either surplus or shortage of ingredients, affecting the kitchen's efficiency and profitability.

•	Inconsistent Order Processing: The absence of an integrated order management system leads to confusion and delays in processing customer orders.

To address these issues, Crazy Kitchen needs a robust database solution that can integrate all aspects of its operations into a single, cohesive system.

## Objectives of Project:

The primary objective of this project is to design and implement a fully functional and efficient database system for Crazy Kitchen. The specific goals include:

•	Centralized Data Management: Create a unified database that consolidates all operational data, including reservations, inventory, orders, and employee schedules.

•	Reservation System: Develop a module to efficiently manage table reservations, preventing overbooking and ensuring optimal seating arrangements.

•	Inventory Management: Implement an inventory tracking system to monitor stock levels, reduce waste, and streamline ordering processes.

•	Order Processing System: Design an order management system that accurately records and tracks customer orders from placement to fulfillment.

•	Scalability and Security: Ensure the database is scalable to accommodate future growth and includes robust security measures to protect sensitive information.

## Relational Model

•	Customer (Customer ID, Name, Email, Phone, MemberID)
-	FOREIGN KEY MemberID refers to MemberID in Customer; NULL NOT ALLOWED

•	Member (MemberID, Discount, JoinDate, ExpiryDate)

•	Staff (StaffID, Name, Email, Phone, Wage, ManagerID, Department, HireDate)
-	FOREIGN KEY ManagerID refers to StaffID in Staff; NULL NOT ALLOWED

•	Order (OrderID, OrderDate, CustomerID, StaffID, TableNumber)
-	FOREIGN KEY CustomerID refers to CustomerID in Customer; NULL NOT ALLOWED
-	FOREIGN KEY StaffID refers to StaffID in Staff; NULL NOT ALLOWED
-	FOREIGN KEY TableNumber refers to TableNumber in Table; NULL ALLOWED

•	OrderedDish (OrderID, DishName, Quantity)
-	FOREIGN KEY OrderID refers to OrderID in Order; NULL NOT ALLOWED
-	FOREIGN KEY DishName refers to DishName in Dish; NULL NOT ALLOWED

•	Supplier (Supplier ID, Name, Phone)

•	Table (TableNumber, Capacity)  

•	Dish (DishName, Description, Price)

•	Ingredient (IngredientID, IngredientName) 

•	IngredientsUsed (IngredientID, DishName, Quantity)
-	FOREIGN KEY IngredientID refers to IngredientID in Ingredient; NULL NOT ALLOWED
-	FOREIGN KEY DishName refers to DishName in Dish; NULL NOT ALLOWED

•	IngredientsSupplied (IngredientID, SupplierID, Quantity)
-	FOREIGN KEY IngredientID refers to IngredientID in Ingredient; NULL NOT ALLOWED
-	FOREIGN KEY SupplierID refers to SupplierID in Dish; NULL NOT ALLOWED

•	Receipt (ReceiptID, Amount, SaleDate, PaymentMethod, OrderID)
