# Mental Health Backend API

Backend RESTful API built with **Spring Boot** and **Java**, designed to serve as the core service for a Mental Health application. It manages users and mental health tasks (e.g., wellness goals, therapy exercises).

## Tags
`Java` `Spring Boot` `REST API` `Mental Health` `Backend`

## Features
- **User Management**: Creation and retrieval of users.
- **Task Management**: Assignment and tracking of mental health goals/tasks.
- **Global Error Handling**: Standardized JSON error responses.
- **In-Memory Database**: H2 database for zero-config startup and easy testing.
- **Continuous Integration**: GitHub Actions workflow included for automated testing and building.

## Requirements
- Java 17+
- (Optional) Maven if you don't use the provided Maven Wrapper.

## Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/k4inos1/java-api.git
   cd java-api
   ```

2. **Open as a Maven Project**
   *Important*: Open the `java-api` folder directly in your IDE (VSCode, IntelliJ, or Eclipse) to avoid "non-project file" warnings. The IDE needs to detect the `pom.xml` at the root.

3. **Run the Application**
   Using the included Maven Wrapper:
   ```bash
   # Windows
   .\mvnw.cmd spring-boot:run
   
   # Linux/macOS
   ./mvnw spring-boot:run
   ```
   The application will start on `http://localhost:8080`.

## API Endpoints

### Users
- `GET /api/users`: List all users.
- `POST /api/users`: Create a new user. 
  - Body: `{"name": "John Doe", "email": "john@example.com"}`

### Tasks
- `GET /api/tasks`: List all tasks.
- `GET /api/tasks/user/{userId}`: List tasks for a specific user.
- `POST /api/tasks/user/{userId}`: Create a task for a user.
  - Body: `{"title": "Morning Meditation", "description": "10 minutes of mindfulness"}`
- `PATCH /api/tasks/{id}/status?status=COMPLETED`: Update the status of a task.
- `DELETE /api/tasks/{id}`: Delete a task.
