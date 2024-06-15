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
    "email": "test@gmail.com",
    "gender": "female",
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
### Predict
* Method <br>
POST
* URL <br>
  /predict
* Headers <br>
Key = Authorization <br>
Value = Bearer (token from login)
* Body Request
Key = image <br>
Value = (select files)
* Response
```
{
    "status": "success",
    "message": "Model predicted successfully",
    "data": {
        "id": "48a7995a-7591-4917-8005-e7f3936158fd",
        "predictedClassName": "dark",
        "predictions": {
            "0": 0.8377628326416016,
            "1": 0.000004212452950014267,
            "2": 0.16201093792915344,
            "3": 0.00022200567764230072
        },
        "predictedClassIndex": 0,
        "createdAt": "2024-06-15T07:27:25.277Z",
        "recommendation": [
            "#03045e",
            "#832161",
            "#363062",
            "#751628"
        ],
        "jewelryRecommendation": [
            "gold"
        ]
    }
}
```
