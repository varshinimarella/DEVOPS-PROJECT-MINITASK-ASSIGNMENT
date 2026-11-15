# DEVOPS-PROJECT-MINITASK-ASSIGNMENT
# MiniTask – FastAPI DevOps Project
A Python-based FastAPI application developed as a DevOps mini project, featuring RESTful API development, Docker containerization, Docker Compose orchestration, automated testing with Pytest, and Continuous Integration (CI) using GitHub Actions.
# MiniTask – FastAPI DevOps Project

A Python-based REST API application built using **FastAPI**, containerized with **Docker**, and integrated with **GitHub Actions CI** for automated testing and Docker image builds.

## Project Overview

MiniTask is a simple task management API that allows users to check application health, retrieve tasks, and create new tasks. The project demonstrates essential DevOps practices, including containerization, automated testing, and Continuous Integration.

## Technologies Used

- **Programming Language:** Python 3.12
- **Framework:** FastAPI
- **Testing:** Pytest
- **Containerization:** Docker
- **Container Orchestration:** Docker Compose
- **CI/CD:** GitHub Actions
- **Version Control:** Git and GitHub

## Project Structure

```text
MiniTask_Student_Starter/
│
├── app/
│   ├── __init__.py
│   └── main.py
│
├── tests/
│   └── test_api.py
│
├── .github/
│   └── workflows/
│       └── ci.yml
│
├── .dockerignore
├── .gitignore
├── Dockerfile
├── compose.yaml
├── requirements.txt
├── requirements-dev.txt
├── README.md
└── LICENSE
```

## Features

- REST API development using FastAPI
- Health-check endpoint
- Task creation and retrieval
- API validation using Pydantic
- Automated testing using Pytest
- Docker image creation
- Docker Compose configuration
- Automated CI workflow using GitHub Actions

## Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/varshinimarella/DEVOPS-PROJECT-MINITASK-ASSIGNMENT.git
cd DEVOPS-PROJECT-MINITASK-ASSIGNMENT
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

### 3. Activate the environment

Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

### 4. Install dependencies

```bash
pip install -r requirements-dev.txt
```

## Run the Application

Start the FastAPI application:

```bash
uvicorn app.main:app --reload
```

Open the API documentation:

http://127.0.0.1:8000/docs

## API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/` | Application welcome message |
| GET | `/health` | Health check |
| GET | `/tasks` | Retrieve all tasks |
| POST | `/tasks` | Create a new task |

## Docker Setup

Build the Docker image:

```bash
docker compose build
```

Start the application:

```bash
docker compose up -d
```

Check running containers:

```bash
docker compose ps
```

Stop the application:

```bash
docker compose down
```

## Run Tests

Execute the test suite:

```bash
python -m pytest
```

## GitHub Actions – Continuous Integration

The project uses GitHub Actions to automate the following workflow whenever code is pushed to the `main` branch or a pull request is created:

1. Checkout the repository.
2. Set up Python 3.12.
3. Install development dependencies.
4. Execute automated tests using Pytest.
5. Build the Docker image.

The workflow helps verify application functionality and Docker build compatibility automatically.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---
## Project Overview

MiniTask is a Python-based REST API application developed using FastAPI as part of a DevOps mini project. It provides basic task management functionality, including creating and retrieving tasks, along with a health-check endpoint to monitor application availability. The project demonstrates essential DevOps practices such as application development, containerization, automated testing, and Continuous Integration using GitHub Actions.

## Technologies Used

This project uses Python 3.12 as the primary programming language and FastAPI for developing RESTful APIs. Pytest is used for automated testing to verify application functionality. Docker is used to containerize the application, while Docker Compose simplifies building and running the container. Git and GitHub are used for version control and source code management, and GitHub Actions automates the testing and Docker image build process.

## Project Structure

The project follows a structured directory organization to maintain clean and manageable code. The `app/` directory contains the FastAPI application source code, while the `tests/` directory contains automated test cases. The `.github/workflows/` directory stores the GitHub Actions CI configuration. The `Dockerfile` defines the application image, and `compose.yaml` manages the application container. The `requirements.txt` and `requirements-dev.txt` files specify application and development dependencies. The `.gitignore` and `.dockerignore` files exclude unnecessary files from version control and Docker build contexts.

## Features

The application provides REST API endpoints for checking application health, retrieving existing tasks, and creating new tasks. It uses Pydantic validation to ensure that task input meets the defined requirements. The project also supports Docker-based deployment, automated API testing with Pytest, and continuous integration through GitHub Actions. These features help demonstrate a basic development-to-deployment workflow.

## Installation and Setup

To set up the project locally, first clone the GitHub repository and navigate to the project directory. Create and activate a Python virtual environment to isolate project dependencies. Install the required packages using the provided `requirements-dev.txt` file. Once the dependencies are installed, the application is ready to run and test in your local development environment.

## Run the Application

The FastAPI application can be started locally using the Uvicorn ASGI server. After starting the server, the application becomes accessible through a local browser. FastAPI also provides an interactive Swagger UI documentation page, which allows users to explore available API endpoints, submit requests, and view responses without requiring a separate API testing tool.

## API Endpoints

The application exposes four REST API endpoints. The root endpoint (`GET /`) displays a welcome message confirming that the application is running. The health-check endpoint (`GET /health`) returns the application's operational status. The task retrieval endpoint (`GET /tasks`) returns the available tasks, while the task creation endpoint (`POST /tasks`) accepts task details and creates a new task. These endpoints demonstrate basic REST API operations using HTTP methods and JSON responses.

## Docker Setup

Docker is used to package the FastAPI application and its dependencies into a portable container image. The `Dockerfile` contains the instructions required to build the image, including selecting the Python base image, installing dependencies, copying application files, and starting the server. Docker Compose simplifies the process of building, starting, and stopping the application container through the `compose.yaml` configuration. This approach helps maintain a consistent application environment.

## Run Tests

The project uses Pytest to execute automated tests and verify the functionality of the FastAPI application. The test suite checks important API operations, including health checks, task retrieval, and task creation. Running the test suite helps identify issues early and ensures that the application behaves as expected before building and deploying the Docker image.

## GitHub Actions – Continuous Integration

GitHub Actions is configured to automate the Continuous Integration process whenever changes are pushed to the `main` branch or a pull request is created. The workflow checks out the repository, sets up Python 3.12, installs the required development dependencies, executes the automated test suite, and builds the Docker image. This

**Developed as a DevOps Mini Project using Python, FastAPI, Docker, and GitHub Actions.**
