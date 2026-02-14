# CTSE Lab 3 - Spring Boot Microservice with H2 & Swagger

**Module:** Current Trends in Software Engineering (SE4010)  
**Semester:** 1, 2025  
**Institution:** SLIIT | Department of Computer Science & Software Engineering | Faculty of Computing  
**Lab:** DevOps Lab 3  

## Overview
This project implements a simple Spring Boot microservice with CRUD REST APIs, an in-memory H2 database, and Swagger (OpenAPI) documentation.

## Lab Tasks Completed
**Part 1 - Creating a Spring Boot Microservice**
1. Generated project using Spring Initializr (Maven, Java, Jar).
2. Added dependencies: Spring Web, Spring Data JPA, H2 Database, Springdoc OpenAPI UI.
3. Opened and configured the project in the IDE.

**Part 2 - Implementing REST APIs**
1. Created `Product` entity with `id`, `name`, and `price`.
2. Created `ProductRepository` extending `JpaRepository`.
3. Created `ProductController`.
4. Implemented `POST`, `GET`, `GET by ID`, and `DELETE` endpoints.

**Part 3 - Using an In-Memory Database (H2)**
1. Configured H2 properties in `application.properties`.
2. Enabled H2 console.
3. Ran the application and accessed `http://localhost:8080/h2-console`.
4. Verified table creation.

**Part 4 - Enabling Swagger (OpenAPI)**
1. Added `springdoc-openapi` dependency.
2. Started the application.
3. Accessed Swagger UI at `http://localhost:8080/swagger-ui.html` and tested APIs.

## Dependency Issue Encountered (Swagger "No operations defined in spec")
**Problem:** Swagger UI showed **"No operations defined in spec"** at `/v3/api-docs`.  
**Cause:** Incompatible versions between Spring Boot and `springdoc-openapi` (e.g., Spring Boot 4.x with springdoc 2.5.0) and/or missing web starter alignment.  
**Fix Applied:** Aligned Spring Boot and springdoc versions and ensured the standard web starter is used. After updating the dependency versions in `pom.xml`, Swagger correctly lists all REST endpoints.

## Expected Outcome
Build a Spring Boot microservice with REST APIs, use an in-memory database, and document APIs using Swagger.
