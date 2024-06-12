# API-Docs
### Register
* Method <br>
POST
* URL <br>
  /register
* Body Request
```
{
    "username": "test",
    "gender": "female",
    "email": "test@email.com",
    "password": "password"
}
```
* Response
```
{
    "status": "success",
    "message": "User created successfully"
}
```
### Login
* Method <br>
POST
* URL <br>
  /login
* Body Request
```
{
    "email": "test@email.com",
    "password": "password"
}
```
* Response
```
{
    "status": "success",
    "message": "login successful",
    "username": "test",
    "data": {
        "token": "<token>"
    }
}
```
### Read User
* Method <br>
GET
* URL <br>
/readUser
* Headers <br>
Key = Authorization <br>
Value = Bearer (token from login)
* Response
```
{
    "status": "success",
    "message": "read successful",
    "data": {
        "id": (user id),
        "username": "test",
        "gender": "female",
        "email": "test@gmail.com"
    }
}
```
### Update User
* Method <br>
PUT
* URL <br>
/updateUser
* Headers <br>
Key = Authorization <br>
Value = Bearer (token from login)
* Body Request
```
{
  "username": "test",
  "gender": "female",
  "email": "test@gmail.com",
  "password": "password"
}
```
* Response
```
{
    "status": "success",
    "message": "update successful"
}
```
### Delete User
* Method <br>
POST
* URL <br>
  /deleteUser
* Headers <br>
Key = Authorization <br>
Value = Bearer (token from login)
* Body Request
```
{
    "password": "password"
}
```
* Response
```
{
    "status": "success",
    "message": "Delete successful"
}
```
### Get History
