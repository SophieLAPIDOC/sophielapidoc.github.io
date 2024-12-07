<link rel="stylesheet" type="text/css" href="./assets/css/sophie-custom.css" />

#### Back to [Home](index.md) | [Get started](index.md#get-started) | [Tutorials](index.md#tutorials) | [References](index.md#reference)

## Get all dogs

Get the full list of the dogs registered in the WOOF! API identified by their unique ID.

### Request
<span class="button" id="get">GET</span>`/dog` 


### (Optional) Query Parameters

| Parameter name   | Type   | Description   |   
|---|---|---|
| `size`  | string   | Filter the list by the dog size category: Large, Medium, Large.  |  
| `zip_code`  | string   | Filter the list by the zip code where dog and humans reside.  |   
| `at_the_park_?`  | string   | Filter the list by the dog's presence at the park: Y, N. |     

### Sample request
```
{base_url}/dog?size=Small
```

### Sample response
**Status code:** <span class="status-2xx">200 OK</span>

```json
[
    {
        "name": "Bella",
        "photo": "../Photos/Bella.jpeg",
        "breed": "mini pittie mix",
        "size": "Small",
        "human": "Wendy & Chris",
        "zip_code": "06417",
        "something_about_yourself": "I like dogs with good manners.",
        "at_the_park_?": "Y",
        "park_id": 3,
        "id": 1
    },
    {
        "name": "Eloise",
        "photo": "../Photos/Ellie.jpeg",
        "breed": "Chihuahua mix",
        "size": "Small",
        "human": "Josh & Trish",
        "zip_code": "06109",
        "something_about_yourself": "Big dogs intimidate me!",
        "at_the_park_?": "N",
        "park_id": 1,
        "id": 3
    }
]
```
## Response status

| Status value   | Return status  | Description   | 
|---|---|---|
| 200  | OK (sucess)  | Request successful. The server has responded as required.  | 
| ECONNREFUSED | N/A | Service is offline. Start the service and try again.|

## Other `dog` endpoints
* [Find a dog by ID](dog-get-dog-by-id.md)
* [Add a dog](dog-add-dog.md)
* [Update the details of dog](dog-update-dog.md)
* [Remove a dog](dog-delete-dog.md)