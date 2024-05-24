# Shoppingo E-commerce API Documentation

Welcome to the documentation for the Shoppingo E-commerce API. This guide provides an overview of the features and functionalities of the API.

## Project Overview

- **Hosted Project**: [Shoppingo API Render URL](https://node-course-e-commerce.onrender.com/)
- **Description**: Shoppingo is an E-commerce API built using Express.js and MongoDB.

## Quick Start

To get started with the Shoppingo API, follow these steps:

1. Clone this repository.
2. Install dependencies using `npm install`.
3. Set up your MongoDB connection string in the `.env` file.
4. Start the server using `npm start`.

## Features

- **User Authentication**: Register, login, and logout functionalities with JWT authentication.
- **User Management**: CRUD operations for managing user accounts.
- **Product Management**: CRUD operations for managing products.
- **Order Management**: Create, update, and view orders.
- **Review Management**: Create, update, and view product reviews.

## Usage

### Authentication

- **Register**: `POST /api/v1/auth/register`
- **Login**: `POST /api/v1/auth/login`
- **Logout**: `GET /api/v1/auth/logout`

### User Management

- **Get All Users**: `GET /api/v1/users`
- **Get Single User**: `GET /api/v1/users/:id`
- **Update User**: `PUT /api/v1/users/:id`
- **Update Password**: `PUT /api/v1/users/:id/password`

### Product Management

- **Get All Products**: `GET /api/v1/products`
- **Get Single Product**: `GET /api/v1/products/:id`
- **Create Product**: `POST /api/v1/products`
- **Update Product**: `PUT /api/v1/products/:id`
- **Delete Product**: `DELETE /api/v1/products/:id`

### Order Management

- **Get All Orders**: `GET /api/v1/orders`
- **Get Single Order**: `GET /api/v1/orders/:id`
- **Create Order**: `POST /api/v1/orders`
- **Update Order**: `PUT /api/v1/orders/:id`

### Review Management

- **Get All Reviews**: `GET /api/v1/reviews`
- **Get Single Review**: `GET /api/v1/reviews/:id`
- **Create Review**: `POST /api/v1/reviews`
- **Update Review**: `PUT /api/v1/reviews/:id`
- **Delete Review**: `DELETE /api/v1/reviews/:id`

## Testing

Test the API endpoints using tools like Postman to ensure proper functionality.
