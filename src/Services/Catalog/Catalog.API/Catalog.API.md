# Catalog.API Documentation

## Overview
The **Catalog.API** microservice is responsible for managing the product catalog, including:
- Adding, updating, and deleting products.
- Categorizing products for easier navigation.

---

## Endpoints

| HTTP Method | Endpoint                | Description                 |
|-------------|-------------------------|-----------------------------|
| GET         | `/products`             | Retrieve all products       |
| GET         | `/products/{id}`        | Retrieve product by ID      |
| GET         | `/products/category`    | Retrieve products by category |
| POST        | `/products`             | Add a new product           |
| PUT         | `/products/{id}`        | Update a product by ID      |
| DELETE      | `/products/{id}`        | Delete a product by ID      |

---

## Notes
- **Database**: PostgreSQL with [Marten](https://martendb.io/) as the data access library.
- **Authentication**: Token-based authentication is required for admin-level operations.
- **Future Enhancements**:
  - Implement caching for frequently accessed data.
  - Add support for searching and filtering products.
  - Maybe implement Swagger, but not the focus here (just a nice-to-have).

---

## Technology Highlights
- **Marten**: Leveraging Marten for PostgreSQL to simplify data access and enable event sourcing, document storage, and efficient querying.

## Pattern & Principles

- Vertical Slice Architecture
- CQRS Pattern
- Mediator Pattern
- DI
- Minimal API
- ORM Pattern

# Libraries
- MediatR for CQRS
- Carter for API Endpoints
- Marten for PostgreSQL Interaction
- Mapster for Object Mapping
- FluentValidation for Input Validation