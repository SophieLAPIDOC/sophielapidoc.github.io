# [WOOF! API Reference](index.md#reference)
## Find a park by ID

Get the details of a single park identified by its unique ID.

### Request
```
GET /park/{id}
```

## Parameters

|Parameter name   |Type   |Description   |   
|---|---|---|
| `id`  |integer  | Park's record ID.   |

### Sample request
```
{base_url}/park/4
``` 

## Sample response
Status code: `200 OK`

```json
{
    "park_name": "Rocky Hill Dog Park",
    "town": "Rocky Hill",
    "coordinates": "41.660178, -72.648414",
    "hours": "6 AM - 6 PM",
    "amenities": "water bowls, poop bags",
    "comments": "Lot of dogs at noon",
    "rating": "4",
    "id": 4
}
```

## Response status
|Status value   |Return status  |Description   |   
|---|---|---|
|200  |OK (sucess)  | Request successful. The server has responded as required.  |  
|404|Not found|Requested resource could not be found.|
|ECONNREFUSED|N/A|Service is offline. Start the service and try again.|
