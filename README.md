# cipta-integrasi-nusantara-backend


## GET STARTED

- run "npm i"
- run sequelize commands to setup database
- copy .dotenv-example and rename it to .dotenv
- replace SECRET_KEY to actual secret key
- run "npm run dev"

## Endpoints

### POST /register

- body
```
{
    name : "jovi",
    email : "jovi@test.com",
    password : "1234"
}
```

- response 
```
{
  "message": "User with email jovi@mail.com is created"
}
```

### POST /login

- body
```
{
    email : "jovi@test.com",
    password : "1234"
}
```

- response 
```
{
  "message": "Login success",
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6NSwibmFtZSI6bnVsbCwiZW1haWwiOiJqb3ZpQG1haWwuY29tIiwiaWF0IjoxNjkwMjExNTU2fQ.QsDdGcF5UEufuveTXnrMZjCT8LEn-D5L4qwyhE0ubGM"
}
```

### GET /me

- headers
```
{
    token : "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6NSwibmFtZSI6bnVsbCwiZW1haWwiOiJqb3ZpQG1haWwuY29tIiwiaWF0IjoxNjkwMjExNTU2fQ.QsDdGcF5UEufuveTXnrMZjCT8LEn-D5L4qwyhE0ubGM"
}
```

- response 
```
{
  "id": 1,
  "name": "Jovi Petra",
  "email": "jovi@test.com",
  "iat": 1690211162
}
```

