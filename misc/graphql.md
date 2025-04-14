# GraphQL

**What it is:**
- A query language and runtime for APIs developed by Facebook
- Lets clients request exactly the data they need — and nothing more

---

## Key Concepts

| Concept       | Description |
|---------------|-------------|
| **Schema**    | Strongly typed contract between server and client |
| **Query**     | Client request for data |
| **Mutation**  | Write/update/delete operations |
| **Subscription** | Real-time data stream (usually over WebSocket) |
| **Resolver**  | Server function that returns data for a field |

---

## Example Schema
```graphql
type User {
  id: ID!
  name: String!
  email: String!
}

type Query {
  users: [User]
  user(id: ID!): User
}

type Mutation {
  createUser(name: String!, email: String!): User
}
```

---

## Example Query
```graphql
query {
  users {
    id
    name
  }
}
```

## Example Mutation
```graphql
mutation {
  createUser(name: "Alice", email: "alice@example.com") {
    id
    name
  }
}
```

---

## Benefits
- Single endpoint (`/graphql`) instead of many REST endpoints
- Reduces over-fetching and under-fetching
- Strong typing improves tooling and documentation
- Built-in introspection

---

## Drawbacks
- Complex caching
- Performance can suffer for large/deep queries
- Harder to implement simple role-based auth
- Overhead if not needed (e.g. for simple CRUD APIs)

---

## Tooling
- **Apollo** (Client/Server, Federation)
- **GraphiQL** / **Altair** (Playground UIs)
- **Relay** (Client caching)
- **Hasura** (GraphQL layer over Postgres)

---

## GraphQL vs REST
| Aspect        | GraphQL                         | REST                          |
|---------------|----------------------------------|-------------------------------|
| Endpoint      | Single                           | Multiple (one per resource)   |
| Data fetching | Precise                          | Fixed responses               |
| Versioning    | Schema evolves                   | Often requires new endpoints  |
| Overhead      | Higher per-query                 | More predictable              |

---

## Interview Tips
- Be able to explain when to use GraphQL vs REST
- Show query/mutation syntax and schema understanding
- Know how resolvers and data sources are wired
- Discuss complexity tradeoffs for caching, auth, and rate limiting
