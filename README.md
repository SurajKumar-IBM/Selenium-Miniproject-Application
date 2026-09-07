# E-Commerce Application | Selenium Mini Project

This repository contains the **E-Commerce Application** used for our Selenium Automated Regression Testing mini project.

## Project Objective

The main objective of this project is to demonstrate how automated regression testing can detect bugs introduced when new features are added to an existing application.

Our workflow follows this process:

```text
Application Change
        ↓
Code Pushed to GitHub
        ↓
Application Updated/Deployed
        ↓
Automated Regression Tests Triggered
        ↓
Selenium Executes Test Cases
        ↓
Test Results (PASS / FAIL)
```

## Application Features

The E-Commerce application includes functionality such as:

* Viewing products
* Viewing product details
* Adding products to the cart
* Managing cart items
* Calculating the total amount
* Checkout functionality

Additional features may be added during the project to demonstrate regression testing scenarios.

## Regression Testing Scenario

One of the main business rules tested in this project is:

> **A user must not be able to complete a checkout when the final order amount is zero or negative.**

For example:

| Product Price | Discount | Final Amount | Expected Result  |
| ------------- | -------: | -----------: | ---------------- |
| ₹100          |      ₹20 |          ₹80 | Checkout Allowed |
| ₹100          |     ₹100 |           ₹0 | Checkout Blocked |
| ₹100          |     ₹150 |         -₹50 | Checkout Blocked |

### Regression Demonstration

The project will introduce a new feature such as a **Discount Card**.

The discount feature may affect the final order amount.

Example:

```text
Product Price: ₹100
Discount: ₹150

Final Amount: -₹50
```

The application must prevent the user from completing the checkout.

If a new feature accidentally allows checkout with a zero or negative final amount, the automated Selenium regression suite should detect the issue and fail.

```text
New Feature Added
        ↓
Existing Business Rule Broken
        ↓
Regression Tests Executed
        ↓
Test Case Failed 
        ↓
Regression Bug Detected
```

## Automation Testing

The Selenium automation tests for this application are maintained in a separate repository.

The automation project is responsible for:

* Selenium test automation
* Regression test execution
* TestNG test cases
* Page Object Model implementation
* Automated test reports
* GitHub Actions integration

## Project Architecture

```text
E-Commerce Application Repository
        │
        │ Application Changes
        ▼
     GitHub
        │
        ▼
Application Deployment
        │
        ▼
Selenium Automation Tests
        │
        ▼
Regression Test Results
```

## Technology Stack

The technologies used in this application depend on the original e-commerce project implementation.

Possible technologies include:

* HTML
* CSS
* JavaScript

## Project Purpose

This repository is part of a mini project focused on demonstrating:

* Selenium Automation Testing
* Automated Regression Testing
* Continuous Integration
* GitHub Actions
* Regression Bug Detection
* Software Testing Collaboration

The goal is to simulate a real-world scenario where application changes are continuously validated using automated regression tests.

## Related Repository

The Selenium automation framework and regression test cases are maintained in a separate repository.

**Automation Repository:**
`<selenium-automation-repository-link>`
