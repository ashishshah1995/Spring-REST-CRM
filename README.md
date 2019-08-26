# Spring-REST-CRM

Build Sprint REST API application using Spring framework for allowing a client to make **Create, Read, Update and Delete** operations on a list of Customers. 

# Operations

1. `GET` - 
2.  `POST`
3. `PUT`-
4.  `DELETE`-

| HTTP Method        | Endpoint           | Crud Action  |
| ------------- |:-------------:| -----:|
| POST     | api/customers | Create a new customer  |
| GET      | api/customers      |   Read a list of customer |
| GET      | api/customers/{customerId}      |   Read a single customer |
| PUT | api/customers     |    Update an existing customer   |
| DELETE | api/customers/{customerId} | Delete a customer |
## Steps to set database

1. Mysql Database and workbench should be installed to the local machine which the application is going to run. (MySQL can be downlaoded from http://dev.mysql.com/downloads)

2. Open MySql workbench and run these two scripts 
- create-user.sql
- employee-directory.sql

These scripts would create a db user called springstudent, create the DB schema called employee_directory create a Employee table and populate the Employee table.

# Starting the application:

a. Select the root project folder

b. SpringbootCrudDemoApplication.java

c. If you have Postman installed, you may make the following HTTP requests; 


GET http://localhost:8080/springboot-crud-demo/api/employees (Selects all employees)
GET http://localhost:8080/springboot-crud-demo/api/employees/1 (Select the employee  with having the id 1)
POST http://localhost:8080/springboot-crud-demo/api/employees (Insert a new employee)

Body;

{
  "id":0,
  "firstName": "Gorkem",
  "lastName": "Turan",
  "email": "gorkem@luv2code.com"
}

PUT http://localhost:8080/springboot-crud-demo/api/employees (Update the customer with having the id 6)
  
Body;

{
  "id":6,
  "firstName": "Gorkem",
  "lastName": "Turan",
  "email": "gorkem.turan@luv2code.com"
}

DELETE http://localhost:8080/springboot-crud-demo/api/employees/6 (Delete the customer with the id 6)

![a](https://user-images.githubusercontent.com/26305085/63658429-7b4a9880-c778-11e9-86fb-430518ccd670.gif)
