#### Back to [Home](index.md) | [Get started](index.md#get-started) | [Tutorials](index.md#tutorials) | [References](index.md#reference)

# `dog` resource

Base endpoint:

```
{base_url}/dog
```
**Note:** The `{base_url}` will vary depending on your developemnt environement. When running the WOOF!API locally, the `{base_url}` is `http://localhost:3000`.

`dog` contains details about the dog(s) registered in the WOOF! API.
## Resource properties
Sample `dog` resource

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

## Endpoints
* [Get all dogs](dog-get.all-dogs.md)
* [Find a dog by ID](dog-get-dog-by-id.md)
* [Add a dog](dog-add-dog.md)
* [Update the details of a dog](dog-update-dog.md)
* [Remove a dog](dog-delete-dog.md)
  
## Related topics
* [park](park-ref.md)
* [tutorials](index.md#tutorials)

