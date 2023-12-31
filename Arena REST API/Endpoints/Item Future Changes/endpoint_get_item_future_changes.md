# GET Item Future Changes
/items/&lt;GUID&gt;/futurechanges

/items/&lt;GUID&gt;/futurechanges/&lt;GUID&gt;

Returns the future changes of an Item object. These are Changes that may affect the Item in the future. Appending a GUID to the URL returns the future change with that GUID.

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
Get all the future changes associated with an Item of a given GUID.

GET /items/&lt;GUID&gt;/futurechanges

```
{
    "count": 4,
    "results": [
        {
            "change": {
                "creationDateTime": "2021-09-07T19:02:13Z",
                "effectivityType": "PERMANENT_ON_APPROVAL",
                "guid": "I0K3MZKBY1KN6O446611",
                "number": "ECO-000024",
                "title": "BOM Mods"
            },
            "guid": "ZH1K3G1SFI04N6T4J21G"
        },
        {
            "change": {
                "creationDateTime": "2021-09-07T19:04:03Z",
                "effectivityType": "PERMANENT_ON_APPROVAL",
                "guid": "K2M5O1MD03MP8Q66883X",
                "number": "ECO-000026",
                "title": "Files View"
            },
            "guid": "1J3M5I3UHK26P8V6L43J"
        },
        {
            "change": {
                "creationDateTime": "2021-09-07T19:01:18Z",
                "effectivityType": "PERMANENT_ON_APPROVAL",
                "guid": "HZJ2LYJAX0JM5N33550D",
                "number": "ECO-000023",
                "title": "PCB Specs View"
            },
            "guid": "YG0J2F0REHZ3M5S3I10S"
        },
        {
            "change": {
                "creationDateTime": "2021-09-07T19:03:00Z",
                "effectivityType": "PERMANENT_ON_APPROVAL",
                "guid": "J1L4N0LCZ2LO7P55772G",
                "number": "ECO-000025",
                "title": "Files View"
            },
            "guid": "0I2L4H2TGJ15O7U5K32Z"
        }
    ]
}
```
Get a single future change with a specific GUID associated with an Item with a specific GUID.

GET /items/&lt;GUID&gt;/futurechanges/&lt;GUID&gt;

```
{
            "change": {
                "creationDateTime": "2021-09-07T19:02:13Z",
                "effectivityType": "PERMANENT_ON_APPROVAL",
                "guid": "I0K3MZKBY1KN6O446611",
                "number": "ECO-000024",
                "title": "BOM Mods"
            },
            "guid": "ZH1K3G1SFI04N6T4J21G"
}
```
request with bad GUID

```
{  
   "status":400,
   "errors":[  
      {  
         "code":3011,
         "message":"The guid \"L3N6PX663K3K3HOBOOT0 \" is not valid."
      }
   ]
}
```
