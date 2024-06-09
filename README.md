# API-Docs
### Register
* method
<br>POST
* URL
### Login
### Read User
* Method <br>
GET
* URL <br>
/getUser
* Response
```
{
    "status": "success",
    "message": "get successful",
    "data": {
        "username": "asfia",
        "gender": "male",
        "email": "asfia@gmail.com"
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
    "newUsername": "asfia",
    "newGender": "male",
    "newPassword": "asfia",
    "newEmail": "asfia@gmail.com"
}
```
* Response
```
{
    "success": true,
    "message": "User updated successfully!"
}
```
### Delete User
### Get History
