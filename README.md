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
    "message": "User created successfully!"
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
    "message": "Login successful!"
}
```
### Read User
* Method <br>
GET
* URL <br>
/getUser
* Response
```
{
    "status": "success",
    "message": "get user successful!",
    "data": {
        "username": "test",
        "gender": "female",
        "email": "test@email.com"
    }
}
```
### Update User
* Method <br>
PUT
* URL <br>
/updateUser
* Body Request
```
{
    "newUsername": "test",
    "newGender": "male",
    "newPassword": "test",
    "newEmail": "test@email.com"
}
```
* Response
```
{
    "status": "success",
    "message": "User updated successfully!"
}
```
### Delete User
### Get History
