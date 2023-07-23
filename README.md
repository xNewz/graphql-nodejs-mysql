# React + GraphQL + Node.js + MySQL

## Description
This is a simple project to demonstrate how to use React, GraphQL, Node.js and MySQL together.

## How to run
1. Clone this repository
2. Run `yarn' or 'npm install' in the client folder
3. Run `yarn' or 'npm install' in the server folder

## How to run the server
1. Run `yarn start' or 'npm start' in the server folder
2. Open http://localhost:3001/graphql to see the GraphQL playground
3. Run the following query to create a new user:
```
mutation {
  createUser(name: "John Doe", username: "john.doe", password: "1234") {
    id
    name
    username
    password
  }
}
```
4. Run the following query to get the user:
```
query {
  getAllUsers{
    id
    name
    username
    password
  }
}
```
5. Run the following query to delete the user:
```
mutation {
  deleteUser(id: 5) {
    message
  }
}
```
6. Run the following query to update the user password:
```
mutation {
  updatePassword(username: "john.doe", oldPassword: "1234", newPassword: "112233") {
    message
  }
}
```

## How to run the client
1. Run `yarn start' or 'npm start' in the client folder
2. Open http://localhost:3000 to see the React app
3. You can create a new user, get all users, delete a user and update a user password