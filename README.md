# Labook

Go to the API Docummentation [here](https://documenter.getpostman.com/view/27685475/2s9Y5eNzL8)

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

```

# Exemplos de requisição

## Login
Endpoint público utilizado para login. Devolve um token jwt.
```typescript
// request POST /users/login
// body JSON
{
  "email": "beltrana@email.com",
  "password": "beltrana00"
}

// response
// status 200 OK
{
  token: "um token jwt"
}
```


## Create post
Endpoint protegido, requer um token jwt para acessá-lo.
```typescript
// request POST /posts
// headers.authorization = "token jwt"
// body JSON
{
    "content": "Partiu happy hour!"
}

// response
// status 201 CREATED
```


## Get posts
Endpoint protegido, requer um token jwt para acessá-lo.
```typescript
// request GET /posts
// headers.authorization = "token jwt"

// response
// status 200 OK
[
    {
        "id": "uma uuid v4",
        "content": "Hoje vou estudar POO!",
        "likes": 2,
        "dislikes" 1,
        "createdAt": "2023-01-20T12:11:47:000Z"
        "updatedAt": "2023-01-20T12:11:47:000Z"
        "creator": {
            "id": "uma uuid v4",
            "name": "Fulano"
        }
    },
    {
        "id": "uma uuid v4",
        "content": "kkkkkkkkkrying",
        "likes": 0,
        "dislikes" 0,
        "createdAt": "2023-01-20T15:41:12:000Z"
        "updatedAt": "2023-01-20T15:49:55:000Z"
        "creator": {
            "id": "uma uuid v4",
            "name": "Ciclana"
        }
    }
]
```

