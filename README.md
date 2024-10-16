# E-commerce Common Service

## Overview

The **E-commerce Common Service** provides shared utilities and common functionalities used across various microservices within the e-commerce application. This service aims to centralize code that can be reused by other services, improving maintainability and reducing duplication.

## Features

- **Shared Models**: Contains common data models used by multiple services.
- **Utility Functions**: Provides reusable functions for operations like validation, formatting, etc.
- **Configuration Management**: Centralizes configuration settings for the microservices that require common configurations.
- **Error Handling**: Implements standard error handling mechanisms for consistent API responses.

## Technologies Used

- **Java**
- **Spring Boot**
- **Maven** (for dependency management)
- **Spring Cloud** (for service discovery and configuration management)

## Prerequisites

Before running this service, ensure you have the following installed:

- **Java JDK 11 or higher**
- **Maven** (for building the project)
- Access to the relevant microservices (See below)

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/juansebstt/ecommerce-common-service.gi
    ```

2. Navigate to the project directory:

    ```bash
    cd ecommerce-common-service
    ```

3. Build the project using Maven:

    ```bash
    mvn clean install
    ```


## Configuration

The common service may require configuration for connecting to other services. Ensure to set the appropriate configuration settings in your application properties.

### Sample Configuration

You may need to configure the following settings in your `application.yml` or `application.properties` file:

```yaml
server:
  port: 8090

spring:
  application:
    name: ecommerce-common-service

```

## Inter-Service Communication

The E-commerce Frontend connects with the following microservices:

- **[E-commerce API Gateway](https://github.com/juansebstt/ecommerce-api-gateway)**:
    - All requests from the frontend are routed through the API Gateway, which forwards them to the appropriate microservices.
- **[E-commerce Auth Service](https://github.com/juansebstt/ecommerce-auth-service)**:
    - Manages user authentication and authorization, providing JWT tokens for secure access.
- **[E-commerce Payment Service](https://github.com/juansebstt/ecommerce-payment-service):**
    - Handles payment processing when users make purchases.
- **[E-commerce Product Service](https://github.com/juansebstt/ecommerce-product-service)**:
    - Retrieves product details and availability for display in the frontend.
- **[E-commerce Cart Service](https://github.com/juansebstt/ecommerce-cart-service)**:
    - Manages users' shopping cart sessions and updates.
- **[E-commerce Order Service](https://github.com/juansebstt/ecommerce-order-service)**:
    - Handles order creation and management after checkout.
- **[E-commerce User Service](https://github.com/juansebstt/ecommerce-user-service)**:
    - Manages user profiles and account information.
- **[E-commerce Notification Service](https://github.com/juansebstt/ecommerce-notification-service)**:
    - Sends notifications and updates to users regarding their orders and account activities.
- **[E-commerce Catalog Service](https://github.com/juansebstt/ecommerce-catalog-service)**:
    - Provides detailed product information and availability.
- **[E-commerce Contact Service](https://github.com/juansebstt/ecommerce-contact-service)**:
    - Manages customer support inquiries and communication.

## Usage

This service runs in the background and is called by other microservices as needed. The shared functionality will enhance the overall efficiency of the e-commerce application.

## Contributing

Feel free to submit pull requests or open issues if you find bugs or want to contribute to the project.