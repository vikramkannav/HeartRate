# Post

## Posts

This is API is used for the user posts.

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
 			"post_id": "3",
 			"post_decription": "post_decription"
 		},
 		{
 			"post_id": "6",
 			"post_decription": "post_decription"
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


