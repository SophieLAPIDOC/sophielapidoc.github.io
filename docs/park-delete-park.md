<link rel="stylesheet" type="text/css" href="./assets/css/sophie-custom.css" />

#### Back to [Home](index.md) | [Get started](index.md#get-started) | [Tutorials](index.md#tutorials) | [References](index.md#reference)

## Remove a park
Delete the details of a `par` from the WOOF! API.

### Request

<span class="button" id="delete">DELETE</span>`/park/{id}`


## Parameters

| Parameter name   | Type   | Description   |   
|---|---|---|
| `id`  | number   | The record ID of the park to remove. |   

## Sample request
```
{base_url}/park/6
```


## Sample response

**Status code:** <span class="status-2xx">200 OK</span>

Returns an empty `park` object.

```json
{}
```

## Response status

| Status value   | Return status  | Description   |   
|---|---|---|
| 200  | OK (success)  | Request successful. The server has responded as required.  |  
| 404 | Not found | Requested resource could not be found. |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

## Other `park` endpoints
* [Get all parks](park-get-all-parks.md)
* [Find a park by ID](park-get-park-by-id)
* [Add a park](park-add-new-park.md)
* [Update the details of park](park-update-park.md)
