# Flask CRUD API with PostgreSQL

This project is a simple Flask-based web application that provides CRUD (Create, Read, Update, Delete) operations on a `Person` entity, with PostgreSQL as the database backend. The application is containerized using Docker and can be easily set up and tested with `docker-compose`.

## Features
- Create, Read, Update, Delete operations on a `Person` entity.
- RESTful API with JSON responses.
- PostgreSQL database integration using SQLAlchemy.
- Dockerized application with `docker-compose`.
- Unit tests using `pytest`.
- Deployed with `gunicorn` for production.

## Technologies Used
- **Flask**: Web framework.
- **Flask-SQLAlchemy**: ORM for database interactions.
- **PostgreSQL**: Relational database.
- **Docker**: Containerization.
- **pytest**: Unit testing framework.
- **pydantic**: Data validation.
- **gunicorn**: WSGI server for production.

## Project Structure
├── app.py # Main application code

├── Dockerfile # Docker image configuration

├── docker-compose.yml # Docker Compose configuration

├── requirements.txt # Python dependencies

├── u_test.py # Unit tests using pytest

└── README.md # Project documentation

## API Endpoints

### Test Route:
- **GET** `/test`: Returns a message confirming the API is working.

### Create a Person:
- **POST** `/person`: Creates a new person.
- Request body (JSON):
    ```json
    {
      "name": "John",
      "family": "Doe",
      "email": "john@example.com"
    }
    ```

### Get All People:
- **GET** `/person`: Retrieves a list of all people.

### Get a Person by ID:
- **GET** `/person/<id>`: Retrieves a person by their ID.

### Update a Person:
- **PUT** `/person/<id>`: Updates a person by their ID.
- Request body (JSON):
    ```json
    {
      "name": "John",
      "family": "Doe",
      "email": "john@example.com"
    }
    ```

### Delete a Person:
- **DELETE** `/person/<id>`: Deletes a person by their ID.

---

## Running Tests

To run the unit tests using `pytest`, follow these steps:

1. **Bring up the containers** (if they are not already running):
    ```bash
    docker-compose up --build
    ```

2. **Run tests**:
    In another terminal window, run:
    ```bash
    docker-compose exec flask_app pytest
    ```

This will execute the unit tests defined in the `u_test.py` file.

---

## Environment Variables

- **DB_URL**: PostgreSQL connection string. Set in the `docker-compose.yml` file.

Example:
```yaml
DB_URL: postgresql://postgres:123@flask_db:5432/test

