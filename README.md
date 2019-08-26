# Spring-REST-CRM

Build Sprint REST API application using Spring framework for allowing a client to make **Create, Read, Update and Delete** operations on a list of Customers. 

# Operations

| HTTP Method        | Endpoint           | Crud Action  |
| ------------- |:-------------:| -----:|
| POST     | api/customers | Create a new customer  |
| GET      | api/customers      |   Read a list of customer |
| GET      | api/customers/{customerId}      |   Read a single customer |
| PUT | api/customers     |    Update an existing customer   |
| DELETE | api/customers/{customerId} | Delete a customer |

## Steps to setup the database

1. Mysql Database and workbench should be installed to the local machine which the application is going to run. (MySQL can be downlaoded from http://dev.mysql.com/downloads)

2. Open MySql workbench and run these two scripts 
- create-user.sql
- employee-directory.sql


# Running the application:


a. Select the root project folder

b. Right-Click, select Run As > Run On Server (A tomcat server should have been installed in your local machine)



d. EMPLOYEE role can perform following;

  1. Get a list of all customers. GET /api/customers
  2. Get a single customer. GET /api/customers/{customerId}
  
  MANAGER role can perform following in addition to EMPLOYEE;
  
  1. Add a new customer. POST /api/customers
  2. Update an existing customer. PUT /api/customers
  
  ADMIN role can perform following in addition to MANAGER;
  
  1. Delete a customer. DELETE /api/customers/{customerId}

  User 'susan' with the password test123 has the admin rights, can perform all actions.

 
e. If you have Postman installed, you may make the following HTTP requests (Do not forget to enter the credentials as
susan, test123 in the authorization tab); 


GET http://localhost:8080/spring-crm-rest/api/customers (Selects all customers)
GET http://localhost:8080/spring-crm-rest/api/customers/1 (Select customer with having the id 1)
POST http://localhost:8080/spring-crm-rest/api/customers (Insert a new customer)

Body;

{
  "id":0,
  "firstName": "Gorkem",
  "lastName": "Turan",
  "email": "gorkem@luv2code.com"
}

PUT http://localhost:8080/spring-crm-rest/api/customers (Update the customer with having the id 6)
  
Body;

{
  "id":6,
  "firstName": "Gorkem",
  "lastName": "Turan",
  "email": "gorkem.turan@luv2code.com"
}

DELETE http://localhost:8080/spring-crm-rest/api/customers/6 (Delete the customer with the id 6)

![a](https://user-images.githubusercontent.com/26305085/63658429-7b4a9880-c778-11e9-86fb-430518ccd670.gif)
