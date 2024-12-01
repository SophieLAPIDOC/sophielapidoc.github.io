# [WOOF! API Tutorials](overview.md#tutorials)
# Find who goes to your favourite park
WOOF! connects people, dogs and parks. Before making a park your favourite hang out, check who is also a regular there. 
## Prerequisites 
 1. Start the json-server, as explained in [set up your environment](initial-setup.md).
 2. Open the [Postman desktop app](https://www.postman.com/downloads/).

 ## 1. Find park in your town
First let's find a list of parks in Madison CT.
### Request
Send the following request with the parameter `town`: `Madison`.
```
GET http://localhost:3000/park?town=Madison
```

### Response
The request returns an array of two parks. Make note of `id`: `3`.
```json
[
    {
        "park_name": "Salt Meadow Park Dog Park",
        "town": "Madison",
        "coordinates": "41.272346, -72.549974",
        "hours": "Salt Meadow Park is open year around from dawn to dusk",
        "amenities": "No water at the park",
        "comments": "The park just opened in May so water and shade are yet to be put in but overall great area.",
        "rating": "4",
        "id": 1
    },
    {
        "park_name": "Madison Dog Park",
        "town": "Madison",
        "coordinates": "41.272346, -72.549974",
        "hours": "until sunset",
        "amenities": "poop bags, hand sanitizer, water bowls",
        "comments": "Near the beach",
        "rating": "5",
        "id": 3
    }
]
```
 ## 2. Find dogs by park id
 Let's find who is a regular attendee at Madison Dog Park with `id`: `3` and check if they would make a suitable playmate.
 ### Request
```
GET http://localhost:3000/dog?park_id=3
```

### Response
The request returns the details of two dogs: Bella and Mr. Henry Sullivan.
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
        "name": "Mr. Henry Sullivan",
        "photo": "../Photos/HenrySullivan.jpeg",
        "breed": "Treeing Walker Coonhound",
        "size": "Large",
        "human": "Wendy & Chris",
        "zip_code": "06417",
        "something_about_yourself": "I love to play chase!",
        "at_the_park_?": "Y",
        "park_id": 3,
        "id": 2
    }
]
```
## Other tutorials
* [Find the best parks (user-rated) in your city](tuto-get-top-rated-park.md)
* [Update your dog's presence at the park](tuto-update-park-presence.md)
* [Find other small dogs in your favourite park.](tuto-get-park-small-dogs.md)


