#### Back to [Home](index.md) | [Get started](index.md#get-started) | [Tutorials](index.md#tutorials) | [References](index.md#reference)

## Update the details a of park

Change any of the proprties for an existing `park` entry.

### Request
```
PUT /park/{id}
```
### Request Headers
* `Content-Type`: `application/json`

### Request body
When using the **POST** method include  all the `park` respurce properties as listed in [park resource](park-ref.md) and change the values, as required.





|Property name   |Type    |  Description | 
|---|---|---|
| `park_name`  |string   | The name of the park.  |
| `town`  |string   | Town where the park is located.  |   
| `coordinates`  |number  | Geographic coordinates of the park, as decimal degrees. |   
| `hours`  |string   | Opening hours of the park.  |   
| `amenities`  |string  | Brief enumeraton of amenities available to dogs.  |  
| `comments`  |string   | Any additional information about the park.  |   
| `rating`  |integer  | Dog owner rating for the pak, on a 1-5 scale, where 1 is poor satisfaction and 5 is very satisfied.  |   
| `id`  |integer  | The record ID of the pak.  | 

## Sample request
```
{base_url}/park/6
```

## Sample body

```json, 
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

Status code: `200 OK`

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
| 200  | OK (sucess)  | Request successful. The server has responded as required.  |  
| 404 | Not found | Requested resource could not be found. |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |