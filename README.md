# Pet Store API Testing Project

## Overview

This project contains automated API tests for the Swagger Pet Store API using Postman.

The collection covers the main API functionalities including:

* Pet endpoints
* Store endpoints
* User endpoints

The goal of this project is to practice API testing concepts and improve automation testing skills using Postman.

---

# Technologies Used

* Postman
* JavaScript
* REST API Testing
* Swagger Pet Store API

---

# Project Structure

```text
Pet_Store/
│
├── Pet_Store_Collection.json
├── Pet_Store_Environment.json
└── README.md
```

---

# Tested Modules

## Pet Module

### Test Cases

* Find pets by status
* Add new pet
* Update pet information
* Delete pet by ID

### Validations

* Status code validation
* Response time validation
* Response body validation
* JSON data type validation

---

## Store Module

### Test Cases

* Find order by ID
* Find pet inventories
* Place an order for a pet
* Delete order by ID

### Validations

* Status code validation
* Response time validation
* Response body validation

---

## User Module

### Test Cases

* Create a new user
* Get user by username
* Login user
* Update user
* Delete user
* Logout user

### Validations

* Status code validation
* Response time validation
* Response body validation

---

# Implemented API Test Types

This project includes different API testing validations such as:

* Functional testing
* Response status validation
* Response time validation
* JSON response validation
* Data type validation
* Response body validation

---

# Example of Automated Tests

```javascript
pm.test("Response time is less than 3000ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(3000);
});

let response = pm.response.json();

pm.test("Pet id is a number", function () {
    pm.expect(response.id).to.be.a("number");
});
```

---

# Environment Variables

The project uses Postman environment variables.

Example:

```text
{{Base_URL}}
```

Environment file included:

```text
Pet_Store_Environment.json
```

---

# How to Run the Project

## 1. Import Files into Postman

Import:

* Collection file
* Environment file

---

## 2. Configure Base URL

Set the value of:

```text
Base_URL
```

Example:

```text
https://petstore.swagger.io/v2
```

---

## 3. Run the Collection

Use:

* Collection Runner in Postman

or

* Newman CLI

Example:

```bash
newman run Pet_Store_Collection.json
```

---

