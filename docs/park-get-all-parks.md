<link rel="stylesheet" type="text/css" href="./assets/css/sophie-custom.css" />

#### Back to [Home](index.md) | [Get started](index.md#get-started) | [Tutorials](index.md#tutorials) | [References](index.md#reference)

## Get all parks
Get the full list of the parks registered in the WOOF! API identified by their unique ID.

### Request

<span class="button" id="delete">GET</span>`/park`


## (Optional) Query Parameters

| Parameter name   |Type   |Description   |  
|---|---|---|
| `town`  |string   | Town where the park is located.  |   
| `coordinates`  |number  | Geographic coordinates of the park, as decimal degrees. |   
| `rating`  |number   | Dog owner rating for the park, on a 1-5 scale, where 1 is poor satisfaction and 5 is very satisfied.  |    

## Sample request

```
GET {base_url}/park?town=Clinton
```



## Sample response
**Status code:** <span class="status-2xx">200 OK</span>

```json
 {
        "park_name": "Bailey's Dog Park",
        "town": "Clinton",
        "coordinates": "41.305547, -72.527168",
        "hours": "5 AM - 5 PM",
        "amenities": "none",
        "comments": "Bring your own everything",
        "rating": "2",
        "id": 5
    }
```
## Response status

|Status value   |Return status  |Description   |  
|---|---|---|
| 200  | OK (sucsess)  | Request successful. The server has responded as required.  |  
| 201  | Created  | Request successful. The server created a new resource.  |  
| 404|Not found| Requested resource could not be found.|
| ECONNREFUSED| N/A| Service is offline. Start the service and try again.| 

## Other `park` endpoints
* [Find a park by ID](park-get-park-by-id)
* [Add a park](park-add-new-park.md)
* [Update the details of park](park-update-park.md)
* [Remove a park](park-delete-park.md)