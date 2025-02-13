# FastAPI Book Catalog

## Overview

The **FastAPI Book Catalog** is a RESTful API built with **FastAPI**, designed to manage a collection of books efficiently. This API supports full **CRUD (Create, Read, Update, Delete)** operations, allowing users to:

- Fetch all books
- Search books by **title**, **author**, or **category**
- Add new books
- Update existing book details
- Remove books from the inventory

This API is ideal for managing an online bookstore or personal book collection.

---

## Endpoints

### 📚 Fetch Books

- **GET** `/books` - Retrieves all books in the inventory.
- **GET** `/books/{book_title}` - Fetches details of a specific book by its title.
- **GET** `/books/?category={category}` - Retrieves books filtered by category.
- **GET** `/books/{book_author}/?category={category}` - Retrieves books written by a specific author within a category.
- **GET** `/Books/{author}/` - Fetches all books from a given author.

### ✍️ Manage Books

- **POST** `/books/create_book` - Adds a new book to the inventory.
  - **Request Body**: JSON payload with book details.
- **PUT** `/books/update_book` - Updates an existing book's details.
  - **Request Body**: JSON payload with updated book information.
- **DELETE** `/books/delete_book/{book_title}` - Removes a book from the inventory by title.

---

## Data Model

Each book is stored in memory as a dictionary within a Python list (`BOOKS`). The book structure includes the following attributes:

- ``: Title of the book
- ``: Author of the book
- ``: Genre or classification
- ``: Unique identifier for the book
- ``: Cost of the book
- ``: Number of copies available in the inventory

---

## 🔧 Usage

Follow these steps to set up and run the FastAPI Book Catalog:

1. **Clone the repository**:

   ```sh
   git clone https://github.com/your-username/fastapi-book-catalog.git
   cd fastapi-book-catalog
   ```

2. **Install dependencies**:

   ```sh
   pip install -r requirements.txt
   ```

3. **Run the FastAPI application**:

   ```sh
   uvicorn main:app --reload
   ```

4. **Access the API**:

   - Use **Postman**, **cURL**, or any API testing tool to interact with the endpoints.
   - Open [**http://127.0.0.1:8000/docs**](http://127.0.0.1:8000/docs) in a browser to view the interactive API documentation (powered by **Swagger UI**).

---

## 📌 Notes

- The API is designed to run in memory and does not use a database. Restarting the application will reset the inventory.
- FastAPI automatically generates OpenAPI documentation, accessible at `/docs` or `/redoc`.

Feel free to contribute and enhance the functionality of this FastAPI-based book catalog! 🚀

