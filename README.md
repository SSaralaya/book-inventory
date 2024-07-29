This project is a Book Inventory Management System built with Spring Boot. It allows users to perform CRUD (Create, Read, Update, Delete) operations on a collection of books, with fields such as title, author, ISBN, price, and available volumes. The project also includes custom error handling to provide a user-friendly experience.

Tech Stack Used
Backend:
        Spring Boot: For creating a robust and scalable REST API.
        Spring Data JPA: For database interactions.
        Thymeleaf: For server-side rendering of HTML pages.
        Database: MySQL
        Maven: For project management and dependency resolution.
Frontend:
        HTML/CSS: For creating the structure and styling of the web pages.
        Bootstrap: For responsive design and prebuilt components.

Database Setup Procedure:
Open the MySQL command-line client or any MySQL GUI tool (like MySQL Workbench) and create a new database
        CREATE DATABASE book_inventory;

Create a new MySQL user and grant privileges to the database:
        CREATE USER 'bookuser'@'localhost' IDENTIFIED BY 'password';
        GRANT ALL PRIVILEGES ON book_inventory.* TO 'bookuser'@'localhost';
        FLUSH PRIVILEGES;

Table Creation:
        CREATE TABLE books (
            id BIGINT AUTO_INCREMENT PRIMARY KEY,
            title VARCHAR(255) NOT NULL,
            author VARCHAR(255) NOT NULL,
            isbn VARCHAR(20) UNIQUE NOT NULL,
            price DECIMAL(10, 2) NOT NULL,
            available_volumes INT NOT NULL
      );


