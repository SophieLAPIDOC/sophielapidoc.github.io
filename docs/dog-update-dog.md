###### Back to [Home](index.md) | [Get started](index.md#get-started) | [Tutorials](index.md#tutorials) | [References](index.md#reference)

## Update the details of a dog
Change any of the proprties for an existing `dog` entry.

### Request
```
PUT /dog/{id}
```
### Request Headers
* `Content-Type`: `application/json`

### Request body
When using the **POST** method include  all the `dog` respurce properties as listed in [dog resource](dog-ref.md) and change the values, as required.

|Property name   |Type   |Description   |   
|---|---|---|
| `name`  |string   | The name of the dog.  |
| `photo`  |string   | File path to the dog's photo.  |   
| `breed`  |string   | The record ID of the user.  |   
| `size`  |string   | The size category of the dog: Small, Medium, Large.  |   
| `human`  |string  | The name of the owner or person in charge. Multiple values allowed if comma separated. Can be full name or first name only.  | 
| `zip_code`  |string   | Zip Code where dog and humans reside.  |   
| `something_about_yourself`  |string   | A short description of the dog's character personality.  |   
| `at_the_park_?`  |string   | Whether the dog is at the park right now: True/False. Default value is False. |   
| `park_id`  |integer  | The record ID of the park.  |   
| `id`  |integer   | The record ID of the dog.  | 

### Sample request
```
{base_url}/dog/8
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

Status code: `200 OK`

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
|Status value   |Return status  |Description   |   
|---|---|---|
| 200  |OK (sucess)  | Request successful. The server has responded as required.  |  
|404|Not found|Requested resource could not be found.|
|ECONNREFUSED|N/A|Service is offline. Start the service and try again.|
