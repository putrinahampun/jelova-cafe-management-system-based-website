# 🥘Jelova Cafe Management System Based on Website🥘

## 🖼️ Project Description 
**Introduction**

The Jelova Café & Resto Management Website is designed to replace the manual management system of Jelova Café & Resto, which has caused inefficiencies such as order errors, delayed service, and cashier overload, especially during busy times. This new system aims to streamline operations by providing an efficient, fast, and accurate service platform, thus enhancing customer experience and improving staff productivity. The website is intended for the café's owner and staff, ensuring smoother order management, reducing confusion in the kitchen, and easing the cashier's workload to deliver optimal service.

**Features**

- **User Registration & Login**
  User registration is used to store new user data, while user login verifies the data of users who have registered through the registration feature. Login verification uses authentication services with the Auth Facades library.
- **Role Based Access Control (RBAC)**
  Role-Based Access Control refers to a system where different users have specific roles. For this website, there are three roles: Cashier, Waiter, and Kitchen staff. The Cashier is responsible for managing the café's income. The Waiter is responsible for serving customers' orders. The Kitchen staff is responsible for updating the order status, whether it is still being cooked or ready to be served. This feature can be implemented using Middleware from Laravel.
- **CRUD (Create, Read, Update, & Delete)**
  CRUD refers to the technical features for creating, reading, updating, and deleting data in the system. Each role has access to these features based on their specific tasks.

## ⚙️ Setup 

**Dependencies**
- Laravel == 8x
- Composer == 2.0.12
- Bootstrap == 3.4.0
- PHP == 3.4.0
  
**Tools**
- VS CODE : as the IDE (you can use another IDE).
- XAMPP : software to access MySQL Server for Database.
- Browser : for showing up the result (using localhost).
  
## 🏗️ Database Schema

**Table & Field**
- Database Name: tubes_imk
- Total Table: 11 tables

  | Table name | Atributes | Purpose |
  | ---------- | --------- | ------- |
  | casirs | id | saving id for role Cassir |
  | kitchens | id | saving id for role Kitchen |
  | waiters | id | saving id for role Waiter |
  | users | id, name, email, password, role, avatar(image) | saving users data |
  | drinks | id, drink_name, price | saving drink's menu | 
  | tables | id, table | saving the number of table |
  | food | id, food_name, price | saving food's menu |
  | services | id, services | saving services options (dining, take away) |
  | price_sums | id, food_order, drink_order | saving the total of food's and drink's price |
  | drink_orders | id, table_no, drink_order, drink_portion, services, status | saving drink's order data |
  | food_orders | id, table_no, food_order, food_portion, services, status | saving food's order data | 
 
**Entity Relationship Diagram**
![image](https://github.com/user-attachments/assets/c31d56c6-478d-4eed-a4ac-6c96b025c9d7)

## 💻 Deployment 

**Cloning Project**
- Open the project on github, find the HTTPS or SSH button. Choose and press one of them, then copy the link provided.
- In your local computer, create or choose the folder you want to save the project. Open the gitbash, type this command git clone [paste the link] and paste the copied-link after that. If you can't find the gitbash, then you should download and install git or your computer.

**Running Project**
- Open the project on your IDE. Copy file .env by using ```cp.env.example .env``` (change the copied-file from .env.example to .env). Make sure the name of databases already exists in your database system.
- Open the terminal section and type this command ```composer install``` for installing the Composer.
- Type this command ```php artisan key:generate``` after you there's no doubt in step one and two.
- After that, type this command ```php artisan migrate``` to migrate the all the table's structures to your database.
- This project provides a database seeder to give you a data example, so type this command too ```php artisan db:seed```.
- Finally type this command to run the project ```php artisan serve```.
- Well done!

## 🖋️ Additional Comments 

**Future Plans**
- Improving the databases to be more well-structured.
