# [WOOF! API Tutorials](index.md#tutorials)
# Find other small dogs in your favourite park
Whether your dog is large and boisterous, or small and timid, you might find it more comfortable to go to a park frequented by dogs the same size as yours.
## Prerequisites 
 1. Start the json-server, as explained in [set up your environment](initial-setup.md).
 2. Open the [Postman desktop app](https://www.postman.com/downloads/).
## Find small dogs by park id
In the previous tutorial [Find who goes to your favourite park](tuto-get-dogs-by-park.md) we have learned that Madison Dog Park has `id`: `3`.
### Request
To find out if other small dogs attending Madison Dog Park send the following request:
```
GET http://localhost:3000/dog?park_id=3&size=Small
```
To find out if any small dog is currently at Madison Dog Park CT, include an additional query parameter in your request: `at_the_park_?` and filter on `Y`.
```
GET http://localhost:3000/dog?park_id=3&size=Small&at_the_park_?=Y
```

### Response
Little Bella is a regular attendee at Madison Dog Park and she is there right now. Time to grab the leash and head out.
```json
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
    }
```
## Other tutorials
* [Find the best parks (user-rated) in your city](tuto-get-top-rated-park.md)
* [Update your dog's presence at the park](tuto-update-park-presence.md)
* [Find who goes to your favourite park](tuto-get-dogs-by-park.md)