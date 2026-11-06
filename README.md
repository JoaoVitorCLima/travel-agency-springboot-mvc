# Travel Agency — Spring Boot MVC & MySQL

Java web application demonstrating server-rendered CRUD, relational persistence and an MVC architecture for managing client records.

## Stack
Java 17 · Spring Boot 3.2 · Spring MVC · Spring Data JPA · Thymeleaf · MySQL · Maven

## Architecture
`Thymeleaf views → ClienteController → ClienteRepository → MySQL`

## Features
- Create, list, view, update and remove client records
- Client image upload and display
- Spring Data JPA persistence
- Thymeleaf server-side templates
- Travel destination and promotion pages

## Run locally
1. Install JDK 17, Maven and MySQL. Create database `clientes` and a dedicated local database account.
2. Supply environment variables: `DB_URL=jdbc:mysql://localhost:3306/clientes`, `DB_USER=travel_app`, `DB_PASSWORD=YOUR_LOCAL_PASSWORD`. See `.env.example`; Spring does not automatically load this file.
3. In this directory, run `./mvnw spring-boot:run` (Linux/macOS) or `mvnw.cmd spring-boot:run` (Windows). An installed Maven is also supported: `mvn spring-boot:run`.
4. Visit `http://localhost:8080/cliente/`.

## Changes made during portfolio preparation
- Removed hardcoded DB credentials.
- Replaced state-changing GET delete with POST and a confirmation form.
- Preserved existing images when editing client details without uploading a replacement.
- Added file upload size limits and repository documentation.

## Limitations and validation
- **Source review completed; Maven build and MySQL workflow were not executed in the packaging environment.**
- Spring Boot 3.2 is an older baseline; refresh and test dependencies before deploying.
- This application lacks user authentication/authorization; do not deploy publicly without security improvements.
- A POST endpoint by itself does not guarantee CSRF protection. Verify the security configuration and CSRF controls before deployment.

## Source ownership
Credit other original contributors as appropriate. No license is implied; distribute only materials you have permission to publish.
