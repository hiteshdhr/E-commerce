# E-Commerce Spring Boot Application

A modern, robust e-commerce backend built with Spring Boot, Spring Data JPA, Spring Security, and MySQL database integration.

## 🚀 Tech Stack
- **Java**: Version 21 (LTS)
- **Framework**: Spring Boot 4.0.3
- **ORM / Database Access**: Hibernate 7.2.4 / Spring Data JPA
- **Database**: MySQL 8.0.x
- **Security**: Spring Security

---

## 🛠️ Local Setup

### 1. Prerequisites
Ensure you have the following installed on your machine:
- OpenJDK 21 or higher
- MySQL Server 8.0.x
- Git

### 2. Database Configuration
The application connects to a MySQL database named `mydatabase`.
1. Open your MySQL client and create the database if it doesn't exist:
   ```sql
   CREATE DATABASE IF NOT EXISTS mydatabase;
   ```
2. The database connection properties are configured in [src/main/resources/application.properties](src/main/resources/application.properties):
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/mydatabase
   spring.datasource.username=root
   spring.datasource.password=Hitesh@718
   ```
   *Note: If your local credentials differ, update the username and password values in the file above.*

---

## 🏃 Running the Application

### Running Tests
To run the Maven test suite and verify database connection and context configurations, execute:
```bash
# Windows
.\mvnw.cmd test

# Unix/macOS
./mvnw test
```

### Running the Server Locally
To start the application server on the default port `8080`, execute:
```bash
# Windows
.\mvnw.cmd spring-boot:run

# Unix/macOS
./mvnw spring-boot:run
```

*Note: On boot, Spring Security will output a temporary generated security password in the console logs for development use.*

---

## 🔒 Security
By default, the application is secured with Spring Security:
- All endpoints require authentication.
- For development testing, use HTTP Basic authentication:
  - **Username**: `user`
  - **Password**: *Check generated console logs on startup*
