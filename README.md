# To-Do List Application

This is a simple To-Do List application built with HTML, CSS, JavaScript, and Node.js. The application allows users to create, read, update, and delete (CRUD) to-do items. It also includes user authentication and connects to a MySQL database.

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)

## Features

- User authentication (login and signup)
- Create, read, update, and delete to-do items
- Store user and to-do data in a MySQL database

## Technologies Used

- HTML
- CSS
- JavaScript
- Node.js
- Express.js
- MySQL

## Prerequisites

Before you begin, ensure you have the following installed on your system:

- [Node.js](https://nodejs.org/) (version 12 or later)
- [MySQL](https://dev.mysql.com/downloads/mysql/)

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/PalakonduPavithra/ToDoList.git
   cd todo-app
2. Install the dependencies
   npm install
3. setup MySQL database
   - Start MySQL server and log in using MySQL client:
     mysql -u root -p
   - Create a new database and tables:
     CREATE DATABASE todo_app;
USE todo_app;

CREATE TABLE userdetails (

  userid INT AUTO_INCREMENT PRIMARY KEY,
  
  username VARCHAR(255) NOT NULL,
  
  password VARCHAR(255) NOT NULL
  
);

CREATE TABLE todo (

  todoid INT AUTO_INCREMENT PRIMARY KEY,
  
  userid INT NOT NULL,
  
  titleId INT NOT NULL,
  
  title VARCHAR(255) NOT NULL,
  
  description TEXT NOT NULL,
  
  due_date DATE,
  
  status ENUM('todo', 'inprogress', 'completed'),
  
  FOREIGN KEY (userid) REFERENCES userdetails(userid)
  
);

4. Configure the database connection
   Edit 'server.js' and update the MySQL connection details with your database credentials.
5. Start the server:
   node server.js
   Open a web browser and go to 'http://localhost:3000' to access the application.


## Usage

1. **Sign Up**: Create a new user account.
2. **Log In**: Log in with your credentials.
3. **Create To-Do**: Add new to-do items.
4. **View To-Dos**: View all your to-do items.
5. **Update To-Do**: Edit an existing to-do item.
6. **Delete To-Do**: Remove a to-do item.

## Project Structure

todo-app/

├── node_modules/

├── public/

│   ├── index.html

│   ├── styles.css

│   └── scripts.js

├── server.js

├── package.json

├── package-lock.json

└── README.md

* **public/**: Contains static files (HTML, CSS, JavaScript).
* **server.js**: Node.js server file.
* **package.json**: Project metadata and dependencies.
* **package-lock.json**: Locked versions of project dependencies.
* **README.md**: Project documentation.
