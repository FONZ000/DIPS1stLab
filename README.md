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

├── app.py # Main application code\
├── Dockerfile # Docker image configuration 
├── docker-compose.yml # Docker Compose configuration 
├── requirements.txt # Python dependencies 
├── u_test.py # Unit tests using pytest 
└── README.md # Project documentation


## Setup

### Prerequisites

Ensure you have the following installed on your machine:

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

### Steps to Run Locally

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd <repository-directory>
