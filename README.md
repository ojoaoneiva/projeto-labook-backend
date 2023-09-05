<div align="center">
# Labook
</div>

[API Docummentation](https://documenter.getpostman.com/view/27685475/2s9Y5eNzL8)

## About:
The "Labook" project aims to build the backend of a small social media plataform and its API and database, with data source for users, posts, post's comments and likes. The project uses layered architecture and poo to estructure the code.

---

## Functionalities:
- [x]   <strong>Login Page:</strong> The user can connect (if the user and email are valid and previously created) and the app will autenticat the data, and generate an acess token and go to the Feed page.
- [x]  <strong>Sign up Page:</strong> The user can creat an account (with email that haven't been used before), and the app will generate an acess JWT token and go to the Feed page.
- [x]  <strong>Feed page:</strong> Only authorized to be seen if a valid user is logged and the JWT token. The page shows all the posts created by all users.
- [x]  <strong>Like or dislike:</strong> The user can like or dislike a post.
- [x]  <strong>Create post:</strong> The user can create on the textfield a new post.
- [x]  <strong>Edit post:</strong> The user can edit a post if he/she created it.
- [x]  <strong>Delete post:</strong> The user can delete a post if he/she created it.
- [x]  <strong>Layered Architecture:</strong> The app's structure was built and organized with layered architecture to make the code more organized and for its reusability, maintainability and scalability.
- [x]  <strong>Hashed passwords:</strong> All the passwords are hashed using BcryptJS before its storage on the databse, so the information is protected.
- [x]  <strong>Database:</strong> All the users, posts, comments and likes/dislikes information are storaged on an SQLite database in the backend.
---

## How to run the project:

```bash
# Clone the project's repository:
    git clone https://github.com/ojoaoneiva/projeto-labook-backend.git

# Enter the back-end paste:
    cd projeto-labook-backend

# Install the app's dependencies:
    npm i

# Run the application in developpement mode:
    npm run dev

# The server will start on localhost:3003
```
---

## Technologies used:
- Node JS
- Typescript
- Express
- SQLite
- Knex
- UUID
- BcryptJS
- JWT
- ZOD
- POO
- Express router
- Layred Architecture
- Postman
---
