# Post

## Posts

This API is used for the posts those he follow or like users.
With this API user can see the other users posts.

```shell
curl -X GET \
  http://base_url/posts \
  -H 'accept: application/json' \
  -H 'authorization: Token token:DDEJKRAS2356' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
```


> The above command returns JSON structured like this:

```json
 {
 	"posts ": [{
 			"id": "3",
 			"decription": "post_decription"
 		},
 		{
 			"id": "6",
 			"decription": "post_decription"
 		}
 	]
 }
```

### HTTP Request

`GET  http://base_url/posts`


### Parameters

    Parameter | Type | Description| Required | Default
    --------- | ------- | -----------| -----------| -----------
              |         |            |            |
              |         |            |            |

<aside class="success">status:200 OK</aside>
<aside class="warning">status:401 Unauthorized.</aside>


