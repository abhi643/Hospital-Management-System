### README.md

# Hospital Management System

## Overview
The Hospital Management System (HMS) is a Java-based project designed to manage essential hospital operations such as patient and doctor management. This project demonstrates proficiency in Core Java, advanced JDBC, and MySQL integration.

## Features
- **Core Java**: Utilizes object-oriented programming principles for modular design.
- **JDBC**: Implements advanced features like transaction handling, prepared statements, and batch operations.
- **MySQL Integration**: Fully integrated with a MySQL database for managing hospital data.

## Prerequisites
Before running the project, ensure you have the following set up:
- **Java Development Kit (JDK)**: Ensure you have JDK 8 or above installed.
- **MySQL**: Install MySQL and set up the necessary database.
- **JDBC Connector**: Download the MySQL Connector/J and add it to your project’s reference libraries.

## Setup Instructions

### 1. Download and Configure MySQL Connector/J
1. Download the MySQL Connector/J from the [official MySQL website](https://dev.mysql.com/downloads/connector/j/).
2. Add the `mysql-connector-java-x.x.xx-bin.jar` file to the project:
   - In your IDE (e.g., Eclipse, IntelliJ IDEA), right-click on your project in the Project Explorer.
   - Select **Build Path** > **Add External Archives...**.
   - Browse to the location of the downloaded `jar` file and add it to your project.

### 2. Create Database and Tables
1. Open your MySQL Command Line Interface (CLI) or any MySQL client.
2. Create the necessary database and tables by running the following commands:
   ```sql
   CREATE DATABASE hospital_management;
   USE hospital_management;

   CREATE TABLE doctors (
       id INT PRIMARY KEY AUTO_INCREMENT,
       name VARCHAR(100),
       specialization VARCHAR(100)
   );

   CREATE TABLE patients (
       id INT PRIMARY KEY AUTO_INCREMENT,
       name VARCHAR(100),
       disease VARCHAR(100),
       doctor_id INT,
       FOREIGN KEY (doctor_id) REFERENCES doctors(id)
   );
   ```

### 3. Configure Database Connection
1. Open the `HospitalManagementSystem.java` file in your IDE.
2. Locate the database connection URL, username, and password section.
3. Update the URL, username, and password with your MySQL database credentials:
   ```java
   String url = "jdbc:mysql://localhost:3306/hospital_management";
   String user = "your_username";
   String password = "your_password";
   ```

### 4. Run the Project
After configuring the above steps, you can run the `HospitalManagementSystem.java` file from your IDE to start the application.

## Conclusion
This Hospital Management System project serves as a solid foundation for understanding Java-based application development with JDBC and MySQL integration. By following the setup instructions carefully, you can ensure the code runs efficiently on your system. 
