# Name of the project
# Name of the team 
-Team Spririt
# team members 
- Changchang Liu 
- Jiatian Wang
# Project Description
This project creates
# User Data Models
There are three user data models: customer users, customer service staff users and company Users. 
Customer users have the following 11 fields: customer id (PK), firstname, lastname, username, customer rank (which is an enum), password, personal description, email, date of birth, created date and updated date. 
Customer service staff users are similar with 9 fields: staff id (PK), firstname, lastname, username, password, email, date of birth, created date and updated date. 
Company users include 10 fields: company id (PK), name, username, country or region, description, password, email, company type (which is an enum), created date and updated date. 
# Domain Object Data Model: Game Product, Review and Order
There are three domain object data models: Game Product, Review and Order. Game and Accessory are inherited from game products. 
Game Products include 8 fields: product id (PK), company id (FK), country or region, description, release date, price, and also the created date and updated date. Game and Accessory are inherited from game products, with additional fields game genre, system requirement and game name, or accessory type, accessory name and other details. 
Reviews have 7 fields including review id (PK), customer id (FK), product id (FK), score, comment, created date and updated date. 
Orders have 8 fields including order id (PK), customer id (FK), product id (FK), service staff id (FK), date of purchase, status, created date and updated date. 
# User to Domain Object Relationship
Customer users have one-to-many relationships with orders and reviews, and a many-to-many relationship with products. Meanwhile, customer service staffs have an one-to-many relationship with orders. And each company user can be related to many products. 
# User to User Relationship
Customer users have a many-to-many relationship with customer-service staff users. 
# Domain object to Domain Object Relationship
Products have one-to-many relationships with orders and reviews. 
# Portable Enums
There are 5 portable enumerations: CustomerRank, GameGenres, AccessoryType, CompanyType and OrderStatus. 
# User Interface Requirements
