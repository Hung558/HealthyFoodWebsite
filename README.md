# 🥗 Healthy Food - Comprehensive Online Nutrition Platform

![Java](https://img.shields.io/badge/Language-Java-orange.svg?style=for-the-badge&logo=java)
![JSP/Servlet](https://img.shields.io/badge/Technology-JSP%20%2F%20Servlet-blue.svg?style=for-the-badge)
![MySQL](https://img.shields.io/badge/Database-MySQL-blue.svg?style=for-the-badge&logo=mysql)
![NetBeans](https://img.shields.io/badge/IDE-NetBeans-green.svg?style=for-the-badge&logo=apache-netbeans-ide)

## 📖 Introduction
**Healthy Food** is a robust web-based e-commerce platform designed to promote a healthy lifestyle by providing high-quality nutritious meals. This project aims to bridge the gap between nutritionists and consumers, ensuring that every meal ordered is not just delicious but also scientifically beneficial for the user's health.

The system manages a complex ecosystem involving customers, logistics (shippers), inventory (sellers), and specialized nutrition consultants (nutritionists).

---

## 🌟 Key Features

### 🛠 Six-Role Management System
The platform features a sophisticated access control system with 6 distinct roles:

1.  **Guest:** * Browse healthy menus and categories.
    * Search for dishes based on nutritional needs.
    * Place orders by manually providing contact and shipping information.
2.  **Customer:** * All Guest features with an enhanced experience (saved profiles).
    * **BMI Calculator:** Calculate Body Mass Index and receive personalized meal suggestions.
    * Order history tracking and profile management.
3.  **Nutritionist:** * Manage nutritional facts for every dish (calories, protein, fats, etc.).
    * **Health Blog:** Create and manage a specialized blog to educate users on healthy eating habits.
4.  **Seller:** * Manage incoming orders and verify payments.
    * Coordinate with the kitchen and shippers.
5.  **Shipper:** * Pick up orders and update real-time delivery status.
    * Manage delivery routes and completed tasks.
6.  **Manager:** * Oversee store operations.
    * Approve requests and content updates from Sellers and Nutritionists.
    * Generate reports on revenue and growth.

---

## 💻 Tech Stack
* **Backend:** Java EE (JSP & Servlet)
* **Database:** MySQL Server
* **Frontend:** HTML5, CSS3 (Bootstrap 5), JavaScript
* **Development Tool:** NetBeans IDE 
* **Web Server:** Apache Tomcat 9.0 (or higher)
* **Design Pattern:** MVC (Model-View-Controller)

---

## 📂 Project Structure
```text
HealthyFood_Project/
├── src/java/
│   ├── com.healthyfood.controller/  # Servlets for handling requests
│   ├── com.healthyfood.dao/         # CRUD operations with MySQL
│   ├── com.healthyfood.model/       # Plain Old Java Objects (Entities)
│   └── com.healthyfood.utils/       # DBConnection, Security, Filters
├── web/
│   ├── views/                       # Organized JSP files for each Role
│   ├── assets/                      # CSS, JS, Images, and Fonts
│   └── WEB-INF/                     # Configuration (web.xml)
└── sql/
    └── database_script.sql          # Full database schema & sample data
