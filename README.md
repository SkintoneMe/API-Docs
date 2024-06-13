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
        "id": "<idpredict>",
        "predictedClassName": "mid-dark",
        "predictions": {
            "0": 6.849454052826331e-7,
            "1": 5.806282388221007e-8,
            "2": 0.9927035570144653,
            "3": 0.007295762654393911
        },
        "predictedClassIndex": 2,
        "createdAt": "2024-06-13T16:45:38.267Z",
        "recommendation": [
            "#8c001a",
            "#d7c0d0",
            "#64113f",
            "#2e294e"
        ],
        "jewelryRecommendation": [
            "gold"
        ],
        "colorPaletteImg": [
            "https://storage.googleapis.com/color_recommendation/mid-dark/8c001a.png",
            "https://storage.googleapis.com/color_recommendation/mid-dark/d7c0d0.png",
            "https://storage.googleapis.com/color_recommendation/mid-dark/64113f.png",
            "https://storage.googleapis.com/color_recommendation/mid-dark/2e294e.png"
        ]
    }
}
```
