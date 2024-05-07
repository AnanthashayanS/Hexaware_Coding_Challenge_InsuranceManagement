# Hexaware Coding Challenge Insurance Management

This project is an Insurance Management System designed to help manage insurance policies and claims efficiently. It provides a command-line interface that interacts with a SQL database to perform various insurance-related operations, following object-oriented principles.

# Project Structure:
## **Entity**
Contains the core model classes representing the entities in the insurance domain: <br>
### User: Represents a user in the system with confidential attributes like user ID, username, and role.<br>
### Client: Stores client details such as name, contact information, and associated policy.<br>
### Claim: Handles claim details like claim number, amount, status, and associated client and policy.<br>
### Policy: Represents an insurance policy with attributes like policy name, type, and associated clients and claims.<br>
## **DAO (Data Access Object)** <br>
Implements the data interaction logic <br>
### Interface (IPolicyService): 
Defines the structure of policy operations such as creation, retrieval, updating, and deletion.<br>
### Implementation (InsuranceServiceImpl): 
Implements the above operations by interacting with the database.<br>
## **Exception**<br>
Defines custom exceptions that are thrown and handled across different parts of the system:<br>
## PolicyNotFoundException: <br>
Raised when a policy is not found during retrieval or update operations.<br>
## **Util (Utility Classes)** <br>
Provides utility methods for database connections:<br>
### DBPropertyUtil:
Reads database connection details from a properties file and returns a formatted connection string.<br>
### DBConnUtil: Uses the connection string to establish a database connection.<br>
## **Main(Main Module)** <br>
Contains the MainModule class which provides a menu-driven command-line interface. Users can create, update, delete, and list insurance policies through this interface.<br>
