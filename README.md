# swagger-api-testing-boilerplate

###Installation

1.Clone the git repository.
2.Keep the docs folder in assets directory of your sails project.
3. Then change in *swag.json*
```javascript
"host": "localhost:1337",
  "basePath": "/",
```

4. Add the api routes you want to test in *swag.json*
```javascript
"paths": {    
    "/students/createStudent": {
      "post": {
        "tags": [
          "User"
        ],
        "summary": "Signup API",
        "produces": [
          "application/xml"
        ],
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
