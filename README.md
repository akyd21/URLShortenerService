# URL Shortener

A simple URL shortener built with Spring Boot, Thymeleaf, Spring Data JPA, and MySQL.

![Application Screenshot](file:///C:/Desktop/Screenshots/Screenshot%202026-09-14%20235914.png)

![Additional Screenshot](file:///C:/Desktop/Screenshots/Screenshot%202026-09-15%20000258.png)

## Resume Highlights

- Developed a Spring Boot-based URL shortener application that converts long URLs into concise, shareable links with a user-friendly web interface.
- Implemented backend logic for URL validation, storage, and redirection, enabling efficient link management and seamless user navigation.
- Designed a unique short-code generation mechanism to create reliable short URLs while minimizing duplication and maintaining application consistency.
- Built the full application using Java, Spring MVC, Thymeleaf, Maven, and MySQL, demonstrating practical end-to-end web development skills.
- Applied core software engineering practices such as modular design, repository-based data access, and configuration management to create a scalable and maintainable project.

## Requirements

- Java 21 or later
- MySQL 8 or later
- Maven Wrapper (included in this project)

## Database Setup

Create the application database in MySQL:

```sql
CREATE DATABASE IF NOT EXISTS urlshortener;
```

The default database settings are in `src/main/resources/application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/urlshortener
spring.datasource.username=root
spring.datasource.password=
```

Update the username and password if your local MySQL installation uses different credentials.

## Run the Application

From the project directory, run:

Windows PowerShell:

```powershell
.\mvnw.cmd spring-boot:run
```

macOS/Linux:

```bash
./mvnw spring-boot:run
```

The application starts on:

```text
http://localhost:8081
```

## Usage

1. Open `http://localhost:8081` in a browser.
2. Enter a valid URL.
3. Submit the form to generate a shortened URL.
4. Open the generated short URL to redirect to the original URL.

## Endpoints

| Method | Path | Description |
| --- | --- | --- |
| `GET` | `/` | Displays the URL shortening form. |
| `POST` | `/shorten` | Creates a short URL from a valid URL. |
| `GET` | `/{shortCode}` | Redirects to the original URL. |

## Configuration

The application uses the following settings:

- Server port: `8081`
- Database: `urlshortener`
- JPA schema management: `update`
- SQL logging: enabled

Hibernate creates or updates the required table automatically when the application starts.

## Build and Test

Run the tests:

```powershell
.\mvnw.cmd test
```

Build the application:

```powershell
.\mvnw.cmd clean package
```
#
