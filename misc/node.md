# Node.js

**What it is:**
- A runtime for executing JavaScript code server-side, built on Chrome's V8 engine
- Used for building fast, scalable network applications
- Popular in backend APIs, full-stack JS apps, and tooling

---

## Key Features

| Feature        | Description |
|----------------|-------------|
| **Event Loop** | Non-blocking I/O with async/callback-based concurrency |
| **Single Threaded** | Lightweight thread model using events |
| **npm**         | Node package manager — massive open-source ecosystem |
| **Modules**     | ES Modules (`import`) or CommonJS (`require`) |
| **Express**     | Minimalist framework for building REST APIs |

---

## Basic Example
```js
const express = require('express');
const app = express();

app.get('/', (req, res) => {
  res.send('Hello, world!');
});

app.listen(3000, () => {
  console.log('Server started on port 3000');
});
```

---

## Common Tools
- `nodemon` – reload app on file changes
- `dotenv` – load environment variables
- `eslint` – static analysis and linting
- `jest` / `mocha` – testing frameworks
- `axios` / `node-fetch` – HTTP requests

---

## Asynchronous Patterns
```js
// Callback
fs.readFile('file.txt', (err, data) => {...});

// Promise
fs.promises.readFile('file.txt').then(data => {...});

// async/await
const data = await fs.promises.readFile('file.txt');
```

---

## Use Cases
- REST and GraphQL APIs
- CLI tools
- Real-time apps with WebSockets
- Serverless functions (e.g. AWS Lambda using Node.js)
- Dev tooling (e.g. Webpack, ESLint)

---

## Interview Tips
- Understand the event loop and async flow
- Know when to use `require` vs `import`
- Explain middleware pattern in Express
- Be able to test with `jest`, mock APIs, and handle errors
