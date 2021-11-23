# Name of the project
Game retailer
# Name of the team 
-Team Spririt
# team members 
- Changchang Liu 
- Jiatian Wang
# Project Description
Game industry are popular these days. And player are more willing to pay for their favorite games and products. The next generation game console PS5 and Xbox are released this year. And we think it's a good idea to come up with a platform which allows players and compaies to sell and purchase game products. <br />
# User Data Models
There are three user data models: customer users, customer service staff users and company Users. <br />
Customer users have the following 11 fields: customer id (PK), firstname, lastname, username, customer rank (which is an enum), password, personal description, email, date of birth, created date and updated date. <br />
Customer service staff users are similar with 9 fields: staff id (PK), firstname, lastname, username, password, email, date of birth, created date and updated date. 
Company users include 10 fields: company id (PK), name, username, country or region, description, password, email, company type (which is an enum), created date and updated date. <br />
# Domain Object Data Model: Game Product, Review and Order
There are three domain object data models: Game Product, Review and Order. Game and Accessory are inherited from game products. <br />
Game Products include 8 fields: product id (PK), company id (FK), country or region, description, release date, price, and also the created date and updated date. Game and Accessory are inherited from game products, with additional fields game genre, system requirement and game name, or accessory type, accessory name and other details. <br />
Reviews have 7 fields including review id (PK), customer id (FK), product id (FK), score, comment, created date and updated date. <br />
Orders have 8 fields including order id (PK), customer id (FK), product id (FK), service staff id (FK), date of purchase, status, created date and updated date. <br />
# User to Domain Object Relationship
Customer users have one-to-many relationships with orders and reviews, and a many-to-many relationship with products. Meanwhile, customer service staffs have an one-to-many relationship with orders. And each company user can be related to many products. 
# User to User Relationship
Customer users have a many-to-many relationship with customer-service staff users. 
# Domain object to Domain Object Relationship
Products have one-to-many relationships with orders and reviews. 
# Portable Enums
There are 5 portable enumerations: CustomerRank, GameGenres, AccessoryType, CompanyType and OrderStatus. <br />
CustomerRank includes Immortal, Divine, Ancient, Legend, Archon. <br />
GameGenres includes Sports, RPG, RTS, MOBA, simulator. <br />
AccessoryType includes Controller, Audio, Video, Console, Others. <br />
CompanyType includes game-developer, game-publisher, accessories-company. <br />
OrderStatus includes cancelled, processing, completed, refunded. <br />
# User Interface Requirements
For User interface, we will build user interface for customer, customer service and company based on React.js frameworks.
In customer screen, player will be able to search or purchase product. And allow user to review on a product. <br />
User will be able to operate CRUD operations on reviews. <br />
For customer service screen, customer service will be able to update information about an order, reply a customer's message.
On company screen, companies can have full CRUD operations on a product which means they can update or delete a product 
on the user interface. <br />
