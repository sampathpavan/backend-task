# Backend-task
Developing Institute Management System using Spring Boot
# Problem Statement
Design and implement a RESTful API using Java and Spring Boot that allows
for the management of institutes, including registration, modification, and retrieval of
institute information.

## Tech stack used
1.) Java 17
2.) Spring Boot
3.) Mysql Database
4.) JUnit and Mockito

## Requirements
1.)IDE
2.)JDK
3.)Database
4.)Postman

# Approach

I followed a three layer architecture to implement the solution.
Repository Layer, Service Layer and Controller Layer.
When client or end user hits the endpoint then the request comes to controller and controller is talking to service and then service is talking to repository layer.
Finally repository layer talks to database and fetches data from database.

## End user -------------> controller -----------> service----------> repository------------>database

## Endpoints used in the project :
1.) For Institute Registration 
------- https://localhost:8081/api/institute/register
## Request format :
{
    "name":"test",
    "location":"test",
    "contactInformation":"7657667787"
}

2.) For Retrieval of Institute based on Id
------- https://localhost:8081/api/institute/getById/{id}
3.) For Updating the Institute based on id
------- https://localhost:8081/api/institute/update/{id}
## Request format
{
    "name":"test",
    "location":"test",
    "contactInformation":"9768973654"
}
# Workflow
-> Create different packages which includes Entity, Repository, Service, Controller, Validation.
-> Create an Entity class with required fields and provide getters and setters as this is required to create a table in db (create a schema in db initially).
-> Create a Repository interface which extends Jpa Repository which is useful in talking to db which has various methods to perform CRUD operations.
-> Create a Service Interface in which we define all our methods to implement and next we create a class which implements the interface in which we write all the business logic
-> Create a Controller class where we define all our endpoints.
-> Create a Validation class to customize the validation response.

# Testing the application
-> Tested each layer using junit and mockito


