<link rel="stylesheet" type="text/css" href="./assets/css/sophie-custom.css" />

#### Back to [Home](index.md) | [Get started](index.md#get-started) | [Tutorials](index.md#tutorials) | [References](index.md#reference)

## Update the details of a dog
Change any of the proprties for an existing `dog` entry.

### Request

<span class="button" id="put">PUT</span>`/dog/{id}`

### Request Headers
**Content-Type**: `application/json`

### Request body
When using the **PUT** method include  all the `dog` resource properties as listed in [dog resource](dog-ref.md) and change the values, as required.

|Property name   |Type   |Description   |   
|---|---|---|
| `name`  |string   | (Mandatory) The name of the dog.  |
| `photo`  |string   | (Optional) File path to the dog's photo, if supplied  |   
| `breed`  |string   | (Mandatory) The breed of the dog.  |   
| `size`  |string   | The size category of the dog: Small, Medium, Large.  |   
| `human`  |string  | (Mandatory) The name of the owner or person in charge. Multiple values allowed if comma separated. Can be full name or first name only.  | 
| `zip_code`  |string   | Zip Code where dog(s) and human(s) reside.  |   
| `something_about_yourself`  |string   | (Optional) A short description of the dog's character personality.  |   
| `at_the_park_?`  |string   | Whether the dog is at the park right now: True/False. Default value is False. |   
| `park_id`  | number  | The record ID of the park.  |   
| `id`  | number  | The record ID of the dog.  |

### Sample request
```
PUT {base_url}/dog/8
```

### Sample body

```json
{
    "name": "Beckett Jr.",
    "photo": "",
    "breed": "Irish Wolfhound",
    "size": "Large",
    "human": "Samuel and Suzanne",
    "zip_code": "06040",
    "something_about_yourself": "Plays tough with big guys and gentle with little ones.",
    "at_the_park_?": "N",
    "park_id": 3
}
```

## Sample response
Returns the updated `dog` record.

**Status code**: <span class="status-2xx">200 OK</span>

```json
{
    "name": "Beckett Jr.",
    "photo": "../Photos/Beckett.jpeg",
    "breed": "Irish Wolfhound",
    "size": "Large",
    "human": "Samuel and Suzanne",
    "zip_code": "06040",
    "something_about_yourself": "Plays tough with big guys and gentle with little ones.",
    "at_the_park_?": "N",
    "park_id": 4,
    "id": 8
}
```
## Response status

| Status value   | Return status  | Description   |    
|---|---|---|
| 200  | OK (sucess)  | Request successful. The server has responded as required.  |  
| 404| Not found | Requested resource could not be found.|
| ECONNREFUSED | N/A | Service is offline. Start the service and try again.| 

## Other `dog` endpoints
* [Get all dogs](dog-get-all-dogs.md)
* [Find a dog by ID](dog-get-dog-by-id.md)
* [Add a dog](dog-add-dog.md)
* [Remove a dog](dog-delete-dog.md)