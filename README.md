# TodoApp
A high-performance asynchronous Todo API built with Sanic and Tortoise-ORM.

## Overview
TodoApp is a RESTful API service for task management, built using modern Python asynchronous frameworks. It provides endpoints for creating, reading, updating, and deleting tasks, along with user authentication functionality.

## Features
High-performance asynchronous API using Sanic
User authentication with secure password hashing
Complete CRUD operations for todo items
PostgreSQL database with Tortoise-ORM

## Tech Stack
Sanic: Fast asynchronous web framework
Tortoise-ORM: Async ORM for Python
PostgreSQL: Relational database
bcrypt: Password hashing library
Aerich: Database migration tool

##  Installation
### Clone the repository:
bashgit clone https://github.com/yourusername/todoapp.git
cd todoapp

### Create a virtual environment:
bashpython -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

### Install dependencies:
bashpip install -r requirements.txt

### Configure your PostgreSQL settings in config.py
Initialize the database:
bashaerich init-db


## Running the Application
### Start the server:
bashpython app.py
The API will be available at http://localhost:8000

## Testing
This API has been thoroughly tested using POSTMAN:
Import the included POSTMAN collection file to quickly test all endpoints
Test authentication flows, error handling, and successful operations
Verify request/response formats and status codes

## Todo Operations
GET /todos - List all todos for the authenticated user
POST /todos - Create a new todo
GET /todos/{id} - Get a specific todo
PUT /todos/{id} - Update a specific todo
DELETE /todos/{id} - Delete a specific todo

🔧 Project Structure
todoapp/
├── app.py                  # Main application file
├── config.py               # Configuration settings
├── requirements.txt        # Project dependencies
├── db/
│   └── init.py             # Database initialization
├── models/
│   ├── todo.py             # Todo model
│   └── user.py             # User model
├── routes/
│   ├── todo_routes.py      # Todo endpoints
│   └── user_routes.py      # User authentication endpoints
