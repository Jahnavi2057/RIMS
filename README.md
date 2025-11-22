# RIMS

RIMS (Residential Inventory Management System) is a Java-based console application designed to manage and automate residential property operations such as listing, booking, payments, and resident tracking. The system supports three user roles: Owner, Registered User, and Looker. Each role provides different access privileges suited for property administration or tenant interaction.

**Features**

**Owner:**
Add new properties
View all properties
Change property availability
Delete properties
View and update booking statuses

**Registered User:**
View available properties
Book properties with date validation
Make payments using multiple methods
Cancel bookings with transaction safety
View previous bookings including cancelled and completed ones

**Looker:**
View available properties in read-only mode

Technical Stack
Java
Core OOP concepts
JDBC
MySQL database
Console-based user interface

**Object-Oriented Concepts Implemented**

Classes and Objects: The system is structured around classes such as Admin, RegisteredUser, Sightseer, OperationResult, and Main. Instances of these classes represent different user roles and system actions.

Constructors: Constructors are used to initialize objects, such as passing the logged-in user ID into the RegisteredUser class.

Inheritance: RegisteredUser and Sightseer both extend the Admin class. This reuses common functionality and customizes behavior where needed.

Polymorphism: All user roles implement the UserRole interface. The application stores and invokes user actions through a UserRole reference, allowing different menu behaviors based on the actual object type.

Encapsulation: Key fields such as database credentials, user IDs, and operation results are encapsulated within their respective classes.

Generic Classes: The OperationResult<T> class demonstrates the use of Java generics by returning typed results along with success status and messages.

Exception Handling: The system manages invalid input, database issues, constraint violations, and transaction failures through structured exception handling.

JDBC Integration

**The application uses JDBC for:**

Establishing MySQL connections
Executing queries through PreparedStatement
Reading data using ResultSet
Handling transactions with commit and rollback
Managing inserts, updates, and deletes

**Database Structure**

The MySQL database contains the following tables:
admin
user
property
booking
payment
resident
feedback

Foreign keys ensure referential integrity, and several operations run within transactions to maintain consistency.

**Setup Procedure**

Install Java and MySQL.
Import the provided SQL schema into MySQL to create the required tables and sample data.
Update the database credentials in the source file if necessary.
Compile and run the Java program from the terminal.

**System Workflow Overview**

Owner Workflow: Login, manage properties, and oversee bookings.

Registered User Workflow: Register or login, browse available properties, make bookings, process payments, cancel bookings if needed, and view booking history.

Looker Workflow: Browse available properties in a non-interactive mode.

Future Enhancements: Implementation of a graphical user interface

Password hashing for security: Email notifications for bookings and cancellations

Feedback analytics and property ratings: Admin dashboard for reporting and insights

**Purpose**

This project is intended for academic demonstration and provides a structured example of integrating Java, JDBC, MySQL, and object-oriented design principles into a functional application.
