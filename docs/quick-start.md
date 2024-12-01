# Get started with the WOOF! API
Using the WOOF! API is a walk in the park. 
In this quick start topic, we'll show you how to find a park in your town, then add your dog's profile to the service. 
We'll also show you add a new park to WOOF!

This should take about 15 - 20 minutes to complete. Just a short stroll.

If you want to wander further afield, read our advanced [Tutorials](index.md#tutorials).

## Prerequisites 
 1. Start the json-server, as explained in [set up your environment](initial-setup.md).
 2. Open the [Postman desktop app](https://www.postman.com/downloads/).
    

## Find a park in your town
To locate a dog park in a specific town - in this example, let's use Madison CT - send this request:
```
POST http://localhost:3000/park?town=Madison
```
If  a park record is found for Madison CT, WOOF! returns the following details:
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

## Add your dog to WOOF!
To connect with other park users or let them know when they are present in a specific park, owners must register their dog(s) with WOOF!

This request creates a new dog record in the service.
```
POST http://localhost:3000/dog/
```
To add a profile for Tiana, the Husky Cross, send this information in the body of the request:
```json
{
    "name": "Tiana",
    "photo": "",
    "breed": "Husky Cross",
    "size": "Large",
    "human": "Lagertha",
    "zip_code": "06443",
    "something_about_yourself": "I love playing with kids, but I run fast. catch me if you can",
    "at_the_park_?": "N",
    "park_id": 3
}
```
Make sure you select a park. In our case, we will use the park we've just found in Madison CT.

**Note:** The selected park can be updated later. By default, the park presence is set to `N` (No).  


The service returns the following response, with `id`: `9` for Tiana:

```json
{
    "name": "Tiana",
    "photo": "",
    "breed": "Husky Cross",
    "size": "Large",
    "human": "Lagertha",
    "zip_code": "06443",
    "something_about_yourself": "I love playing with kids, but I run fast. catch me if you can",
    "at_the_park_?": "N",
    "park_id": 3,
    "id":9
}
```

## Add a park to WOOF!

Town councils and Park services sometimes open new dog parks. To keep WOOF! up-to-date, add new parks as they open up to the public. 

To add a new par to WOOF!, send this request:

```
POST http://localhost:3000/park

```
Send as much information about the park as possible in the body of the request. 

```json
{
  "park_name": "Salt Meadow Park Dog Park",
  "town": "Madison",
  "coordinates": "41.265421, -72.592163",
  "hours": "open year around from dawn to dusk",
  "amenities": "off-leash area, poo bags, separate areas for small and large dogs",
  "comments": "A brand new park, with limited amenities for now. Bring your own water, dog bowl and poop bags. Can get hot. ",
  "rating": ""
}
```
## Related topics
To discover other features of the WOOF! API, refer to the [Tutorials](index.md#tutorials) section.
