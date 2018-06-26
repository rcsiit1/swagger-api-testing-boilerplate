# swagger-api-testing-boilerplate
Swagger is an open source tool to test the APIs made in javascript.The api can be tested based on the paramters set in the datastore.The complete body of the response with the headers and response code is shown on the user interface.Integrating this wonderful tool helps you test and debug your apis quickly in your project.Here is the boiler plate to include in your sails project to start running with the swagger tool.
## Installation

* Clone the git repository.

* Keep the docs folder in assets directory of your sails project.<br/>
![assests hierarchy](/images/assets.png)

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
* Run your project in terminal with *sails lift* command.
* Hit the following URL in your browser window
http://localhost:1337/docs/ <br/><br/><br/>
![swagger-ui](/images/swaggger-ui.png)
<br/><br/>

* Enjoy testing your APIs with swagger on sails js.
