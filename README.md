# swagger-api-testing-boilerplate

##Installation

*Clone the git repository.
*Keep the docs folder in assets directory of your sails project.
* Then change in *swag.json*
```javascript
"host": "localhost:1337",
  "basePath": "/",
```

* Add the api routes you want to test in *swag.json*
```javascript
"paths": {  
//this the route to check api
    "/students/createStudent": {
      "post": {
        "tags": [
          "User"
        ],
        "summary": "Signup API",
        "produces": [
          "application/xml"
        ],
        // the parameters that the api uses
        "parameters": [
          {
            "name": "name",
            "in": "formData",
            "description": "Fullname",
            "required": true,
            "type": "string"
          },
          {
            "name": "roll_number",
            "in": "formData",
            "description": "roll_number",
            "type": "integer"
          },
          {
            "name": "profile_pic",
            "in": "formData",
            "description": "Profil Picture",
            "required": true,
            "type": "string"
          }
        ]
      }
    },
    "/login": {
      "post": {
        "tags": [
          "User"
        ],
        "summary": "Signin API",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "email",
            "in": "formData",
            "description": "Email",
            "type": "string"
          },
          {
            "name": "password",
            "in": "formData",
            "description": "Password",
            "type": "string"
          }
        ]
      }
    }
```
