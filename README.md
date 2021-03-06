Cinema-app
====
This simple web application imitates the work of the online cinema tickets shop with basic registration, authentication and authorization abilities.

Project structure
-----------
Application is designed according to SOLID, REST principles, using DAO, DI and N-Tier Architecture patterns with next layers:
1. controllers layer;
2. services layer;
3. DAO layer;

Features
-----------
1. Register
2. Login / Logout
3. Display all movies
4. Display all cinema halls
5. Display all movie sessions
6. Complete order (for User only)
7. Display all orders

Also, there are some features for Admin only
1. Create movie
2. Create cinema hall
3. Create / Update / Delete movie session
4. Find user by email

Technologies
-----------
* Java 11
* Spring Core
* Spring WEB
* Spring Security
* Hibernate
* Apache Tomcat(v9.0.50)
* Apache Maven
* MySQL

Usage
-----------
1. Install IntelliJ IDEA ultimate version;
2. Clone this project from GitHub and make sure that an absolute path doesn't include any white spaces and/or non-latin
   symbols;
3. Install and configure Apache Tomcat(v9.0.50), connect and configure Tomcat inside the application;
4. Install MySQL and MySQL Workbench;
5. Install Postman 
6. Configure db.properties file to make a connection to you DB;
7. Run application;
8. Test application using postman and/or your browser address bar
     * Use login: user@i.ua and password: user123 to authenticate as user;
     * USE login: admin@i.ua and password: admin123 to authenticate as admin.

List of allowed http methods with available endpoints and roles
-----------
```
POST: /register - all
GET: /cinema-halls - user/admin
POST: /cinema-halls - admin
GET: /movies - user/admin
POST: /movies - admin
GET: /movie-sessions/available - user/admin
POST: /movie-sessions - admin
PUT: /movie-sessions/{id} - admin
DELETE: /movie-sessions/{id} - admin
GET: /orders - user
POST: /orders/complete - user
PUT: /shopping-carts/movie-sessions - user
GET: /shopping-carts/by-user - user
GET: /users/by-email - admin
```
_____________________________
* All incoming and outgoing data converted to JSON format.