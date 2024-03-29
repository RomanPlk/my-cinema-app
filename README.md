﻿![](https://i.pinimg.com/564x/fc/eb/df/fcebdf9e34ad5d5f1d8f728f781a00ac.jpg)
# Cinema-app
## Project description:
This web application is a simple representation of cinema's ticket reservation system that requires registration or authentication process for access and includes basic CRUD operations. Access to certain functions is limited to the following roles: `USER`, `ADMIN`.
## Features:
➩ registration;

➩ log in;

➩  add / find by email:
* a user

➩  add / get by id / get all:
* a movie / movies
* a cinema hall / cinema halls

➩  add / get by id / find available:
* a movie session

➩  add a session / find by user / register & clear:
* a shopping cart

➩  complete / get a history:
* an order.

All guest users have access to */register* & */login* endpoint.

Users with role `ADMIN` are able to add new movies, movie sessions and cinema halls to DB, as well as update or delete movie session by id and find users by their email addresses. 

As for the authenticated users with role `USER`, they're able to add movie sessions to a shopping cart, check shopping carts details, orders history and complete orders.

## Structure:
Project uses an N-tier architecture with following layers of functionality:

* Controller: processes users' requests and responds to them;
* DAO: operates with data in DB;
* Service: contains all business logic of the application.

## Application technologies:
* JDK **11**
* Apache Maven **3.8.5**
* Apache Tomcat **9.0.65**
* MySQL **8.0.30**
* Hibernate **5.4.27.Final**
* HQL
* Spring Framework (**Core**, **MVC**, **Security**).

## Usage:
Project assumes that you've already installed:

* JDK (*version 11 or higher*)
* Apache Maven
* Apache Tomcat (*version 9.0.65*)
* MySQL and MySQL Workbench
1. Clone this project to your IDE and check errors in *pom.xml* file (if needed):

   `git clone https://github.com/RomanPlk/my-cinema-app`
2. Set up connection to your DB (use file *db.properties* in resources folder):

Below you'll find an example:
   
* db.driver=com.mysql.cj.jdbc.Driver
* db.url=jdbc:mysql://localhost: ... (URL of your schema in MySQL DB)
* db.user= ... (your username from MySQL DB)
* db.password= ... (your password from MySQL DB)

3. Configure Tomcat by choosing Tomcat Server Local. Choose JRE and find "Fix" button: 

![](https://scontent.fifo4-1.fna.fbcdn.net/v/t1.15752-9/301374096_631451522015765_5929056274909479032_n.png?_nc_cat=106&ccb=1-7&_nc_sid=ae9488&_nc_ohc=1Aw-QWd1GiMAX_lnAC4&_nc_ht=scontent.fifo4-1.fna&oh=03_AVLcWdGGlfWBEIru1MOAmExB8r2eLatj-W9hOPvR3SzRzg&oe=63613C08)

select *war exploded* artifact to deploy and change application context to **"/"**:

![](https://scontent.fifo4-1.fna.fbcdn.net/v/t1.15752-9/300024428_5490410521037921_3142103885892112077_n.png?_nc_cat=105&ccb=1-7&_nc_sid=ae9488&_nc_ohc=b32PXP6Q7h4AX8F9MOX&_nc_ht=scontent.fifo4-1.fna&oh=03_AVKp7pFW-xJ_yNe42bSPBQ0nvMZ3wB1QUi45wipCCJjtJg&oe=63620FF5)

4. Fell free to test application using Postman to validate and test requests & responses.
## UML diagram for DB:
![](https://scontent.fifo4-1.fna.fbcdn.net/v/t1.15752-9/323176917_751554619239577_6328043965006958812_n.png?_nc_cat=105&ccb=1-7&_nc_sid=ae9488&_nc_ohc=XyATzD_GtL0AX-hxIEg&_nc_ht=scontent.fifo4-1.fna&oh=03_AdRTChEDdDYa9ljX1bI5OJMMnRioAdCHestk4N_3Lsf9kA&oe=63F3C450)
