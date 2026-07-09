# Swagger Petstore API Testing - QA

Welcome to my API Testing repository!

This project is a comprehensive API (Application Programming Interface) testing documentation using **Swagger Petstore** as a **dummy** system. 

The primary goal of this project is to demonstrate my understanding of the end-to-end Quality Assurance (QA) workflow from reading the API Contract and designing Test Case scenarios, to executing tests via Postman and compiling professional Bug Reports.


## Tools & Technologies

* **API Testing:** Postman
* **API Documentation:** Swagger / OpenAPI
* **Test Management & Reporting:** Microsoft Excel
* **Testing Methodology:** Black-box Testing, Positive & Negative Testing, Security Edge-cases (XSS Injection test).

---

## 📁 Project Structure
This repository is structured to be easily readable and understandable:

```text
├── 📁 Contract/
│   └── api contract petstore.json                 # Original/blueprint API Contract as a testing reference.
├── 📁 Postman-Files/
│   ├── Swagger Petstore.postman_collection.json   # Collection file of requests & automation tests.
│   └── pet store swagger.postman_environment.json # Environment variables file (Base URL, etc.).
└── 📁 Reports/
   ├── Swagger_Petstore_Complete_TestCases_Final.xlsx  # Document containing hundreds of test case scenarios.
   └── QA_Bug_Report_Petstore.xlsx                     # System vulnerability/bug report (High, Medium, Low severity).
```

---

## Testing Scope & Key Findings

The testing is focused on data structure validation, input security, and business logic responses on the main endpoints (Pet, User, and Store).

Bug Report Highlights:
A good system shouldn't just be tested for its normal functions (Positive testing), but must also be resilient against errors (Negative testing). Here are some interesting bugs I found and reported:

🔴 [High Severity]: Fatal error (500 Internal Server Error) when attempting to create a user with manipulated array/list inputs, which could potentially crash the service.

🟠 [Medium Severity]: Weak validation on form-data endpoints. The system returns a 200 OK status and saves empty data even when mandatory fields (like pet name) are left blank.

🟡 [Low Severity]: RESTful standard non-compliant response codes, such as the system returning a 404 Not Found instead of a 400 Bad Request when attacked with the wrong ID data type format.


## How to Run the Tests (Postman)

Want to try running this test script yourself? It's super easy:

Clone or download this repository.

Open the Postman application.

Click the Import button, then select the collection file (.postman_collection.json) and the environment file (.postman_environment.json) from the Postman-Files folder.

Don't forget to activate the pet store swagger environment in the top right corner of Postman.

Run it via the Collection Runner to see the test case execution results in real-time!

