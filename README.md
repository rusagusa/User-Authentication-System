# User-Authentication-System
Auth App - Local Setup

This is a simple user authentication system built with Node.js, Express, MySQL, JWT, and Tailwind CSS.

Prerequisites

Node.js installed (v18+ recommended)

MySQL installed or access to a MySQL database

npm (comes with Node.js)

Git (optional)


Setup Steps

1. Clone the repository

git clone <YOUR_REPO_URL>
cd auth-app

2. Install dependencies

npm install

3. Configure environment variables

Create a .env file in the root of the project:

DB_HOST=localhost
DB_USER=root
DB_PASSWORD=YOUR_PASSWORD_HERE
DB_NAME=authdb
DB_PORT=3306
JWT_SECRET=your_secret_key
PORT=5000

> Replace the values with your MySQL credentials and desired JWT secret.

4. Create MySQL database and table

CREATE DATABASE authdb;
USE authdb;

CREATE TABLE users (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(100) NOT NULL,
  email VARCHAR(100) NOT NULL UNIQUE,
  password VARCHAR(255) NOT NULL
);

5. Start the server

npm start

The server will start at http://localhost:5000.

6. Access the app

Open your browser and go to http://localhost:5000 to see the frontend. You can register, log in, and access the dashboard.

Notes

The frontend files are in the public/ folder.

JWT tokens are stored in localStorage in the browser.

Passwords are hashed with bcrypt before being saved to the database.



