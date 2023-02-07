# Cyderes Coding Challenge (Node.js Server)

This project is built for my Cyderes Coding Challenge (Backend Server/API). It provides a backend GraphQL end-points that handles requests regarding domain name, IPV4, and IPV6 information like who owns the domain name/IP address, is the domain name available, etc.

🚀 [API End Point](https://cydrs-server-dfxzx.ondigitalocean.app/)

## 📦 Built With

- Node.js
- Apollo Server (TypeScript)
- GraphQL
- Docker
- WHOIS API

## 📚 Docs

### Queries

Check out ([src/schema.ts])schema.ts for supported graphQL queries.
Check out ([src/resolvers.ts])resolvers.ts for supported graphQL queries.

#### How to add a new GraphQL query?

1. Create your queries inside `src/schema.ts` and `src/resolvers.ts`, say you want to create a new route to serve foods

Schema.ts -

```ts
// Tells graphQL what end points are available

type Query {
    ...
    // creates a food end point that will take in an input food name and return a string.
    food(foodName: String!): String
}
```

Resolvers.ts -

```ts
// Tells graphQL how to handle those requests/queries

export const resolvers = {
  Query: {
    food(_: any, { foodName }: { foodName: String }) {
      // invoke some functions to get food data
      return "Some data";
    },
  },
};
```

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.<br />
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br />
You will also see any lint errors in the console.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).
