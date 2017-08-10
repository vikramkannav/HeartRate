# User

## Followers

This API is used to show the followers by the user.

```shell
curl -X GET \
  http://base_url/followers \
  -H 'accept: application/json' \
  -H 'authorization: Token token:DDEJKRAS2356' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
 ```


> The above command returns JSON structured like this:

```json

 {
 	"users ": [{
 			"user_id": "5",
 			"name": "vikram",
 			"dob": "17/07/1984",
 			"about_us": "Text msg",
 			"gender": "Male",
 			"occupation": "IT",
 			"age_range": "20-30",
 			"dating": "women"
 		},
 		{
 			"user_id": "7",
 			"name": "sumit",
 			"dob": "17/07/1984",
 			"about_us": "Text msg",
 			"gender": "Male",
 			"occupation": "IT",
 			"age_range": "20-30",
 			"dating": "women"
 		}
 	]
 }
```


### HTTP Request

`GET  http://base_url/followers`


### Parameters

    Parameter | Type | Description| Required | Default
    --------- | ------- | -----------| -----------| -----------
              |         |            |            |
              |         |            |            |

<aside class="success">status:200 OK</aside>
<aside class="warning">status:401 Unauthorized.</aside>

## Following

This API is used to show the following the user.

```shell
curl -X GET \
  http://base_url/following \
  -H 'accept: application/json' \
  -H 'authorization: Token token:DDEJKRAS2356' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
 ```


> The above command returns JSON structured like this:

```json

  {
    	"users ": [{
    			"id": "4",
    			"name": "Ram",
               "dob": "17/07/1984",
               "about_us": "Text msg",
               "gender": "Male",
               "occupation": "IT",
               "age_range": "20-30",
               "dateing": "women"
           	},
    		{
    			"id": "9",
    			"name": "Gyan",
               "dob": "17/07/1984",
               "about_us": "Text msg",
               "gender": "Male",
               "occupation": "IT",
               "age_range": "20-30",
               "dateing": "women"
          	}
    	]
    }
```


### HTTP Request

`GET  http://base_url/following`


### Parameters

    Parameter | Type | Description| Required | Default
    --------- | ------- | -----------| -----------| -----------
              |         |            |            |
              |         |            |            |
<aside class="success">status:200 OK</aside>
<aside class="warning">status:401 Unauthorized.</aside>

##Follow

This API is used to follow by the user.

```shell
curl -X POST \
  http://base_url/users/:id/follow \
  -H 'accept: application/json' \
  -H 'authorization: Token token:DDEJKRAS2356' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \

 ```
 
 
> The above command returns JSON structured like this:

```json
 {
 	"message" : "user follow successfully " 
 }
```

### HTTP Request

`POST  http://base_url/users/:id/follow`

### Parameters

    Parameter | Type | Description| Required | Default
    --------- | ------- | -----------| -----------| -----------
              |         |            |            |
              |         |            |            |

<aside class="success">status:200 OK</aside>
<aside class="warning">status:422 Unprocessable Entity.</aside>

##Un Follow

This API is used to unfollow by the user.

```shell
curl -X POST \
  http://base_url/users/:id/unfollow\
  -H 'accept: application/json' \
  -H 'authorization: Token token:DDEJKRAS2356' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
 ```
 
 
> The above command returns JSON structured like this:

```json
  {
  	"message" : "user un follow successfully " 
  }
```


### HTTP Request

`POST http://base_url/users/:id/unfollow`


### Parameters

    Parameter | Type | Description| Required | Default
    --------- | ------- | -----------| -----------| -----------
              |         |            |            |
  
<aside class="success">status:200 OK</aside>
<aside class="warning">status:422 Unprocessable Entity.</aside>
  
            
##Block user

This API is used to block the user by using.

```shell
curl -X DELETE \
   http:/base_url/users/:id/block\
  -H 'accept: application/json' \
  -H 'authorization: Token token:DDEJKRAS2356' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
 ```
 
 
> The above command returns JSON structured like this:

```json
  {
  	"message" : "user block successfully " 
  }
```


### HTTP Request

`POST http:/base_url/users/:id/block`


### Parameters

    Parameter | Type | Description| Required | Default
    --------- | ------- | -----------| -----------| -----------
              |         |            |            |
 
<aside class="success">status:200 OK</aside>
<aside class="warning">status:422 Unprocessable Entity.</aside>

            
##User unblock

This API is used to unblock the user by using.

```shell
curl -X DELETE \
  -H 'accept: application/json' \
  -H 'authorization: Token token:DDEJKRAS2356' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
 ```
 
 
> The above command returns JSON structured like this:

```json
  {
  	"message" : "user unblock successfully " 
  }
```


### HTTP Request

`POST http://base_url/users/:id/unblock`


### Parameters

    Parameter | Type | Description| Required | Default
    --------- | ------- | -----------| -----------| -----------
              |         |            |            |
            
<aside class="success">status:200 OK</aside>
<aside class="warning">status:422 Unprocessable Entity.</aside>

##Report user

This API is used to report the another user by using.

```shell
curl -X POST \
  http://base_url/users/:id/report \
  -H 'accept: application/json' \
  -H 'accept: application/json' \
  -H 'authorization: Token token:DDEJKRAS2356' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
 ```
 
 
> The above command returns JSON structured like this:

```json
  {
  	"message" : "user report successfully " 
  }
```


### HTTP Request

`POST http://base_url/users/:id/report`


### Parameters

    Parameter | Type | Description| Required | Default
    --------- | ------- | -----------| -----------| -----------
              |         |            |            |
            
<aside class="success">status:200 OK</aside>
<aside class="warning">status:422 Unprocessable entry.</aside>


## Notification

This API is used to, he/she gets the notification post by another user follow with him.
```shell
curl -X POST \
  http://base_url/users/:id/notification\
  -H 'accept: application/json' \
  -H 'accept: application/json' \
  -H 'authorization: Token token:DDEJKRAS2356' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
 ```
 
 
> The above command returns JSON structured like this:

```json
  {
  	"message" : "User notification get successfully" 
  }
```


### HTTP Request

`POST http://base_url/users/:id/notification`


### Parameters

    Parameter | Type | Description| Required | Default
    --------- | ------- | -----------| -----------| -----------
              |         |            |            |
            
<aside class="success">status:200 OK</aside>
<aside class="warning">status:422 Unprocessable Entity.</aside>


## Like user

This API is used to like another user by him. 

```shell
curl -X POST \
  http://base_url/users/:id/like \
  -H 'accept: application/json' \
  -H 'accept: application/json' \
  -H 'authorization: Token token:DDEJKRAS2356' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
 ```
 
 
> The above command returns JSON structured like this:

```json
  {
  	"message" : "User like successfully" 
  }
```


### HTTP Request

`POST http://base_url/users/:id/like`


### Parameters

    Parameter | Type | Description| Required | Default
    --------- | ------- | -----------| -----------| -----------
              |         |            |            |
            
<aside class="success">status:200 OK</aside>
<aside class="warning">status:422 Unprocessable Entity.</aside>


## Unlike user

This API is used to unlike the other user by him.

```shell
curl -X DELETE \
  http://base_url/users/:id/unlike \
  -H 'accept: application/json' \
  -H 'accept: application/json' \
  -H 'authorization: Token token:DDEJKRAS2356' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
 ```
 
 
> The above command returns JSON structured like this:

```json
  {
  	"message" : "User unlike successfully" 
  }
```


### HTTP Request
:
`DELETE http://base_url/users/:id/unlike`


### Parameters

    Parameter | Type | Description| Required | Default
    --------- | ------- | -----------| -----------| -----------
              |         |            |            |
            
<aside class="success">status:200 OK</aside>
<aside class="warning">status:422 Unprocessable Entity.</aside>
