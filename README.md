# NodeJS Project - Product Management API

This NodeJS project comprises an API for managing products, allowing users to retrieve products based on various criteria, including filtering, sorting, and pagination.

## Setup

1. **Installation:**

   - Ensure Node.js is installed on your machine.
   - Clone this repository.
   - Run `npm install` to install dependencies.

2. **Database Configuration:**

   - Configure your database settings in `./config/database.js`.
   - The project currently uses MongoDB for data storage.

3. **Environment Variables:**

   - Set up environment variables (if necessary) in a `.env` file.

4. **Start Server:**
   - Run `npm start` to start the server.

## Project Structure

The project structure is as follows:

- **Controllers:** Handle business logic and interaction with the database.

  - `controllers/products.js`: Contains methods for retrieving products with different query parameters.

- **Models:** Define database schemas and models.

  - `models/product.js`: Defines the schema for the product model.

- **Routes:** Define API endpoints.

  - `routes/products.js`: Contains routes for accessing product-related functionality.

- **Utilities:**
  - `config/database.js`: Configuration for the database connection.

## Functionality

### `getAllProductsStatic`

- **Route:** `/static`
- **Method:** GET
- **Description:** Retrieves products based on a static filter (products with prices greater than $30).
- **Response:** Returns a JSON object containing filtered products and the count of products retrieved.

### `getAllProducts`

- **Route:** `/`
- **Method:** GET
- **Description:** Retrieves products based on various query parameters like featured status, company, name, sorting, pagination, and specific field selection.
- **Query Parameters:**
  - `featured`: Filter by featured status (true/false).
  - `company`: Filter by company name.
  - `name`: Filter by product name (case-insensitive, supports regex).
  - `sort`: Sort the results by specific fields.
  - `fields`: Select specific fields to be included in the response.
  - `numericFilters`: Filter products based on numeric criteria for fields like price and rating.
  - `page` (optional): Pagination for result pages.
  - `limit` (optional): Limit the number of products per page.
- **Response:** Returns a JSON object containing filtered and paginated products, along with the count of products retrieved.

## Usage

- Use API endpoints `/static` and `/` with appropriate query parameters to retrieve products based on specific criteria.
- Utilize the provided functionalities for filtering, sorting, pagination, and field selection according to your requirements.

## Note

- Ensure proper database connectivity and valid query parameters for expected functionality.
- Handle errors gracefully and validate user input to prevent potential issues.

Feel free to explore and integrate these functionalities into your applications!

For any further assistance or inquiries, please refer to the documentation or contact the project contributors.

---

_(Make sure to update the README with any additional configurations, dependencies, or changes pertinent to your project.)_
