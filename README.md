# Setup

- Installation
  ```
  npm init
  npm install express
  npm install nodemon --save-dev
  npm install dotenv
  npm istall express-async-handler
  npm install mongoose
  npm install bcrypt
  npm install jsonwebtoken

  cp .env.sample .env
  npm run dev
  ```

- Extention:
  + Thunder Client
  + MongoDB for VS Code

- [Mongodb](https://www.mongodb.com/)

# Test API

- Login:
  ```
  curl  -X POST \
    'http://localhost:5000/api/users/login' \
    --header 'Accept: */*' \
    --header 'User-Agent: Thunder Client (https://www.thunderclient.com)' \
    --header 'Content-Type: application/json' \
    --data-raw '{
    "email": "example@gmail.com",
    "password": "password"
  }'
  ```

- Get current user:
  ```
  curl  -X GET \
    'http://localhost:5000/api/users/current' \
    --header 'Accept: */*' \
    --header 'User-Agent: Thunder Client (https://www.thunderclient.com)' \
    --header 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjp7InVzZXJuYW1lIjoiZGFuaCIsImVtYWlsIjoiZXhhbXBsZUBnbWFpbC5jb20iLCJpZCI6IjY3NGZiZDJlM2Q5ZTg2M2Y0NmJhM2NkZSJ9LCJpYXQiOjE3MzMyODAyNzcsImV4cCI6MTczMzI4MTE3N30.KXypcBKWg8n-55EXMWOP57fKW9dRa0DF4uq2skOCKes' \
    --header 'Content-Type: application/json' \
    --data-raw '{
    "email": "example@gmail.com",
    "password": "password"
  }'
  ```