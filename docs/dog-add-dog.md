<link rel="stylesheet" type="text/css" href="./assets/css/sophie-custom.css" />

#### Back to [Home](index.md) | [Get started](index.md#get-started) | [Tutorials](index.md#tutorials) | [References](index.md#reference)

## Add a dog
Create a new catalogue entry for a dog.

### Request

<span class="button" id="post">POST</span>`{base_url}/dog`


### Request Headers
**Content-Type**: `application/json`


### Request body
Include  the `dog` resource properties as listed in [dog resource](dog-ref.md).


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

### Sample body

```json
{
    "name": "Beckett",
    "photo": "",
    "breed": "Irish Wolfhound",
    "size": "Large",
    "human": "Samuel",
    "zip_code": "06040",
    "something_about_yourself": "Plays tough with big guys and gentle with little ones.",
    "at_the_park_?": "N",
    "park_id": 3
}
```
### Sample response
**Status code:** <span class="status-2xx">201 Created</span>
```json
{
    "name": "Beckett",
    "photo": "",
    "breed": "Irish Wolfhound",
    "size": "Large",
    "human": "Samuel and Suzanne",
    "zip_code": "06040",
    "something_about_yourself": "Plays tough with big guys and gentle with little ones.",
    "at_the_park_?": "N",
    "park_id": 3,
    "id": 8
}
```
## Response status

|Status value   | Return status  | Description   |   
|---|---|---|
| 201 | Created  | Request successful. The server has created a new resource.  | 
|ECONNREFUSED | N/A | Service is offline. Start the service and try again.|

## Other `dog` endpoints
* [Get all dogs](dog-get-all-dogs.md)
* [Find a dog by ID](dog-get-dog-by-id.md)
* [Update the details of dog](dog-update-dog.md)
* [Remove a dog](dog-delete-dog.md)