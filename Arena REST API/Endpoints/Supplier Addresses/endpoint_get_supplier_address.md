# GET Supplier Address
/suppliers/&lt;GUID&gt;/addresses/&lt;GUID&gt;

Returns a specific address with a given GUID  of a Supplier object with a given GUID.

## Request Header

| Name  | Value  | Description  |
|  --- |  --- |  --- | 
| arena_session_id  |   | unique ID for session obtained from login  |
| content-type  | application/json  |   |

## Response Codes

| Code  | Description  |
|  --- |  --- | 
| 200  | Success  |
| 400  | Failure  |

## Response Header

| Name  | Value  | Description  |
|  --- |  --- |  --- | 
| Content-Length  | number  | number of characters in response  |
| Content-Type  | application/json  | content type of response  |
| Date  | date  | today's date and time  |
| Server  | ArenaSolutions  |   |
| X-Arena-Next-Request-Limit-Reset   | date  | the scheduled time for resetting of the count  |
| X-Arena-Requests-Remaining   | number  | how many calls left  |

## Sample Response Body
Get the address with a given GUID of a  supplier with a given GUID

/suppliers/&lt;GUID&gt;/addresses/&lt;GUID&gt;

```
{
    "address": {
        "address1": "459 Embarcadero",
        "address2": null,
        "city": "San Francisco",
        "Country/Region": "United States",
        "guid": "5N7Q9M7YLOZ3M5GLXZ0K",
        "label": "SF Office",
        "postalCode": "94003",
        "province": null,
        "state": "CALIFORNIA"
    },
    "primary": false
} 
```
Request with bad GUID

```
{
  "status": 400,
  "errors": [
    {
      "code": 3011,
      "message": "The guid \"0I2L4CLLIZISBUDUIUI4\" is not valid."
    }
  ]
}
```
