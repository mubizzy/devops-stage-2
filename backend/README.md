# Backend - FastAPI with PostgreSQL

This directory contains the backend of the application built with FastAPI and a PostgreSQL database.

## Prerequisites

- Python 3.8 or higher
- Poetry (for dependency management)
- PostgreSQL (ensure the database server is running)

### Installing Poetry

To install Poetry, follow these steps:

```sh
curl -sSL https://install.python-poetry.org | python3 -
```

Add Poetry to your PATH (if not automatically added):

## Setup Instructions

1. **Navigate to the backend directory**:
    ```sh
    cd backend
    ```

2. **Install dependencies using Poetry**:
    ```sh
    poetry install
    ```

3. **Set up the database with the necessary tables**:
    ```sh
    poetry run bash ./prestart.sh
    ```

4. **Run the backend server**:
    ```sh
    poetry run uvicorn app.main:app --reload
    ```

5. **Update configuration**:
   Ensure you update the necessary configurations in the `.env` file, particularly the database configuration.

   # Full Stack Web Application Deployment
This project demonstrates the deployment of a full stack web application using React for the frontend, FastAPI for the backend, and PostgreSQL as the database. The application is containerized using Docker and deployed on an AWS EC2 instance.

## Prerequisites

- Node.js and npm installed
- Python 3.9 installed
- PostgreSQL installed
- Docker and Docker Compose installed

## installation 
### Manual Setup

#### Backend

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/repository.git
    cd repository/backend
    ```

2. Create and activate a virtual environment:
    ```sh
    python3 -m venv venv
    source venv/bin/activate
    ```

3. Install dependencies:
    ```sh
    pip install -r requirements.txt
    ```

4. Set up the database:
    ```sh
    psql -U postgres -c "CREATE DATABASE yourdb;"
    psql -U postgres -c "CREATE USER youruser WITH PASSWORD 'yourpassword';"
    psql -U postgres -c "GRANT ALL PRIVILEGES ON DATABASE yourdb TO youruser;"
    ```

5. Configure environment variables in a `.env` file:
    ```env
    DATABASE_URL=postgresql://youruser:yourpassword@localhost:5432/yourdb
    ```

6. Run the application:
    ```sh
    uvicorn main:app --host 0.0.0.0 --port 8000
    ```
