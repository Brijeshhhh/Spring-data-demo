# Spring Data Demo

This is a simple Spring Boot application that demonstrates the use of Spring Data JPA for accessing data with MYSQL. The project allows adding users to a database and retrieving all users via RESTful endpoints.

## What You Will Build
You will create a MySQL database, build a Spring application, and connect it to the newly created database in a cloud platform

## Prerequisites

To run this project, ensure you have the following installed:

- **Java**: JDK 19 or higher
- **Spring Boot**: Version 3.2.9
- **MySQL**: Aiven MySQL database is used in this project, but you can use any MySQL database.
- **Maven**: Ensure Apache Maven is installed to build the project (`mvn -v` to verify).
- **IDE**: Any Java IDE (IntelliJ IDEA, Eclipse, etc.) with Spring Boot plugin.

## Tools and Technologies Used

- **Spring Boot**: Spring Boot framework for building Java applications.
- **Spring Data JPA**: For ORM (Object-Relational Mapping) with MySQL.
- **JDBC**: Java Database Connectivity for interacting with the MySQL database.
- **Aiven**: Aiven MySQL cloud database for managing user data.
- **JPA (Java Persistence API)**: For handling database operations.
- **MySQL**: As the database system.
- **Maven**: For project dependency management and building.

## How to Implement

1. **Clone the repository**:

   ```bash
   git clone https://github.com/your-username/spring-data-demo.git
   cd spring-data-demo
   ```

2. **Configure the Database**:

   Open `application.properties` and update the MySQL connection settings:

   ```properties
   spring.datasource.url=jdbc:mysql://<your-aiven-url>/<database-name>?useSSL=true
   spring.datasource.username=<your-username>
   spring.datasource.password=<your-password>
   ```

3. **Build the project**:

   Use Maven to build the project:

   ```bash
   mvn clean install
   ```

4. **Run the project**:

   You can start the Spring Boot application using the following command:

   ```bash
   mvn spring-boot:run
   ```

   The application will start on [http://localhost:8080](http://localhost:8080).

5. **Test the Endpoints**:

   Use Postman or cURL to test the following endpoints:

   - **Add User**: Adds a new user to the database.

     ```http
     POST /demo/add?name={name}&email={email}
     ```

     Example cURL request:

     ```bash
     curl -X POST "http://localhost:8080/demo/add?name=John&email=john@example.com"
     ```

   - **Get All Users**: Fetches all users from the database.

     ```http
     GET /demo/all
     ```

     Example cURL request:

     ```bash
     curl -X GET "http://localhost:8080/demo/all"
     ```

## Learning Resources

This project was implemented by following the official [Spring documentation](https://spring.io/guides) and other resources for learning Spring Boot, JPA, and database integration.
