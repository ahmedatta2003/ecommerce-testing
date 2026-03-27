E-Commerce Testing Project (Full QA Automation Suite)

Project Overview

This project represents a complete QA process for an E-commerce web application, built by a single QA Engineer simulating a real-world company environment.

It covers all testing levels:

Manual Testing
API Testing
Automation Testing
Performance Testing
CI/CD Integration
Project Objectives
Validate core E-commerce functionalities
Ensure system reliability and performance
Automate regression testing
Integrate testing into CI/CD pipeline
Project Structure

ecommerce-testing/
│
├── manual-testing/
│ ├── test-cases.csv
│ ├── test-scenarios.csv
│ └── bug-reports.csv
│
├── api-testing/
│ ├── postman_collection.json
│ └── README.md
│
├── automation/
│ ├── pom.xml
│ └── src/
│ ├── main/java/pages/
│ └── test/java/tests/
│
├── performance/
│ ├── test.jmx
│ └── README.md
│
├── .github/workflows/
│ └── ci.yml
│
└── README.md

Manual Testing

Test Scenarios:

User Registration
User Login
Product Search
Add to Cart
Checkout Process

Test Cases:

Each test includes steps and expected results

Bug Reports:

Includes bug description, steps, severity
API Testing

Tools Used:

Postman
Newman

Endpoints Tested:

GET /products
POST /login
POST /cart
POST /checkout

Sample Test Script:

pm.test("Status code is 200", function () {
pm.response.to.have.status(200);
});

pm.test("Response time < 2s", function () {
pm.expect(pm.response.responseTime).to.be.below(2000);
});

Run using Newman:

npm install -g newman
newman run postman_collection.json

Automation Testing

Tech Stack:

Java
Selenium WebDriver
JUnit
Maven

Framework:

Page Object Model (POM)

Test Flow:

Login
Search Product
Add to Cart
Checkout
Performance Testing

Tool:

Apache JMeter

Scenario:

50 to 100 users
Ramp-up: 30 seconds
Loop count: 5

Metrics:

Response Time
Throughput
Error Rate
CI/CD

GitHub Actions is used to run tests automatically on each push.

How to Run

Automation:
mvn test

API:
newman run postman_collection.json

Performance:
Open JMeter and run test.jmx

Skills Demonstrated
Manual Testing
API Testing
Automation Testing
Performance Testing
CI/CD
Author

Ahmed Atta
Junior Software Test Engineer

Notes
This project simulates a real company environment
Built by one QA Engineer
Suitable for portfolio and job applications
Future Improvements
Add Allure Reports
Add TestNG
Add Data Driven Testing
Add Docker
Add API Automation using RestAssured
