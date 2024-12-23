# To-Do List Application with Spring Boot 3.3.7

This is a simple To-Do List application built with **Spring Boot 3.3.7**. It allows users to add, view, delete, and toggle the status of tasks. The application uses **Thymeleaf** for rendering HTML templates and **MySQL** as the database.

## Features
- View all tasks in the list.
- Add new tasks with a title.
- Delete tasks by their ID.
- Toggle the completion status of tasks (completed/incomplete).

## Prerequisites

Before running the application, make sure you have the following installed:

- **Java 17** or higher (for Spring Boot 3.3.7).
- **Maven** or **Gradle**.
- **MySQL** server running.
- A browser to access the application.

## Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/tarikii/todoapp-springboot.git
cd todoapp-spring-boot
```
### 2. Set Up MySQL Database
```bash
CREATE DATABASE todoapp;
```
#### Update the application.properties or application.yml file to match your MySQL configuration:
```bash
# Application name
spring.application.name=todoapp

# JDB Connection Details
spring.datasource.url=jdbc:mysql://localhost:3306/todoapp
spring.datasource.username=root
spring.datasource.password=password

# JPA Configuration
spring.jpa.hibernate.ddl-auto=update
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQLDialect
```

## Architecture

The application is structured with a basic Model-View-Controller (MVC) architecture:
  - Controller: Handles HTTP requests and directs them to the appropriate service methods.
  - Service: Contains the business logic for task management (adding, deleting, and toggling tasks).
  - Model: Represents the Task entity with an id, title, and completed status.
  - Repository: Interfaces with the MySQL database to store and retrieve tasks.

## Endpoints
  - GET / - View all tasks.
  - POST / - Add a new task with a title.
  - GET /tasks/{id}/delete - Delete a task by its ID.
  - GET /tasks/{id}/toggle - Toggle the completion status of a task.

## Technologies Used
  - Spring Boot 3.3.7 - The core framework for building the application.
  - Thymeleaf - Template engine for rendering HTML views.
  - MySQL - Database for storing tasks.
  - Spring Data JPA - For interacting with the MySQL database and managing entities.
  - Spring MVC - Architecture for handling HTTP requests and responses.

