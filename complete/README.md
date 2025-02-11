TUQuiet Proof of Concept
A simple proof of concept demonstrating Spring Boot with MySQL integration.
Prerequisites

Java JDK 17 or later
MySQL 8.0
Windows 10/11 (for these specific instructions)

Database Setup

Start MySQL Shell

bashCopymysqlsh

Switch to SQL mode and connect:

sqlCopy\sql
\connect root@localhost

Create the test database:

sqlCopyCREATE DATABASE test;
Environment Setup
In PowerShell, set the following environment variables:
powershellCopy# Set Database credentials
$env:DB_USER="root"
$env:DB_PASS="your_password"

# Set Java Home (use your actual Java path)

$env:JAVA_HOME="C:\Program Files\Java\jdk-17"
Running the Application

Navigate to the project's complete directory:

powershellCopycd complete

Run the application using Maven wrapper:

powershellCopy.\mvnw spring-boot:run

Test the application by visiting:

http://localhost:8080
http://localhost:8080/test

Expected Output

At /: "Hello from Spring Boot!"
At /test: "If you see this, both the server and routing are working!"

Troubleshooting

If mvnw isn't found, ensure you're in the complete directory
If database connection fails, verify your MySQL service is running
If JAVA_HOME errors occur, confirm your Java installation path
