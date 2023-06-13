#User API Spec

##Register User API

EndPoint : POST /api/users

Request Body : 
```json
{
"username" : "Fahrur221",
"password" : "rahasia",
"name" : "FahrurRozi"
}
```
Response Body Success : 

```json
{
    "data" : {
        "useruame" : "Fahrur221",
        "name" : "FahrurRozi"
    }
}
Response Body Error : 

```json
{
    "errors" : "Username Already Taken!",
}
```
##Login User API

Endpoint : POST /api/users/login

Request Body :

```json
{
    "username" : "Rendi099",
    "password" : "rendiganteng",
}
```
Response Body Success : 
```json
{
    "data" : {
        "token" : "unique-token",
    }    
}
```
Response Body Error : 
```json
{
    "errors" : "Username or passowrd Wrong!",
}
```

##Update User API

Endpoint : PATCH /api/users/currentuser

Headers : 
-authorization : Token

Request Body : 
```json
{
    "name" : "new name",    //optional
    "password" : "new password", //optional
}
```
Response Body Success : 
```json
{
    "data" {
        "username" : "new name",
        "password" : "new password",
    }
}
```
Response Body Error : 
```json
{
    "errors" : "name length max 100",
}
```

##Get User API

Headers : 
-authorization : Token

endpoint : GET /api/users/currentuser

Response Body Success : 
```json
{
    "data" {
        "username" : "Rendi099",
        "name" : "rendi",
    }
}
```
Response Body Error : 
```json
{
    "errors" : "unauthorized",
}
```
##Logout User API
Endpoint : DELETE /api/users/logout

Headers : 
-authorization : Token

Response Body Success :
```json
{
    "data" : "OK",
}
```
Response Body Error : 
```json
{
    "errors" : "Unauthorized",
}
```
