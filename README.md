# GraphQL TypeScript Server

A fully functional **GraphQL API server** built with Apollo Server, Express, and TypeScript for managing car data with complete CRUD operations.

This project demonstrates how to design a GraphQL schema, implement queries and mutations, and structure a TypeScript-based backend application.

---

## 🚀 Tech Stack

* **Apollo Server** – GraphQL server engine
* **Express** – HTTP server framework
* **TypeScript** – Type-safe backend development
* **GraphQL** – Query language & execution engine
* **CORS** – Cross-origin resource sharing
* **Body Parser** – Request parsing middleware

---

## 📁 Project Structure

```
src/
  ├── server.ts      - Apollo Server setup and Express configuration
  ├── schema.ts      - GraphQL type definitions
  ├── resolver.ts    - Query and mutation resolvers
package.json         - Dependencies and scripts
tsconfig.json        - TypeScript configuration
```

---

## ⚙️ Installation

1. Clone the repository:

```bash
git clone https://github.com/AboubacarSow/graph-ts-server.git
cd graph-ts-server
```

2. Install dependencies:

```bash
npm install
```

---

## ▶️ Running the Server

Start the development server:

```bash
npm start
```

The GraphQL endpoint will be available at:

```
http://localhost:4000/graphql
```

You can use Apollo Sandbox or any GraphQL client to test the API.

---

## 📜 API Schema

### 🏎 Type: `Car`

| Field   | Type    | Description         |
| ------- | ------- | ------------------- |
| id      | ID!     | Unique identifier   |
| carType | String! | Type of car         |
| color   | String! | Car color           |
| year    | Int!    | Year of manufacture |

---

## 🔍 Queries

### `getCars`

Returns all cars.

### `getOne(id: ID!)`

Returns a single car by ID.

---

## ✏️ Mutations (CRUD)

### `addCar(carType: String!, color: String!, year: Int!)`

Creates a new car.

### `editCar(id: ID!, carType: String!, color: String!)`

Updates an existing car.

### `deleteCar(id: ID!)`

Deletes a car by ID.

---

## 📌 Example Usage

### Query All Cars

```graphql
query {
  getCars {
    id
    carType
    color
    year
  }
}
```

---

### Query Single Car

```graphql
query {
  getOne(id: 1) {
    id
    carType
    color
    year
  }
}
```

---

### Add Car

```graphql
mutation {
  addCar(carType: "Tesla Model 3", color: "Red", year: 2024) {
    id
    carType
    color
    year
  }
}
```

---

### Edit Car

```graphql
mutation {
  editCar(id: 1, carType: "SUV", color: "Black") {
    id
    carType
    color
    year
  }
}
```

---

### Delete Car

```graphql
mutation {
  deleteCar(id: 1) {
    id
    carType
    color
    year
  }
}
```

---

## 🧠 What This Project Demonstrates

* GraphQL schema design
* Nullability handling
* Resolver implementation
* In-memory data management
* Type-safe backend development with TypeScript
* Express middleware integration with Apollo Server

---

## ⚠️ Notes

* Data is stored in memory (no database persistence).
* Restarting the server resets all data.
* This project is intended for learning and experimentation.

---

## 📄 License

ISC


