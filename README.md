# Java Backend API

**Robust and scalable RESTful API built with Spring Boot and Java, designed to serve as a generic core service.**

<br />

[![Java](https://img.shields.io/badge/Java-17%2B-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)](https://openjdk.java.net)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.1.2-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)](https://spring.io/projects/spring-boot)
[![REST API](https://img.shields.io/badge/REST%20API-005571?style=for-the-badge&logo=json&logoColor=white)](https://restfulapi.net/)
[![H2 Database](https://img.shields.io/badge/H2-Database-003545?style=for-the-badge&logo=h2&logoColor=white)](https://h2database.com)
[![CI — Maven](https://img.shields.io/github/actions/workflow/status/k4inos1/java-api/maven.yml?branch=master&label=Maven%20CI&style=for-the-badge&logo=githubactions&logoColor=white)](https://github.com/k4inos1/java-api/actions/workflows/maven.yml)
[![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)](LICENSE)

---

## Features

- **User Management**: Creation and retrieval of users.
- **Task Management**: Assignment and tracking of tasks.
- **Global Error Handling**: Standardized JSON error responses.
- **In-Memory Database**: H2 database for zero-config startup and easy testing.
- **Continuous Integration**: GitHub Actions workflow included for automated testing and building.

<br />

## Requirements

- **Java 17+**
- **Maven**

<br />

## Setup Instructions

**1. Clone the repository**
```bash
git clone https://github.com/k4inos1/java-api.git
cd java-api
```

**2. Open as a Maven Project**  
*Important*: Open the `java-api` folder directly in your IDE (VSCode, IntelliJ, or Eclipse) to avoid "non-project file" warnings. The IDE needs to detect the `pom.xml` at the root.

**3. Run the Application**
```bash
mvn spring-boot:run
```
The application will start on `http://localhost:8080`.

<br />

## API Endpoints

### Users
- `GET /api/users`: List all users.
- `POST /api/users`: Create a new user.
  - *(Body: `{"name": "John Doe", "email": "john@example.com"}`)*

### Tasks
- `GET /api/tasks`: List all tasks.
- `GET /api/tasks/user/{userId}`: List tasks for a specific user.
- `POST /api/tasks/user/{userId}`: Create a task for a user.
  - *(Body: `{"title": "Complete Backend Setup", "description": "Finish configuring the Spring Boot application"}`)*
- `PATCH /api/tasks/{id}/status?status=COMPLETED`: Update the status of a task.
- `DELETE /api/tasks/{id}`: Delete a task.

<br />

---
*Made with ❤️ by [k4inos1](https://github.com/k4inos1)*
