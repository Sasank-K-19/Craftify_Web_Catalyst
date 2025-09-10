# Craftify_Web_Catalyst

This is a comprehensive e-commerce platform for handcrafted goods, built with a modern, scalable architecture. It provides a robust set of API endpoints for user authentication, product management, reviews, and order processing.

## API Endpoints

The backend server provides the following RESTful API endpoints, categorized by functionality:

### 🔐 Auth

  * `POST /api/auth/register`: Creates a new user account with a specified role (`buyer` or `seller`).
  * `POST /api/auth/login`: Authenticates a user and returns a JSON Web Token (JWT).
  * `GET /api/auth/me`: Retrieves the profile of the currently authenticated user.

### 📦 Products

  * `GET /api/products`: Retrieves a paginated list of all products with support for filtering and sorting.
  * `GET /api/products/featured`: Retrieves a curated list of featured products.
  * `GET /api/products/:id`: Retrieves a single product by its unique ID.
  * `POST /api/products`: Creates a new product. (Requires `seller` or `admin` role)
  * `PUT /api/products/:id`: Updates an existing product. (Requires `seller` or `admin` role)
  * `DELETE /api/products/:id`: Deletes a product. (Requires `seller` or `admin` role)

### 💬 Reviews

  * `POST /api/products/:id/reviews`: Adds a review to a product. (Requires `buyer` role)
  * `PUT /api/products/:productId/reviews/:reviewIndex/reply`: Allows a seller to add a reply to a review on their product. (Requires `seller` or `admin` role)

### 🛒 Orders

  * `POST /api/orders`: Creates a new order for the authenticated user.
  * `GET /api/orders`: Retrieves the authenticated buyer's order history.
  * `GET /api/orders/seller`: Retrieves all orders containing a seller's products. (Requires `seller` or `admin` role)
  * `PUT /api/orders/:id/status`: Updates the status of an order (e.g., "shipped," "delivered"). (Requires `seller` or `admin` role)

## How to Use the Application

Once the application is running, you can:

  * **Register as a Buyer:** Create an account with the `buyer` role to browse products, leave reviews, and place orders.
  * **Register as a Seller:** Create an account with the `seller` role to list your handcrafted items for sale.
  * **Manage Your Products:** If you're a seller, use the dashboard to add new items or manage existing ones.
  * **Explore and Purchase:** As a buyer, use the search and filter options to find unique crafts and complete the simulated checkout process to place an order.

## Contributing

Contributions are what make the open-source community an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

To contribute to this project:

1.  **Fork the Project:** Click the "Fork" button at the top right of this repository.
2.  **Create your Feature Branch:**
    ```bash
    git checkout -b feature/AmazingFeature
    ```
3.  **Commit your Changes:**
    ```bash
    git commit -m 'Add some AmazingFeature'
    ```
4.  **Push to the Branch:**
    ```bash
    git push origin feature/AmazingFeature
    ```
5.  **Open a Pull Request:** Create a pull request to the `main` branch of this repository, describing your changes in detail. You can also simply open an issue with the tag "enhancement" to suggest improvements.
