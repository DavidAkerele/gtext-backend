# G-Text Backend

This is the backend of the E-Commerce application, responsible for handling server-side operations, product management, and database interactions.

## Features

- CRUD operations for product management (Create, Read, Update, Delete)
- Database integration with MongoDB for storing products
- RESTful API endpoints for interaction with the frontend
- Error handling and logging for API requests

## Installation

To get started with the project, follow the steps below:

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/e-commerce-backend.git
    ```

2. Install the required dependencies:
    ```bash
    cd e-commerce-backend
    npm install  # Or `yarn install` if you're using Yarn
    ```

3. Set up your environment variables:
    Create a `.env` file in the root of the backend directory with the following content:
    ```
    MONGODB_URI=your-mongo-db-uri
    PORT=5000
    JWT_SECRET=your-jwt-secret
    ```

    - `MONGODB_URI`: Your MongoDB connection string (can use MongoDB Atlas if you're using a cloud database).
    - `PORT`: The port where the backend server will run (default is `5000`).
    - `JWT_SECRET`: A secret key for JWT authentication (if you're using JWT for authentication).

4. Start the development server:
    ```bash
    npm start  # Or `yarn start` if you're using Yarn
    ```

    The server should now be running on `http://localhost:5000`.

## Technologies Used

- **Backend**: Node.js, Express.js
- **Database**: MongoDB (MongoDB Atlas for cloud database hosting)
- **Authentication**: JWT (for secure API requests)
- **Environment Variables**: For sensitive data like MongoDB URI, JWT secret, etc.

## API Endpoints

### 1. Get All Products
- **GET** `/products`
  - Returns a list of all products.
  - Example response:
    ```json
    [
      {
        "_id": "productId1",
        "name": "Product 1",
        "description": "Description of product 1",
        "price": 29.99,
        "image": "url-to-product-image"
      },
      ...
    ]
    ```

### 2. Get Product by ID
- **GET** `/product/:id`
  - Returns the details of a single product.
  - Example response:
    ```json
    {
      "_id": "productId1",
      "name": "Product 1",
      "description": "Description of product 1",
      "price": 29.99,
      "image": "url-to-product-image"
    }
    ```

### 3. Add New Product
- **POST** `/products`
  - Add a new product.
  - Request body (example):
    ```json
    {
      "name": "New Product",
      "description": "New product description",
      "price": 49.99,
      "image": "url-to-image"
    }
    ```
  - Example response:
    ```json
    {
      "_id": "newProductId",
      "name": "New Product",
      "description": "New product description",
      "price": 49.99,
      "image": "url-to-image"
    }
    ```

### 4. Update Product
- **PUT** `/product/:id`
  - Update a product's details by its ID.
  - Request body (example):
    ```json
    {
      "name": "Updated Product",
      "description": "Updated description",
      "price": 59.99,
      "image": "new-image-url"
    }
    ```
  - Example response:
    ```json
    {
      "_id": "productId1",
      "name": "Updated Product",
      "description": "Updated description",
      "price": 59.99,
      "image": "new-image-url"
    }
    ```

### 5. Delete Product
- **DELETE** `/product/:id`
  - Delete a product by its ID.
  - Example response:
    ```json
    {
      "message": "Product deleted successfully"
    }
    ```

## Contributing

Contributions are welcome! Please fork this repository and submit a pull request for any changes.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature-branch`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature-branch`)
5. Create a new Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For any inquiries, you can reach me at [your-email@example.com](mailto:your-email@example.com).
