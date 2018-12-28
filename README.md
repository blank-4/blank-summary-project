# \_blank: Summary Project

## Prerequisites

Having Completed the [exercise 8] (https://github.com/blank-project/blank-exercises/tree/master/javascript/lesson8) of the JavaScript lesson.

## Features

The goal is to update Exercise 8 to change how the data is stored. As a reminder, in the project, the data is stored *locally*, that is to say that they are only accessible on the computer or the phone (the host) on which the application is used.

For this project, the data will be stored in a database, and accessible via a web application.
The ToDo application will communicate with this application using a client-server protocol.

## Instructions

### API

- Define an API for your Web Application :
  - Tasks :
    - Path, Protocol, Request and Response Data for Creation
    - Path, Protocol, Request and Response Data for Reading and Filtering tasks
    - Path, Protocol, Request and Response Data for Update
    - Path, Protocol, Request and Response Data for Archiving
    - Path, Protocol, Request and Response Data for Deletion
  - Tasks Category :
    - Path, Protocol, Request and Response Data for Creation
    - Path, Protocol, Request and Response Data for Update
    - Path, Protocol, Request and Response Data for Deletion
  
Example for Task Deletion  
**Use case** : deletion of an exisiting Task  
**Path** : `/tasks/{id}/delete`  
**Protocol** : POST  
**Request Data** :  
 - id {String, required} : the id of the task to delete
**Response Data** :
 - if deletion is successful :
   - HTTP 200
   - No body
 - if no task with the given id exists :
   - HTTP 404
   - No body
 - if there is a technical error (can not connect to DataBase, Error in the Middleware)
   - HTTP 500
   - No Body

### Implementation

Once the API is defined and validated, implement it in a Web Server using MongoDB and Express.js :
- Create a controller for Tasks named TaskController
- For each action (Create, Read, Update, Archive, Delete), create a route bound to the path and method defined in yout API.
- Implement each action in the route (write the code in the middleware so that it does what is written in the API).



