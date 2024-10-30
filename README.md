# Microservice Template

## Overview

The **Microservice Template** project is a ready-to-use setup for developing Spring Boot microservices in Java. This template integrates best practices and essential components for building and deploying robust microservices. It includes configurations for CI/CD, containerization, logging, error handling, and more, making it easy to start new microservices with minimal setup.

## Features

- **Spring Boot**: A production-ready, opinionated framework for developing Java-based applications.
- **Java 21**: Uses the latest stable version of Java for improved performance and long-term support.
- **RESTful API**: Provides a starting REST API structure.
- **CI/CD Pipeline**: Pre-configured GitHub Actions for continuous integration and deployment.
- **Containerization**: Docker support for easy containerization and deployment.
- **Logging**: Centralized logging with support for structured logs.
- **Error Handling**: Global error handler for standardizing API responses on errors.
- **Swagger Integration**: API documentation with Swagger UI.

## Getting Started

### Prerequisites

- **Java 21** or later
- **Maven 3** or later
- **Docker** (for containerization)
- **GitHub Account** (for CI/CD)

### Project Structure

```
.
├── src/                        # Source files
│   ├── main/
│   │   ├── java/               # Java source files
│   │   ├── resources/          # Resource files (application.yml, log config, etc.)
│   └── test/                   # Test files
├── .github/                    # GitHub Actions workflows for CI/CD
├── Dockerfile                  # Docker configuration
├── README.md                   # Project documentation
└── pom.xml                     # Maven dependencies and build configuration
```

## Setup and Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/Samira1462/microservice-template.git
   cd microservice-template
   ```

2. **Build the Project**
   ```bash
   ./mvnw clean install
   ```

3. **Run Locally**
    - Start the application:
      ```bash
      ./mvnw spring-boot:run
      ```
    - Access the API documentation at `http://localhost:8080/swagger-ui/`

4. **Run Tests**
   ```bash
   ./mvnw test
   ```

## Deployment

### Docker

1. **Build the Docker Image**
   ```bash
   docker build -t microservice-template .
   ```

2. **Run the Docker Container**
   ```bash
   docker run -p 8080:8080 microservice-template
   ```

### CI/CD with GitHub Actions

The GitHub Actions workflow is set up to run tests and build the Docker image on every push to the main branch. You can also add deployment steps to your chosen platform (e.g., AWS, GCP, or Azure) in the `.github/workflows/ci-cd.yml` file.

## Configuration

The configuration is managed through the `application.yml` file located in the `src/main/resources` directory. Update the values as needed, including database configurations, external service URLs, and API keys.

## API Documentation

The API endpoints are documented using Swagger, accessible at `http://localhost:8080/swagger-ui/` when the application is running.

## Contributing

We welcome contributions to enhance the functionality of this microservice template! Please submit pull requests with detailed descriptions of the changes.

