<link rel="stylesheet" type="text/css" href="./assets/css/sophie-custom.css" />

#### Back to [Home](index.md) | [Get started](index.md#get-started) | [Tutorials](index.md#tutorials) | [References](index.md#reference)

# Find the best parks (user-rated) in your town
When nothing but the best park with great amenities will do, you can trust the community of WOOF! users to tell it like it is. 
## Prerequisites 
 1. Start the json-server, as explained in [set up your environment](initial-setup.md).
 2. Open the [Postman desktop app](https://www.postman.com/downloads/).

## 1. Find a park by rating in your town
Send the following request to retrieve a list of parks in Madison CT with the rating of 5 stars. This request combines two query parameters: `town`: `Madison` and `rating`: `5`.

### Request

<span class="button" id="get">GET</span>`http://localhost:3000/park?town=Madison&rating=5`


### Response
```json
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
```
## 2. Find a park by rating using a comparison operator
If you want to widen your search, you can use a comparison operator. For example, to retrieve parks with a rating greater or equal to 4, send the following request:

### Request


<span class="button" id="get">GET</span>http://localhost:3000/park?rating_gte=4`
### Response
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
## Other tutorials
* [Update your dog's presence at the park](tuto-update-park-presence.md)
* [Find other small dogs in your favourite park.](tuto-get-park-small-dogs.md)
* [Find who goes to your favourite park](tuto-get-dogs-by-park.md)