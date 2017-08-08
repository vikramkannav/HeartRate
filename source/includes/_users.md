# User

## Followers

```shell
curl -X GET \
  http://base_url/followers \
  -H 'accept: application/json' \
  -H 'authorization: Token token:AABB1234' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
 ```


> The above command returns JSON structured like this:

```json

 {
 	"user ": [{
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

```shell
curl -X GET \
  http://base_url/following \
  -H 'accept: application/json' \
  -H 'authorization: Token token:AABB1234' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
 ```


> The above command returns JSON structured like this:

```json

  {
    	"user ": [{
    			"user_id": "4",
    			"name": "Ram",
               "dob": "17/07/1984",
               "about_us": "Text msg",
               "gender": "Male",
               "occupation": "IT",
               "age_range": "20-30",
               "dateing": "women",
           	},
    		{
    			"user_id": "9",
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

```shell
curl -X POST \
  http://base_url/user/:id/follow \
  -H 'accept: application/json' \
  -H 'authorization: Token token:AABB1234' \
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

`POST  http://base_url/user/:id/follow`

### Parameters

    Parameter | Type | Description| Required | Default
    --------- | ------- | -----------| -----------| -----------
              |         |            |            |
              |         |            |            |

<aside class="success">status:200 OK</aside>
<aside class="warning">status:422 Unprocessable entry.</aside>

##Un Follow

```shell
curl -X POST \
  http://base_url/follow/ \
  -H 'accept: application/json' \
  -H 'authorization: Token token:AABB1234' \
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

`POST http://base_url/user/:id/unfollow`


### Parameters

    Parameter | Type | Description| Required | Default
    --------- | ------- | -----------| -----------| -----------
              |         |            |            |
  
<aside class="success">status:200 OK</aside>
<aside class="warning">status:422 Unprocessable entry.</aside>
  
            
##Block User

```shell
curl -X POST \
  http://post/%20http:/base_url/user//block \
  -H 'accept: application/json' \
  -H 'authorization: Token token:AABB1234' \
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

`POST http:/base_url/user/:id/block`


### Parameters

    Parameter | Type | Description| Required | Default
    --------- | ------- | -----------| -----------| -----------
              |         |            |            |
 
<aside class="success">status:200 OK</aside>
<aside class="warning">status:422 Unprocessable entry.</aside>

            
##User Unblock

```shell
curl -X POST \
  http://post/%20http:/base_url/user//unblock/ \
  -H 'accept: application/json' \
  -H 'authorization: Token token:AABB1234' \
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

`POST http://base_url/user/:id/unblock`


### Parameters

    Parameter | Type | Description| Required | Default
    --------- | ------- | -----------| -----------| -----------
              |         |            |            |
            
<aside class="success">status:200 OK</aside>
<aside class="warning">status:422 Unprocessable entry.</aside>

##Report User

```shell
curl -X POST \
  http://base_url/user//report \
  -H 'accept: application/json' \
  -H 'accept: application/json' \
  -H 'authorization: Token token:AABB1234' \
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

`POST http://base_url/user/:id/report`


### Parameters

    Parameter | Type | Description| Required | Default
    --------- | ------- | -----------| -----------| -----------
              |         |            |            |
            
<aside class="success">status:200 OK</aside>
<aside class="warning">status:422 Unprocessable entry.</aside>


## Notification

```shell
curl -X POST \
  http://base_url/user/notification \
  -H 'accept: application/json' \
  -H 'accept: application/json' \
  -H 'authorization: Token token:AABB1234' \
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

`GET http://base_url/user/notification`


### Parameters

    Parameter | Type | Description| Required | Default
    --------- | ------- | -----------| -----------| -----------
              |         |            |            |
            
<aside class="success">status:200 OK</aside>
<aside class="warning">status:401 Unauthorized.</aside>


## Like User

```shell
curl -X POST \
  http://base_url/user/:id/like \
  -H 'accept: application/json' \
  -H 'accept: application/json' \
  -H 'authorization: Token token:AABB1234' \
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

`POST http://base_url/user/:id/like`


### Parameters

    Parameter | Type | Description| Required | Default
    --------- | ------- | -----------| -----------| -----------
              |         |            |            |
            
<aside class="success">status:200 OK</aside>
<aside class="warning">status:422 Unprocessable entry.</aside>


## Unlike User

```shell
curl -X POST \
  http://base_url/user/:id/unlike \
  -H 'accept: application/json' \
  -H 'accept: application/json' \
  -H 'authorization: Token token:AABB1234' \
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
:
`POST http://base_url/user/:id/unlike`


### Parameters

    Parameter | Type | Description| Required | Default
    --------- | ------- | -----------| -----------| -----------
              |         |            |            |
            
<aside class="success">status:200 OK</aside>
<aside class="warning">status:422 Unprocessable entry.</aside>
