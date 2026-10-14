# FitTrack Lite — Backend

## 1. Project Overview

FitTrack Lite is a full-stack fitness and workout progress tracking platform. This repository contains the backend application responsible for business logic, authentication, API endpoints, and database integration.

The backend is developed using Java, Spring Boot, Spring Security, Spring Data JPA, and MySQL.

## 2. Technologies Used

| Technology | Purpose |
|---|---|
| Java 21+ | Backend programming |
| Spring Boot | Application framework |
| Spring Security | Authentication and security |
| Spring Data JPA | Database access |
| Maven | Dependency management and build |
| MySQL 8.x | Relational database |
| Docker | Containerized deployment |
| Render | Backend hosting |

## 3. Features

- User registration and authentication
- Secure password handling
- REST API endpoints
- Workout plan and history management
- Fitness progress and measurement tracking
- Personal records management
- MySQL database integration

## 4. Prerequisites

| Tool | Version |
|---|---|
| JDK | 21 or newer |
| Maven | 3.9+ |
| MySQL Server | 8.x |

Verify the installations:

```bash
java -version
mvn -v
```

## 5. Run Locally in VS Code

### Step 1: Clone the repository

```bash
git clone https://github.com/mihirm262-hue/FitTrack-Lite-Backend.git
cd FitTrack-Lite-Backend
```

### Step 2: Configure MySQL

Create or configure the `fittrack_lite` database as required by the application.

Set your database credentials using environment variables. For Windows PowerShell:

```powershell
$env:DB_USERNAME="root"
$env:DB_PASSWORD="your_mysql_password"
```

For macOS, Linux, or Git Bash:

```bash
export DB_USERNAME="root"
export DB_PASSWORD="your_mysql_password"
```

Use the database credentials appropriate for your own MySQL installation.

### Step 3: Start the backend

Run:

```bash
mvn spring-boot:run
```

The application is expected to start on port `8080`, provided the application configuration and database connection are correct.

## 6. API Endpoints

The following endpoints are documented for the FitTrack Lite application.

| Method | Endpoint |
|---|---|
| POST | `/api/auth/register` |
| POST | `/api/auth/login` |
| POST | `/api/auth/logout` |
| GET | `/api/auth/me` |
| GET | `/api/dashboard` |
| GET | `/api/workouts/plans` |
| GET | `/api/workouts/history` |
| POST | `/api/workouts` |
| GET | `/api/progress` |
| POST | `/api/progress/measurements` |
| GET | `/api/records` |
| POST | `/api/records` |

Actual endpoint availability depends on the implementation in the source code.

## 7. Environment Variables

Configure the following values in the deployment environment.

| Variable | Purpose |
|---|---|
| `DB_URL` | JDBC connection URL for MySQL |
| `DB_USERNAME` | Database username |
| `DB_PASSWORD` | Database password |
| `FRONTEND_URL` | Allowed frontend origin for CORS, if configured |

Example JDBC URL:

```text
jdbc:mysql://HOST:PORT/DBNAME?sslMode=REQUIRED
```

Replace the example values with your actual database connection details. Never commit real credentials to GitHub.

## 8. Deployment Using Render

1. Sign in to Render.
2. Create a new Web Service and connect the `FitTrack-Lite-Backend` repository.
3. Select Docker as the runtime if using the provided `Dockerfile`.
4. Configure the database environment variables.
5. Configure the frontend origin if required by the application's CORS and security settings.
6. Deploy the service.
7. Check the deployment logs and test the API.

Because this is a separate backend repository, use the repository root as the service's root directory unless you have configured a different layout.

## 9. Related Repository

**Frontend:** https://github.com/mihirm262-hue/FitTrack-Lite-Frontend

## 10. Author

Mihir  
Department: Electronics and Communication Engineering (ECE)
