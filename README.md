# Full-Stack FastAPI and React Template

Welcome to the Full-Stack FastAPI and React template repository. This repository serves as a demo application for interns, showcasing how to set up and run a full-stack application with a FastAPI backend and a ReactJS frontend using ChakraUI.

## Project Structure

The repository is organized into two main directories:

- **frontend**: Contains the ReactJS application.
- **backend**: Contains the FastAPI application and PostgreSQL database integration.

Each directory has its own README file with detailed instructions specific to that part of the application.

## Getting Started

To get started with this template, please follow the instructions in the respective directories:

- [Frontend README](./frontend/README.md)
- [Backend README](./backend/README.md)

# Full Stack Web Application Deployment
This project demonstrates the deployment of a full stack web application using React for the frontend, FastAPI for the backend, and PostgreSQL as the database. The application is containerized using Docker and deployed on an AWS EC2 instance.
## Table of Contents
1. [Prerequisites](#prerequisites)
2. [Installation](#installation)
   - [Manual Setup](#manual-setup)
   - [Docker Setup](#docker-setup)
3. [Usage](#usage)
4. [Additional Resources](#additional-resources)
5. [Contributing](#contributing)
6. [License](#license)

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

#### Frontend

1. Navigate to the frontend directory:
    ```sh
    cd ../frontend
    ```

2. Install dependencies:
    ```sh
    npm install
    ```

3. Start the development server:
    ```sh
    npm start
    ```
### Docker Setup

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/repository.git
    cd repository
    ```

2. Build and run the containers:
    ```sh
    docker-compose up -d
    ```

3. Access the frontend application at `http://localhost` and the backend API at `http://localhost/api`.

## Usage

### Access the Application

- Frontend: [http://localhost](http://localhost)
- Backend API: [http://localhost/api](http://localhost/api)
- API Documentation: [http://localhost/docs](http://localhost/docs)
- Adminer: [http://localhost:8080](http://localhost:8080) (use to manage PostgreSQL database)

## Additional Resources

- [React Documentation](https://reactjs.org/docs/getting-started.html)
- [FastAPI Documentation](https://fastapi.tiangolo.com/)
- [Docker Documentation](https://docs.docker.com/)

  ## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.




