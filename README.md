<div align="center">

# Java Backend API

Robust and scalable backend RESTful API built with Spring Boot and Java, designed to serve as a generic core service.

[![Java](https://img.shields.io/badge/Java-17%2B-ED8B00?style=flat-square&logo=openjdk&logoColor=white)](https://openjdk.java.net)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.1.2-6DB33F?style=flat-square&logo=springboot&logoColor=white)](https://spring.io/projects/spring-boot)
[![REST API](https://img.shields.io/badge/REST%20API-005571?style=flat-square&logo=json&logoColor=white)](https://restfulapi.net/)
[![H2 Database](https://img.shields.io/badge/H2-Database-003545?style=flat-square&logo=h2&logoColor=white)](https://h2database.com)
[![CI — Maven](https://github.com/k4inos1/java-api/actions/workflows/maven.yml/badge.svg?branch=master)](https://github.com/k4inos1/java-api/actions/workflows/maven.yml)
[![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)](LICENSE)

</div>

## Features
- **User Management**: Creation and retrieval of users.
- **Global Error Handling**: Standardized JSON error responses.
- **In-Memory Database**: H2 database for zero-config startup and easy testing.
- **Continuous Integration**: GitHub Actions workflow included for automated testing and building.

## Requirements
- Java 17+
- Maven

## Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/k4inos1/java-api.git
   cd java-api
   ```

2. **Open as a Maven Project**
   *Important*: Open the `java-api` folder directly in your IDE (VSCode, IntelliJ, or Eclipse) to avoid "non-project file" warnings. The IDE needs to detect the `pom.xml` at the root.

3. **Run the Application**
   ```bash
   mvn spring-boot:run
   ```
   The application will start on `http://localhost:8080`.

## API Endpoints

### Users
- `GET /api/users`: List all users.
- `POST /api/users`: Create a new user. 
  - Body: `{"name": "John Doe", "email": "john@example.com"}`
