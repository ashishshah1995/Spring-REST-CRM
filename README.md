# Spring-REST-CRM

Developed Sprint REST API application using Spring framework for allowing a client to make **Create, Read, Update and Delete** operations on a list of Customers. 

Used **Jackson Data Binding API** for data binding between JSON and Java POJO. 

Used **Postman** as testing tool for HTTP methods

# Operations

| HTTP Method        | Endpoint           | Crud Action  |
| ------------- |:-------------:| -----:|
| POST     | api/customers | Create a new customer  |
| GET      | api/customers      |   Read a list of customer |
| GET      | api/customers/{customerId}      |   Read a single customer |
| PUT | api/customers     |    Update an existing customer   |
| DELETE | api/customers/{customerId} | Delete a customer |



## Steps to setup the database and Running the appication
```

1. Mysql Database and workbench should be installed to the local machine which the application is going to run. (MySQL can be downlaoded from http://dev.mysql.com/downloads)

2. Open MySql workbench and run these two scripts 
- create-user.sql
- employee-directory.sql

3. Right-Click, select Run As > Run On Server (A tomcat server should have been installed in your local machine)
```

# HTTP Methods
```

GET- http://localhost:8080/spring-crm-rest/api/customers (Selects all customers)

GET- http://localhost:8080/spring-crm-rest/api/customers/1 (Select customer with having the id 1)

POST- http://localhost:8080/spring-crm-rest/api/customers (Insert a new customer)

PUT-  http://localhost:8080/spring-crm-rest/api/customers (Update an existing customer)

DELETE- http://localhost:8080/spring-crm-rest/api/customers/2 (Delete a customer with id 2)

```

![a](https://user-images.githubusercontent.com/26305085/63658429-7b4a9880-c778-11e9-86fb-430518ccd670.gif)
