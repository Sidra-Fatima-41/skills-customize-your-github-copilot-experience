# 📘 Assignment: Building REST APIs with FastAPI

## 🎯 Objective

Build a small REST API with FastAPI to practice defining routes, validating request data with Pydantic models, and returning appropriate HTTP responses. By the end, you will have an API for managing a collection of books and can explore it through FastAPI's interactive documentation.

## 📝 Tasks

### 🛠️ Create the FastAPI Application

#### Description
Set up a FastAPI application in `main.py` and create an endpoint that confirms the API is running. Start the development server with Uvicorn and use the automatically generated documentation to try the endpoint.

#### Requirements
Completed program should:

- Create a FastAPI application instance in `main.py`
- Add a `GET /` route that returns a JSON message such as `{"message": "Book API is running"}`
- Run the application with `uvicorn main:app --reload`
- Make the root endpoint available at `http://127.0.0.1:8000` and use `/docs` to view the interactive API documentation


### 🛠️ Build Book CRUD Endpoints

#### Description
Represent books as Python data and add routes that allow clients to list, retrieve, create, update, and delete books. Use a Pydantic model to define the fields accepted when a new book is created.

#### Requirements
Completed program should:

- Define a `Book` model with an integer `id`, a non-empty string `title`, a string `author`, and a four-digit publication `year`
- Store at least three books in an in-memory collection
- Implement `GET /books` to return all books
- Implement `GET /books/{book_id}` to return one book by ID
- Implement `POST /books` to validate and add a new book, returning the created book
- Implement `PUT /books/{book_id}` to update an existing book
- Implement `DELETE /books/{book_id}` to remove a book


### 🛠️ Handle Validation and Errors

#### Description
Make the API predictable for clients by validating inputs and returning clear HTTP errors when a requested book does not exist or submitted data is invalid.

#### Requirements
Completed program should:

- Return HTTP status `404` with a helpful detail message when a book ID is not found
- Return HTTP status `201` when a new book is created
- Return HTTP status `204` when a book is successfully deleted
- Reject invalid book data, such as an empty title or a publication year outside a reasonable range, with FastAPI validation errors
- Try successful and failing requests in `/docs` and verify that the response status codes and JSON bodies are correct
