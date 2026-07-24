# JackFood React

JackFood is a food-delivery application with a React frontend and a Spring Boot backend. This repository keeps both parts together so they can be developed, tested, and released as one application.

## Repository layout

| Directory | Stack | Purpose |
| --- | --- | --- |
| `frontend/` | React 18 | Customer and administration web application |
| `backend/` | Spring Boot 3 / Maven | REST API, authentication, payments, and persistence |

## Prerequisites

- Node.js and npm
- Java 17 or later
- MySQL

## Run locally

1. Configure the database and service credentials in `backend/src/main/resources/application.properties`, preferably through environment variables such as `DB_USERNAME` and `DB_PASSWORD`.
2. Start the API:

   ```bash
   cd backend
   ./mvnw spring-boot:run
   ```

   On Windows, use `mvnw.cmd spring-boot:run`.

3. In another terminal, start the web application:

   ```bash
   cd frontend
   npm install
   npm start
   ```

The frontend uses `http://localhost:5454` as the API URL, which matches the backend's default port.

## Useful commands

```bash
# Frontend production build
cd frontend && npm run build

# Backend tests
cd backend && ./mvnw test
```

## Origin

This monorepo consolidates the former `JackFood-React-Frontend` and `JackFood-React-Backend` repositories.
