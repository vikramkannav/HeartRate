# Categories

This API is used for the list of Activity categories.

## Activities

```shell
curl -X GET \
  http://base_url/activities \
  -H 'accept: application/json' \
  -H 'authorization: Token token:DDEJKRAS2356' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
```


> The above command returns JSON structured like this:

```json
{
	"activities": [{
			"id": 1,
			"type": "biking"
		},
		{
			"id": 2,
			"type": "bootcamp"
		}
	]

}

```


### HTTP Request

`GET  http://base_url/activities`


### Parameters

    Parameter | Type | Description| Required | Default
    --------- |------- | -----------| -----------| -----------
              |        |           |             |
              
<aside class="success">status:200 OK</aside>
<aside class="warning">status:401 Unauthorized.</aside>

## Habits

This API is used for the list of habit categories.


```shell
curl -X GET \
  http://base_url/habits \
  -H 'accept: application/json' \
  -H 'authorization: Token token:DDEJKRAS2356' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
```


> The above command returns JSON structured like this:

```json
{
	"habits": [{
			"id": 1,
			"type": "vegetarain"
		},
		{
			"id": 2,
			"type": "Alcohol"
		}
	]

}

```


### HTTP Request

`GET  http://base_url/habits`


### Parameters

    Parameter | Type | Description| Required | Default
    --------- |------- | -----------| -----------| -----------
              |        |           |             |

<aside class="success">status:200 OK</aside>
<aside class="warning">status:401 Unauthorized.</aside>