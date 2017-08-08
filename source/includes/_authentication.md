# Authentication


## Sign Up

This API is used for the sign up with email user name,email id
with password.

This is open API where auth token is not required to passed in the header.


```shell
curl -X POST \
  http://base_url/users/sign_up \
  -H 'accept: application/json' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -d '{
	"user" :{
		 "user_name" :"vikram",
		"email": "vikramkanav",
	    "password":"xyz",
	  }
}'
```

> The above command returns JSON structured like this:

```json
 {
 	"user ": {
 		"name": "",
 		"dob": "",
 		"about_us": "",
 		"gender": "",
 		"occupation": "",
 		"age_range": "",
	 	"refresh_token": "iYa1WQuk5_f9Fd04D_Qrrw",
 		"dateing": ""
 	},
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

`POST  http://base_url/users/sign_up`


### Parameters

    Parameter | Type | Description| Required | Default
    --------- | ------- | -----------| -----------| -----------
    user  | string  | user_name of the user | true |
    email    | string   | email of the user | true |
    password | string   | password of the user | true |

<aside class="success">status:200 OK</aside>
<aside class="warning">422 Unprocessable entry.</aside>



## Update Profile

This API is used for the user update profile.
 

```shell
curl -X POST \
  http://base_url/users \
  -H 'accept: application/json' \
  -H 'authorization: Token token:AABB1234' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
   -d ' {
 	"user ": {
 		"name": "vikram sharma",
 		"dob": "17/07/1984",
 		"about_us": "Text msg",
 		"gender": "Male",
 		"occupation": "IT",
 		"age_range": "20-30",
 		"date_with": "women"
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
     		"date_with": "women",
         	"refresh_token": "iYa1WQuk5_f9Fd04D_Qrrw"
     	},
         	"auth_token": "AABB1234"
 }
```
>The above command returns JSON structured like this for failure:

```json
 {
 	"error": "Please enter the valid format of date ."
 }
```

### HTTP Request

`PUT  http://base_url/users`


### Parameters

    Parameter | Type | Description| Required | Default
    --------- | ------- | -----------| -----------| -----------
     name     | string  | name of the user |true | 
     dob      | date  | dob of the user |true | 
     about_us | text  | about_us of the user |true | 
     gender   | string  | gender of the user |true | 
     occupation  | string | occupation of the user |true | 
     age_range   |text | age_range of the user |true | 
     dateing   | string  | dateing of the user |true | 

<aside class="success">status:200 OK</aside>
<aside class="warning">status:422 Unprocessable entry.</aside>
     
     
     
## Login

This API is used for the sign in.

```shell
curl -X POST \
  http://base_url/users/sign_in \
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
     		"dateing": "women",
     		"refresh_token": "iYa1WQuk5_f9Fd04D_Qrrw"
     	},
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

`POST  http://base_url/users/sign_in`


### Parameters

    Parameter | Type | Description| Required | Default
    --------- | ------- | -----------| -----------| -----------
    email   | string   | email of the user | true |
    password | string | password of the user | true |

<aside class="success">status:200 OK</aside>
<aside class="warning">status:422 Unprocessable entry.</aside>

## Facebook login

This API is used for the facebook sign in

```shell
curl -X POST \
  http://base_url/users/sign_up \
  -H 'accept: application/json' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
    -d ' {
 	"user ": {
 	   "facebook" : "true",
 	   "facebook_tooken": "facebook_tooken"
 	}
 }'

```


> The above command returns JSON structured like this:

```json
 {
   "message" : "user login succfully" 
 }

```


### HTTP Request

`POST  http://base_url/users/sign_up`


### Parameters

    Parameter | Type | Description| Required | Default
    --------- | ------- | -----------| -----------| -----------
    facebook |boolen  |facebook of the user | true |
    token    |  string    | token of the user | true 
    
<aside class="success">status:200 OK</aside>
<aside class="warning">422 Unprocessable entry.</aside>

##Retrieve access Token

This API is used for the regenerating the auth token via refresh token. This API is an authentication API request in which needs to pass auth token in the request header.


```shell
curl -X POST \
  http://base_url/users/sign_up \
  -H 'accept: application/json' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
    -d ' {
 	"user ": {
 	   "facebook" : "true",
 	   "facebook_tooken": "facebook_tooken"
 	}
 }'

```


> The above command returns JSON structured like this:

```json
 {
   "message" : "user login succfully" 
 }

```


### HTTP Request

`POST http://base_url.com/api/refresh_token`


### Parameters

    Parameter | Type | Description| Required | Default
    --------- | ------- | -----------| -----------| -----------
    refresh_token |	string | true 	| refresh_token of the user|

    
<aside class="success">status:200 OK</aside>
<aside class="warning">422 Unprocessable entry.</aside>