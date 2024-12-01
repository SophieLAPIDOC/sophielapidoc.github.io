#### Back to [Home](index.md) | [Get started](index.md#get-started) | [Tutorials](index.md#tutorials) | [References](index.md#reference)

## Remove a dog 
Delete the details of a `dog` from the WOOF! API.

### Request
```
DELETE /dog/{id}
```

### Parameters

| Parameter name   | Type   | Description   |  
|---|---|---|
| `id`  | integer   | The record ID of the dog to remove. |  


### Sample request
```
{base_url}/dog/3
```

## Sample response
Returns an empty object.

Status code: `200 OK`

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