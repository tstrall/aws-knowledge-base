# REST (Representational State Transfer)

**What it is:**
- An architectural style for designing networked APIs
- Based on HTTP verbs, stateless interactions, and resource-based URIs

---

## Core Principles

| Principle          | Description |
|--------------------|-------------|
| **Stateless**      | Each request contains all necessary information |
| **Client-server**  | Separation of concerns between frontend/backend |
| **Cacheable**      | Responses can be cached to improve performance |
| **Uniform interface** | Standard methods and URI structures |
| **Layered system** | APIs can be composed through proxies, gateways, etc. |

---

## Common HTTP Verbs

| Verb     | Action       |
|----------|--------------|
| `GET`    | Retrieve a resource |
| `POST`   | Create a new resource |
| `PUT`    | Replace an existing resource |
| `PATCH`  | Partially update a resource |
| `DELETE` | Remove a resource |

---

## URI Design
```http
GET    /users            # List users
GET    /users/123        # Get user 123
POST   /users            # Create new user
PUT    /users/123        # Replace user 123
DELETE /users/123        # Delete user 123
```

---

## Status Codes

| Code | Meaning |
|------|---------|
| 200  | OK |
| 201  | Created |
| 204  | No Content |
| 400  | Bad Request |
| 401  | Unauthorized |
| 403  | Forbidden |
| 404  | Not Found |
| 409  | Conflict |
| 500  | Internal Server Error |

---

## JSON Format Example
```json
{
  "id": 123,
  "name": "Alice",
  "email": "alice@example.com"
}
```

---

## Tools & Libraries
- **Postman**: Manual testing
- **curl**: CLI-based requests
- **Swagger/OpenAPI**: API documentation
- **FastAPI / Flask / Express / Spring Boot**: REST API frameworks

---

## REST vs. Alternatives
- **GraphQL**: Client controls data shape; single endpoint
- **gRPC**: Binary, contract-based, faster for internal systems

---

## Interview Tips
- Know HTTP methods and response codes
- Be able to describe a RESTful URL scheme
- Understand idempotency (GET/PUT/DELETE = idempotent; POST = not)
- Explain auth methods (API keys, JWT, OAuth)
