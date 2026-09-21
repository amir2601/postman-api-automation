# Postman API Automation

API testing and automation practice using Postman based on the **Valentino's Artisan Coffee House API**.

This project was completed as part of a Postman API Automation course. The original collection was forked from the course/API workspace and extended with test scripts and validations as part of my practice.

## 🧪 What I Practiced

* REST API testing
* GET and POST requests
* HTTP status code validation
* Response header validation
* JSON response validation
* JSON Schema validation
* Collection variables
* Environment/variable handling
* Pre-request scripts
* Post-response test scripts
* Dynamic test data generation
* Response data extraction
* API request chaining
* Regular expression validation

## 📂 API Coverage

### Status

* Get API status
* Validate HTTP status code
* Validate response headers

### Products

* Get all products
* Get a single product
* Validate product response structure
* Validate product JSON schema

### Clients

* Register a new client
* Capture API key from the response

### Orders

* Create a new order
* Generate a dynamic customer name
* Capture and store `orderId`
* Validate customer information
* Validate order ID format
* Validate order response schema
* Get all orders
* Get an order by ID

## 🛠️ Tools

* Postman
* JavaScript
* REST API
* JSON Schema

## ▶️ How to Run

1. Import the collection JSON file into Postman.
2. Configure the required `baseUrl`.
3. Provide a valid API key where required.
4. Set the required `productId` if needed.
5. Run the requests individually or use the Postman Collection Runner.
6. Review the test results in the Postman Test Results section.

## 📌 Key Automation Examples

### Status Code Validation

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```

### Response Data Extraction

```javascript
response = pm.response.json();
pm.collectionVariables.set("orderId", response.id);
```

### Dynamic Test Data

```javascript
pm.collectionVariables.set(
    "customerName",
    pm.variables.replaceIn("{{$randomFullName}}")
);
```

### JSON Schema Validation

The collection also uses JSON Schema validation to verify the structure and data types of API responses.

## 📚 Learning Context

This repository represents my hands-on practice in API testing and automation while developing my Software Quality Assurance skills.
