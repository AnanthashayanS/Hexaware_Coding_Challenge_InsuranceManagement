# Hexaware Coding Challenge Insurance Management

This project is an Insurance Management System designed to help manage insurance policies and claims efficiently. It provides a command-line interface that interacts with a SQL database to perform various insurance-related operations, following object-oriented principles.

# Project Structure:
Entity
Contains the core model classes representing the entities in the insurance domain:
User: Represents a user in the system with confidential attributes like user ID, username, and role.
Client: Stores client details such as name, contact information, and associated policy.
Claim: Handles claim details like claim number, amount, status, and associated client and policy.
Policy: Represents an insurance policy with attributes like policy name, type, and associated clients and claims.
DAO (Data Access Object)
Implements the data interaction logic:
Interface (IPolicyService): Defines the structure of policy operations such as creation, retrieval, updating, and deletion.
Implementation (InsuranceServiceImpl): Implements the above operations by interacting with the database.
Exception
Defines custom exceptions that are thrown and handled across different parts of the system:
PolicyNotFoundException: Raised when a policy is not found during retrieval or update operations.
Util (Utility Classes)
Provides utility methods for database connections:
DBPropertyUtil: Reads database connection details from a properties file and returns a formatted connection string.
DBConnUtil: Uses the connection string to establish a database connection.
Main (Main Module)
Contains the MainModule class which provides a menu-driven command-line interface. Users can create, update, delete, and list insurance policies through this interface.
