<link rel="stylesheet" type="text/css" href="./assets/css/sophie-custom.css" />

#### Back to [Home](index.md) | [Get started](index.md#get-started) | [Tutorials](index.md#tutorials) | [References](index.md#reference)

## Get a dog by ID

Get the catalogue details of a single dog identified by its unique ID.

### Request

<span class="button" id="get">GET</span>`/dog/{id}`


### Parameters

|Parameter name   |Type   |Description   |   
|---|---|---|
| `id`  |number   | The ID of the dog record to be updated.   |  

### Sample request
```
GET {base_url}/dog/4
``` 

### Sample response
Returns the details of the dog identified by its unique ID.

**Status code:** <span class="status-2xx">200 OK</span>

```json
{
    "name": "Loki",
    "photo": "../Photos/Loki.jpeg",
    "breed": "Siberian Husky",
    "size": "Large",
    "human": "Sylvana",
    "zip_code": "06040",
    "something_about_yourself": "As long as no balls are involved, I'm very mellow!",
    "at_the_park_?": "N",
    "park_id": 1,
    "id": 4
}
```

## Response status

| Status value   | Return status  | Description   |    
|---|---|---|
| 200  | OK (sucess)  | Request successful. The server has responded as required.  |  
| 404| Not found| Requested resource could not be found.|
| ECONNREFUSED| N/A| Service is offline. Start the service and try again.| 

## Other `dog` endpoints
* [Get all dogs](dog-get-all-dogs.md)
* [Add a dog](dog-add-dog.md)
* [Update the details of dog](dog-update-dog.md)
* [Remove a dog](dog-delete-dog.md)