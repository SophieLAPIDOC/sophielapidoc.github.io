<link rel="stylesheet" type="text/css" href="./assets/css/sophie-custom.css" />

#### Back to [Home](index.md) | [Get started](index.md#get-started) | [Tutorials](index.md#tutorials) | [References](index.md#reference)

## Add a park 
Create a new catalogue entry for a park

### Request

<span class="button" id="post">POST</span>`{base_url}/park`


### Request body
Include  the `park` resource properties as listed in [park resource](park-ref.md).

### Parameters    

|Property name   |Type    |  Description | 
|---|---|---|
| `park_name`  |string   | (Mandatory) The name of the park.  |
| `town`  |string   | (Mandatory) Town where the park is located.  |   
| `coordinates`  |number  | (Optional) Geographic coordinates of the park, as decimal degrees. |    
| `hours`  |string   | (Mandatory) Opening hours of the park.  |  
| `amenities`  |string  | (Mandatory) Brief enumeration of amenities available to dogs.  | 
| `comments`  |string   | Any additional information about the park.  |    
| `rating`  |number  | (Optional) Dog owner rating for the park, on a 1-5 scale, where 1 is poor satisfaction and 5 is very satisfied.  |   
| `id`  |number  | The record ID of the park.  | 

### Sample body

```json
{
  "park_name": "Indian Ledge Park",
  "town": "Trumbull",
  "coordinates": "41.242874, -73.200669",
  "hours": "9am - 7pm",
  "amenities": "off-leash area, poo bags, separate areas for small and large dogs",
  "comments": "All dogs must be neutered or spayed to access the park. A Trumbull resident sticker is required for parking.",
  "rating": "4"
}
```

## Sample response
Status code: `201 Created`

```json
{
    "park_name": "Indian Ledge Park",
    "town": "Trumbull",
    "coordinates": "41.242874, -73.200669",
    "hours": "9am - 7pm",
    "amenities": "off-leash area, poo bags, separate areas for small and large dogs",
    "comments": "All dogs must be neutered or spayed to access the park. A Trumbull resident sticker is required for parking.",
    "rating": "4",
    "id": 6
}
```
## Response status

| Status value   | Return status  | Description   |    
|---|---|---|
| 201  | Created  | Request successful. The server created a new resource.  |  
| ECONNREFUSED | N/A | Service is offline. Start the service and try again.| 

## Other `park` endpoints
* [Get all parks](park-get-all-parks.md)
* [Find a park by ID](park-get-park-by-id)
* [Update the details of park](park-update-park.md)
* [Remove a park](park-delete-park.md)