# 📘 Assignment: Testing Python Applications with pytest

## 🎯 Objective

Learn how to use `pytest` to write reliable automated tests for Python code. You will test both ordinary functions and a FastAPI endpoint, then use fixtures and parametrized tests to reduce duplication and cover important edge cases.

## 📝 Tasks

### 🛠️ Write Unit Tests for Python Functions

#### Description
Create a module named `calculator.py` with small, focused functions and test it from `test_calculator.py`. Run the tests with the `pytest` command.

#### Requirements
Completed program should:

- Implement `add(a, b)`, `divide(a, b)`, and `is_even(number)` in `calculator.py`
- Include tests for normal inputs and at least one boundary or edge case for each function
- Verify that dividing by zero raises `ZeroDivisionError` using `pytest.raises`
- Run all tests successfully with `pytest`


### 🛠️ Test a FastAPI Endpoint

#### Description
Create a small FastAPI application with a `GET /books/{book_id}` endpoint and use FastAPI's `TestClient` to test it without starting a live server.

#### Requirements
Completed program should:

- Return a book and HTTP status `200` when a valid book ID is requested
- Return HTTP status `404` and a useful error detail for an unknown book ID
- Use `TestClient` in `test_main.py` to send requests to the application
- Assert both response status codes and important JSON response fields


### 🛠️ Improve Test Coverage with Fixtures and Parameters

#### Description
Refactor repeated test setup into a pytest fixture and use parametrization to check several inputs with one test function. Include a short test summary in your submission.

#### Requirements
Completed program should:

- Define and use at least one `pytest.fixture` for shared test data or client setup
- Use `@pytest.mark.parametrize` to test at least three input/output combinations
- Include a test for invalid input or an empty collection
- Pass all tests and report the total number of tests run
- Add at least one new test after reviewing the behavior covered by the original tests
