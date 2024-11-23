# Logistics Management System - Backend

Welcome to the backend repository of the Logistics Management System. This system is designed to manage vehicles, items, orders, and customers for a logistics company.

## Table of Contents

- [Introduction](#introduction)
- [Getting Started](#getting-started)
- [API Documentation](#api-documentation)
- [Authentication](#authentication)
- [Logging](#logging)
- [Error Handling](#error-handling)
- [Project Directory Explanation](#project-directory-explanation)

## Introduction

This backend repository contains the server code for the Logistics Management System. It's built using the MERN (MongoDB, Express, React, Node.js) stack and provides APIs for managing items, customers, delivery vehicles, and orders.

## Getting Started

1. Clone the repository:

   ```
   git clone https://github.com/TeddyMeg/track-order.git
   ```

2. Navigate to the project directory:

   ```
   cd view

   ```

3. Install backend dependencies:

   ```
   npm install
   ```

4. Install frontend dependencies:
   ```
   cd view
   npm install
   ```

## Usage

1. Start the backend server:

   ```
   npm server
   ```

   The backend server will run on http://localhost:8080.

2. Start the frontend development server:

   ```
   cd view
   npm start
   ```

   The frontend development server will run on http://localhost:3000.

## Technologies

- Backend:

  - Node.js
  - Express.js
  - MongoDB (or your chosen database)
  - Bcrypt.js (for user authentication)
  - JWT (JSON Web Tokens) for secure user sessions

- Frontend:
  - React
  - React Router (for routing)
  - Redux (for state management)
  - Axios (for API requests)

---

### Environment Variables

#### Backend Environment Variables

Create a `.env` file in your backend project's root directory and add the following environment variables:

```dotenv
MongoDB_URL = YOUR_MONDO_DB_URL
PORT = 8080

```

- `MongoDB_URL`: MongoDB connection URL.
- `PORT`: Port number for the backend server.

## API Documentation

### User Authentication

- `POST /api/users/register`: Register a new user.
- `POST /api/users/login`: Log in and obtain a JWT token for authentication.

### Items

- `GET /api/items`: Retrieve a list of all items.
- `GET /api/items/:id`: Retrieve details of a specific item.
- `POST /api/items`: Create a new item.
- `PUT /api/items/:id`: Update an existing item.
- `DELETE /api/items/:id`: Delete an item.

### Customers

- `GET /api/customers`: Retrieve a list of all customers.
- `GET /api/customers/:id`: Retrieve details of a specific customer.
- `POST /api/customers`: Create a new customer.
- `PUT /api/customers/:id`: Update an existing customer.
- `DELETE /api/customers/:id`: Delete a customer.

### Delivery Vehicles

- `GET /api/delivery-vehicles`: Retrieve a list of all delivery vehicles.
- `GET /api/delivery-vehicles/:id`: Retrieve details of a specific delivery vehicle.
- `POST /api/delivery-vehicles`: Create a new delivery vehicle.
- `PUT /api/delivery-vehicles/:id`: Update an existing delivery vehicle.
- `DELETE /api/delivery-vehicles/:id`: Delete a delivery vehicle.

### Orders

- `GET /api/orders`: Retrieve a list of all orders.
- `GET /api/orders/:id`: Retrieve details of a specific order.
- `POST /api/orders`: Create a new order.
- `PUT /api/orders/:id`: Update an existing order.
- `DELETE /api/orders/:id`: Delete an order.
- `PUT /api/orders/:id/mark-delivered`: Mark an order as delivered.

For protected routes, include the JWT token in the `Authorization` header.

## Authentication

This backend uses token-based authentication with JSON Web Tokens (JWT). To access protected routes, include a valid JWT token in the `Authorization` header.

To obtain a token, use the `/users/login` route with valid credentials. The response will include a token that should be included in subsequent requests.

## Logging

This backend logs HTTP requests using the `morgan` middleware. Logs are written to an `access.log` file.

## Error Handling

The backend includes basic error handling for API routes. Errors are returned in a standardized format with appropriate HTTP status codes.

## Project Directory Explanation

The project directory is organized as follows:

```
/project-root
│
├── /frontend                # Contains the frontend application code
│   ├── /public              # Public assets (index.html, favicon, etc.)
│   ├── /src                 # Source code for the React application
│   │   ├── /components      # Reusable React components
│   │   ├── /pages           # Page components for different routes
│   │   ├── /store           # Redux store configuration and actions
│   │   ├── /styles          # CSS or styled-components for styling
│   │   └── index.js         # Entry point for the React application
│   │
│   └── package.json         # Frontend dependencies and scripts
│
├── /backend                 # Contains the backend application code
│   ├── /controllers         # Business logic for handling requests
│   ├── /models              # Database models (e.g., Mongoose schemas)
│   ├── /routes              # API route definitions
│   ├── /middleware          # Custom middleware for authentication, logging, etc.
│   ├── /config              # Configuration files (e.g., database connection)
│   └── server.js            # Entry point for the backend application
│
└── README.md                # Project documentation
```

### Explanation of Key Directories and Files:

- **/frontend**: This directory contains the code for the frontend application built with React. It includes components, pages, and styles.
- **/public**: Contains static files that are served directly, such as the main HTML file and images.
- **/src**: The main source code for the React application.
  - **/components**: Contains reusable React components that can be used across different pages.
  - **/pages**: Contains components that represent different pages in the application, typically corresponding to routes.
  - **/store**: Contains Redux store configuration, actions, and reducers for state management.
  - **/styles**: Contains CSS files or styled-components for styling the application.
  - **index.js**: The entry point for the React application where the app is rendered.
- **/backend**: This directory contains the code for the backend application, typically built with Node.js and Express.
  - **/controllers**: Contains the business logic for handling API requests.
  - **/models**: Contains database models, such as Mongoose schemas for MongoDB.
  - **/routes**: Defines the API routes for the application.
  - **/middleware**: Contains custom middleware functions for tasks like authentication and logging.
  - **/config**: Contains configuration files, such as database connection settings.
  - **server.js**: The entry point for the backend application where the server is set up and started.
- **README.md**: The documentation file that provides an overview of the project, setup instructions, and other relevant information.




