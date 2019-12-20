# Building the Bangazon Platform API

Welcome, new Bangazonians!

We have built out a .NET Web API that makes each resource in the Bangazon ERD available to application developers throughout the entire company.

1. Products
1. Product types
1. Customers
1. Orders
1. Payment types
1. Employees
1. Computers
1. Training programs
1. Departments


Our product owner will provide a prioritized backlog of features to work on over the development sprint. The first version of the API will be completely open since we have not determined which authentication method we want to use yet.



## Plan

First, you need to plan.

- The team needs to use the official SQL script (see below) and use your ERD.

## Restore Packages

When you clone down this code, run `dotnet restore` twice-- first in the API project and second in the Test project to restore all of the dependencies. Your app will not run without this step. Once you have done this, open the project with Visual Studio 2019, be sure you have a connection to the database, and run your code.

## Modeling

Each model has the approprate foreign key relationship defined on it.

## Database Management

You will be using the [Official Bangazon SQL](./BangazonAPI/bangazon-api.sql) file to seed your database. Create the database using the SQL Server Object Explorer in Visual Studio and then run the provided SQL file on the new database. Every team member will need to build the database on their own computer.

## Controllers

Controllers will handle GET, POST, PUT, and (conditional) DELETE operations on each resource.

## Test Classes

Each feature has integration testing.



## To test for each feature:


### Products:
Endpoint: /api/product
supported HTTP Methods: (GET All, GET Single (by ID), POST, PUT, DELETE)

### Product types:
Endpoint: /api/producttype
supported HTTP Methods: (GET All, GET Single (by ID), POST, PUT, DELETE)

### Customers:
Endpoint: /api/customer
GET, POST, PUT, and DELETE methods supported.


### Orders:
Endpoint - /api/order
GET, POST, PUT, and DELETE methods supported.

### Payment types:
Endpoint: /api/paymenttype
supported HTTP Methods: (GET All, GET Single (by ID), POST, PUT, DELETE


### Departments:
Endpoint: /api/department
supported HTTP Methods: (GET All, GET Single (by ID), POST, PUT)
Additional queries:  ~department?_include=employees, will show all the employees in a department
        ~department?_filter=budget&_gt={number} will show all the departments with a budget greater than {number}

### Employees:

### Computers:

### Training programs:

### Employee Training
