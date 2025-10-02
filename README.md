# cookies
# User Authentication System

This project is a Node.js-based user authentication system that allows users to register and log in securely. It uses a PostgreSQL database to store user credentials and implements password hashing for security.

## Features

- User registration with email and password.
- Password hashing using `bcrypt` for secure storage.
- Login functionality with `passport.js` for authentication.
- Redirects users to a protected route upon successful login.

## Prerequisites

Before running this project, ensure you have the following installed:

- [Node.js](https://nodejs.org/)
- [PostgreSQL](https://www.postgresql.org/)
- [npm](https://www.npmjs.com/)

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>

   
## Install dependencies:
 npm install

## Set up the database:

## Create a PostgreSQL database.
## Create a users table with the following schema:

CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  email VARCHAR(255) UNIQUE NOT NULL,
  password TEXT NOT NULL
);


## Configure environment variables:

Create a .env file in the root directory and add the following:

-hostDB_HOST=<your-database>
DB_USER=<your-database-user>
DB_PASSWORD=<your-database-password>
DB_NAME=<your-database-name>
SALT_ROUNDS=10

Open your browser and navigate to http://localhost:3000.

Register a new user or log in with existing credentials.

Dependencies
express: Web framework for Node.js.
bcrypt: Library for hashing passwords.
passport: Authentication middleware for Node.js.
pg: PostgreSQL client for Node.js.
File Structure
index.js: Main server file containing routes and logic.
views/: Directory for frontend templates (if applicable).
public/: Directory for static files (if applicable).
Security Notes
Passwords are hashed using bcrypt before being stored in the database.
Ensure your .env file is not committed to version control.

Future Improvements
Add email verification during registration.
Implement session management for better security.
Add support for OAuth-based authentication (e.g., Google, Facebook).
License
This project is licensed under the MIT License.

## Acknowledgments
bcrypt
passport.js
Express.js
