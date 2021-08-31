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
* Spring Security
* MySQL 
* Maven
* Maven Checkstyle Plugin
* Apache Tomcat

# Features implemented:

* DTO Validation
* Password hashing
* Access distribution among USER and ADMIN roles:
  
  * GET: /inject, /login - all(including unauthenticated users)
  * POST: /register - all(including unauthenticated users)
  * GET: /cinema-halls - user/admin
  * POST: /cinema-halls - admin
  * GET: /movies - user/admin
  * POST: /movies - admin
  * GET: /movie-sessions/available - user/admin
  * GET: /movie-sessions/{id} - user/admin
  * POST: /movie-sessions - admin
  * PUT: /movie-sessions/{id} - admin
  * DELETE: /movie-sessions/{id} - admin
  * GET: /orders - user
  * POST: /orders/complete - user
  * POST: /shopping-carts/movie-sessions - user
  * GET: /shopping-carts/by-user - user
  * GET: /users/by-email - admin

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
* To test USER role, login to the system using login: `user@test.com` and password: `1q2w3e4r`
* To test ADMIN role, login to the system using login: `admin@test.com` and password: `1q2w3e4r`