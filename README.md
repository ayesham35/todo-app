# Todo App

A full-stack Todo application built with Spring Boot and Thymeleaf.

## Tech Stack
- Java 26
- Spring Boot 3.5
- Spring MVC + Thymeleaf
- Spring Data JPA + Hibernate
- H2 In-Memory Database (development)
- MySQL (production)
- Bean Validation
- Lombok
- CSS

## Features
- Create, edit, and delete todos
- Toggle completion status
- Filter by All / Active / Completed
- Form validation
- Responsive UI

## How to Run (H2 - Development)
1. Clone the repository
2. Open in IntelliJ IDEA
3. Run `TodoAppApplication.java`
4. Visit `http://localhost:8080`

## H2 Database Console
Visit `http://localhost:8080/h2-console`  
JDBC URL: `jdbc:h2:mem:tododb`  
Username: `sa` | Password: *(leave blank)*

## How to Run (MySQL - Production)
1. Open MySQL Workbench and run the following SQL:

```sql
CREATE DATABASE tododb;
CREATE USER 'todouser'@'localhost' IDENTIFIED BY 'your_password';
GRANT ALL PRIVILEGES ON tododb.* TO 'todouser'@'localhost';
FLUSH PRIVILEGES;
```

2. Copy `application.properties.example` to `application.properties`
3. Fill in your MySQL username and password
4. Open in IntelliJ IDEA
5. Run `TodoAppApplication.java`
6. Visit `http://localhost:8080`
