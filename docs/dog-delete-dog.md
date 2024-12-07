<link rel="stylesheet" type="text/css" href="./assets/css/sophie-custom.css" />

#### Back to [Home](index.md) | [Get started](index.md#get-started) | [Tutorials](index.md#tutorials) | [References](index.md#reference)

## Remove a dog 
Delete the details of a `dog` from the WOOF! API.

### Request

<span class="button" id="delete">DELETE</span>`/dog/{id}`


### Parameters

| Parameter name   | Type   | Description   |  
|---|---|---|
| `id`  | number   | The record ID of the dog to remove. |  


### Sample request
```
DELETE {base_url}/dog/3
```

## Sample response
Returns an empty object.

**Status code:** <span class="status-2xx">200 OK</span>

```json
{}
```
## Response status

| Status value  | Return status  | Description  | 
|---|---|---|
| 200  | OK (sucess)  | Request successful. The server has responded as required.  | 
| 400  | Not found  | Service is offline. Start the service and try again.  | 
| ECONNREFUSED  | N/A  | Service is offline. Start the service and try again.  |

## Other `dog` endpoints
* [Get all dogs](dog-get-all-dogs.md)
* [Find a dog by ID](dog-get-dog-by-id.md)
* [Add a dog](dog-add-dog.md)
* [Update the details of dog](dog-update-dog.md)