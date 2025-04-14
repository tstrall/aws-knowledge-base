# Swagger / OpenAPI

**What it is:**
- **Swagger** is a set of tools for defining, documenting, and testing REST APIs
- **OpenAPI** is the specification format (formerly known as Swagger)
- Commonly used for API design, validation, and integration

---

## Core Concepts

| Concept     | Description |
|-------------|-------------|
| **OpenAPI Spec** | YAML/JSON contract describing the API |
| **Swagger UI**   | Interactive API explorer for testing endpoints |
| **Swagger Editor** | Online tool to write/validate OpenAPI specs |
| **Swagger Codegen** | Generate client/server SDKs from spec |

---

## Sample OpenAPI Spec (YAML)
```yaml
openapi: 3.0.0
info:
  title: User API
  version: 1.0.0
paths:
  /users:
    get:
      summary: List users
      responses:
        '200':
          description: OK
          content:
            application/json:
              schema:
                type: array
                items:
                  $ref: '#/components/schemas/User'
components:
  schemas:
    User:
      type: object
      properties:
        id:
          type: integer
        name:
          type: string
```

---

## Key Benefits
- **Self-documenting APIs**: Clear, consistent, up-to-date docs
- **Interactive testing**: Try endpoints via Swagger UI
- **Client/server generation**: Generate boilerplate code
- **Contract-first development**: Define spec before implementation

---

## Tools
- **Swagger UI**: Browser-based, hosted on `/swagger-ui.html`
- **Swagger Editor**: [editor.swagger.io](https://editor.swagger.io)
- **Swagger Codegen / OpenAPI Generator**: SDKs in Java, Python, etc.
- **Redoc**: Alternative to Swagger UI with better theming

---

## Best Practices
- Use OpenAPI 3.0+ (or 3.1)
- Document all status codes and error messages
- Validate your spec (CI integration recommended)
- Define reusable components (`schemas`, `parameters`, `responses`)

---

## Interview Tips
- Know how Swagger enables contract-first API development
- Be able to read/write OpenAPI YAML and explain structure
- Understand how API gateways (e.g., AWS API Gateway) integrate with OpenAPI
