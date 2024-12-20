<link rel="stylesheet" type="text/css" href="./assets/css/sophie-custom.css" />

#### Back to [Home](index.md) | [Get started](index.md#get-started) | [Tutorials](index.md#tutorials) | [References](index.md#reference)

## Update the details a of park

Change any of the properties for an existing `park` entry.

### Request

<span class="button" id="put">PUT</span>`/park/{id}`

### Request Headers
**Content-Type**: `application/json`

### Request body
When using the **PUT** method include  all the `park` resource properties as listed in [park resource](park-ref.md) and change the values, as required.



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

## Sample request
```
PUT {base_url}/park/6
```

## Sample body

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
Returns the updated `dog` record.

**Status code:** <span class="">200 OK</span>

```json
{
    "park_name": "Indian Ledge Park",
    "town": "Trumbull",
    "coordinates": "41.242874, -73.200669",
    "hours": "9am - 7pm, Veterans Day might affect these hours",
    "amenities": "off-leash area, poo bags, separate areas for small and large dogs",
    "comments": "All dogs must be neutered or spayed to access the park. A Trumbull resident sticker is required for parking.",
    "rating": "4",
    "id": 6
}
```

## Response status

| Status value   | Return status  | Description   |   
|---|---|---|
| 200  | OK (success)  | Request successful. The server has responded as required.  |  
| 404 | Not found | Requested resource could not be found. |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

## Other `park` endpoints
* [Get all parks](park-get-all-parks.md)
* [Find a park by ID](park-get-park-by-id)
* [Add a park](park-add-new-park.md)
* [Remove a park](park-delete-park.md)