![GitHub Logo](cinema.jpg)

# Cinema app

This application emulates the workflow of cinema and allows us to manage a database of users that have the possibility to choose movie sessions and place orders with the help of http requests from the client.
The users have two distinct roles with limited access to url endpoints.
The application is based on SOLID principles and N-tier architecture with 3 levels such as DAO layer with CRUD operations, Service layer, Controller layer. 

# Technologies used:

* Java 11
* Hibernate
* Spring Core
* Spring MVC
* Spring Web
* Spring Security
* MySQL 
* Maven Checkstyle Plugin
* Apache Tomcat

# Features implemented:

* DTO Validation
* Password hashing
* Access distribution among USER and ADMIN roles


# Configuration:

* Clone this project to your computer and open project in your IDE.
* Install MySQL and MySQL Workbench
* Set your mySQL username, password and db url as parameters in `src/main/resources/db.properties`
* Configure Apache Tomcat
    * Edit Configurations
    * Add New Configuration -> TomCat Server -> Local
    * Fix -> web-security:war exploded
    * Deployment tab -> Application context -> leave only "/"
* Launch application and access `http://localhost:8080/inject` to inject roles and test users to DB
* Login to the system using login and password which you can find in DB in `users` table