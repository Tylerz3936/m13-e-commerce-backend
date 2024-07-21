## E-Commerce Backend API

This project is an E-commerce backend API built with Node.js, Express.js, and Sequelize, connected to a PostgreSQL database. It provides endpoints for managing categories, products, and tags.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- You have installed Node.js and npm.
- You have installed PostgreSQL.
- You have a basic understanding of RESTful APIs and database management.

## Installation

1. **Clone the Repository**

   ```sh
   git clone <repository-url>
   cd <repository-directory>

2. **Install Dependencies**

   ```sh
   npm install

3. **Set up Environment Variables**
    Create a .env file in the root directory and add the following environment variables:
   ```sh
    DB_NAME=your_name
    DB_USER=your_user
    DB_PASSWORD=your_password
    DB_HOST=your_host
    DB_PORT=your_port
4. **Create the Database**
    Ensure your PostgreSQL service is running, then create the database:
   ```sh
    CREATE DATABASE ecommerce_db;
5. **Seed the Database**
    Run the following command to seed the database with initial data:
   ```sh
    npm run seed

## Usage
1. Start the Server
    ```sh
    node server.js
    ```
    The server will start on http://localhost:3001.
2. Test Endpoints 
    Use a tool like Insomnia or Postman to test the API endpoints.

Example Requests
GET /api/products
    - Method: GET
    - URL: http://localhost:3001/api/products

POST /api/products
    - Method: POST
    - URL: http://localhost:3001/api/products
    - Body:
    ```
    {
    "product_name": "New Product",
    "price": 15.99,
    "stock": 100,
    "category_id": 1
    }
    ```
PUT /api/products/
    - Method: PUT
    - URL: http://localhost:3001/api/products/1
    - Body:
    ```
    {
    "product_name": "Updated Product",
    "price": 21.99,
    "stock": 200,
    "category_id": 1
    }
    ```
DELETE /api/products/
    - Method: DELETE
    - URL: http://localhost:3001/api/products/1

Example Endpoints for Categories and Tags
Similar endpoints exist for categories and tags. Replace products with categories or tags in the URL.

## Project Structure
```
|-- config
|   |-- connection.js        # Database connection configuration
|-- db
|-- models
|   |-- Product.js           # Product model
|   |-- Category.js          # Category model
|   |-- Tag.js               # Tag model
|   |-- ProductTag.js        # ProductTag model
|-- routes
|   |-- api
|       |-- product-routes.js    # Product routes
|       |-- category-routes.js   # Category routes
|       |-- tag-routes.js        # Tag routes
|-- seeds
|   |-- index.js             # Seed script
|   |-- category-seeds.js    # Category seed data
|   |-- product-seeds.js     # Product seed data
|   |-- tag-seeds.js         # Tag seed data
|   |-- product-tag-seeds.js # ProductTag seed data
|-- .env.EXAMPLE             # Environment variables example file
|-- package.json             # Project dependencies and scripts
|-- server.js                # Server entry point
```

## Walkthrough
<video controls src="assets/m13-walkthroughdemo.mp4" title="Title"></video>

## Contributing
To contribute to this project, follow these steps:

1. Fork this repository.
2. Create a new branch: git checkout -b feature/your-feature.
3. Make your changes and commit them: git commit -m 'Add some feature'.
4. Push to the branch: git push origin feature/your-feature.
5. Create a pull request.

# Contact
If you have any questions or suggestions about this project, please contact me at tylerzhao103@gmail.com