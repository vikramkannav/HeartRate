# Authentication


## Sign up

This API is used for the sign up with email,user name,email id
with password.

This is open API where auth token is not required to passed in the header.

```shell
curl -X POST \
  http://base_url/signup \
  -H 'accept: application/json' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -d '{
	"user" :{
		 "name" :"vikram",
		"email": "vikramkanav",
	    "password":"xyz",
	  }
}'
```

> The above command returns JSON structured like this:

```json
 {
 	"user ": {
 		"name": "vikram",
 		"email":"vikramkanav@gmail.com"
 		"dob": "",
 		"about": "",
 		"gender": "",
 		"occupation": "",
 		"age_range": "",
	 	"dateing": ""
 	},
 	"refresh_token": "iYa1WQuk5_f9Fd04D_Qrrw",
   	"auth_token": "AABB1234",
 }
```

>The above command returns JSON structured like this for failure:

```json
 {
 	"error": "Please enter the valid email and password."
 }
```

### HTTP Request

`POST  http://base_url/signup`


### Parameters

    Parameter | Type | Description| Required | Default
    --------- | ------- | -----------| -----------| -----------
    username  | string  | Name of the user | true |
    email    | string   | Email address of the user | true |
    password | string   | Password of the user | true |

<aside class="success">status:200 OK</aside>
<aside class="warning">422 Unprocessable Entity.</aside>

## Sign in 

This API is used for user sign in with his/her email address and password.

```shell
curl -X POST \
  http://base_url/signin \
  -H 'accept: application/json' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
   -d ' {
 	"user ": {
 		"email": "vikram@headerlab.com",
 		 "password" : "xyzs"
 	}
 }'

```

> The above command returns JSON structured like this:

```json
 {
 	"user ": {
     		"name": "vikram",
     		"dob": "17/07/1984",
     		"about_us": "Text msg",
     		"gender": "Male",
     		"occupation": "IT",
     		"age_range": "20-30",
     		"dateing": "women"
     		  	},
         	"refresh_token": "iYa1WQuk5_f9Fd04D_Qrrw"
            "auth_token": "AABB1234"
         	
 }
```

>The above command returns JSON structured like this for failure:

```json
 {
 	"error": "Please enter the valid email id and password."
 }
```


### HTTP Request

`POST  http://base_url/signin`


### Parameters

    Parameter | Type | Description| Required | Default
    --------- | ------- | -----------| -----------| -----------
    email   | string   | Email of the user | true |
    password | string | Password of the user | true |

<aside class="success">status:200 OK</aside>
<aside class="warning">status:422 Unprocessable Entity.</aside>


## Facebook login

This API is used for the Facebook login with the help of his/her Facebook token.

```shell
curl -X POST \
  http://base_url/signup \
  -H 'accept: application/json' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
    -d ' {
 	"user ": {
 	   "facebook" : "true",
 	   "facebook_token": "facebook_token"
 	}
 }'

```


> The above command returns JSON structured like this:

```json
 {
   "message" : "User login succfully" 
 }

```


### HTTP Request

`POST  http://base_url/signup`


### Parameters

    Parameter | Type | Description| Required | Default
    --------- | ------- | -----------| -----------| -----------
    facebook |boolean  |Facebook of the user | true |
    token    |  string    | Token of the user | true 
    
<aside class="success">status:200 OK</aside>
<aside class="warning">422 Unprocessable Entity.</aside>

##Retrieve access Token

This API is used for the regeneration the Auth token via refresh token. This API is an authentication API request in which needs to pass Auth token in the request header.

```shell
curl -X POST \
  http://base_url/users/:id/refresh_token \
  -H 'accept: application/json' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
 -d '{
    "refresh_token": "iYa1WQuk5_f9Fd04D_Qrrw"
}'
```


> The above command returns JSON structured like this:

```json
  {
    "user": {
                "name": "vikram",
          		"dob": "17/07/1984",
          		"about_us": "Text msg",
          		"gender": "Male",
          		"occupation": "IT",
          		"age_range": "20-30",
          		"dateing": "women"

    },
    "refresh_token": "absgdtydiid123" ,
    "auth_token":"DDEJKRAS2356"
   }

```


### HTTP Request

`POST http://base_url/users/:id/refresh_token`


### Parameters

    Parameter | Type | Description| Required | Default
    --------- | ------- | -----------| -----------| -----------
    refresh_token |	string | true 	| Refresh token of the user|

    
<aside class="success">status:200 OK</aside>
<aside class="warning">422 Unprocessable Entity.</aside>