# GET Training Plan Records
/trainingplans/&lt;GUID&gt;/records

Returns all the  training records for a specific Training Plan. Using the browser-based application as a point of comparison, this endpoint returns the training records data within the Records view of a specific Training Plan.

## Request Header

| Name  | Value  | Description  |
|  --- |  --- |  --- | 
| arena_session_id  |   | unique ID for session obtained from login  |
| content-type  | application/json  |   |

## Parameters

| Name  | Value  | Description  |
|  --- |  --- |  --- | 
| offset  | integer  | Specifies the position in the list of all changes where results should begin. All changes before the offset in the search results are ignored. The default value is 0.  |
| limit  | integer  | Specifies the number of results that should be returned. By default the maximum number of objects is 20. Can return up 400.  |

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
Get the Training Plan records within the Records view  of  a Training Plan.

GET /trainingplans/&lt;GUID&gt;/records

```
{
    "count": 11,
    "results": [
        {
            "dueDate": "2016-09-18T06:59:59Z",
            "guid": "ZH1K3G1SFIYGZI1K2C5X",
            "item": {
                "guid": "L3N6P2NE14NVETHB8TF2",
                "name": "SOP, Building Evacuation and Safety",
                "number": "020-00004",
                "revisionNumber": "A",
                "revisionStatus": "EFFECTIVE",
                "url": {
                    "api": "https://api.arenasolutions.com/v1/items/L3N6P2NE14NVETHB8TF2",
                    "app": "https://app.bom.com/L3N6P2NE14NVETHB8TF2"
                }
            },
            "signedDateTime": "2016-09-07T23:09:49Z",
            "user": {
                "email": "jdeckard@everyroadgps.com",
                "fullName": "James Deckard",
                "guid": "YG0J2F0REHYH0J2LUKR9"
            }
        },
        {
            "dueDate": "2016-09-18T06:59:59Z",
            "guid": "3L5O7K5WJM2K3M5O6G9M",
            "item": {
                "guid": "7P9SBO90NQ9H0F3XUEJR",
                "name": "SOP, Production and Process Management",
                "number": "020-00008",
                "revisionNumber": "A",
                "revisionStatus": "EFFECTIVE",
                "url": {
                    "api": "https://api.arenasolutions.com/v1/items/7P9SBO90NQ9H0F3XUEJR",
                    "app": "https://app.bom.com/7P9SBO90NQ9H0F3XUEJR"
                }
            },
            "signedDateTime": "2016-09-07T23:10:19Z",
            "user": {
                "email": "jdeckard@everyroadgps.com",
                "fullName": "James Deckard",
                "guid": "YG0J2F0REHYH0J2LUKR9"
            }
        },
        {
            "dueDate": "2016-09-18T06:59:59Z",
            "guid": "YG0J2F0REHXFYH0J1B4F",
            "item": {
                "guid": "R9TCV8TK7AT1KZNHEY9O",
                "name": "SOP, Inspection and Test",
                "number": "020-00005",
                "revisionNumber": "A",
                "revisionStatus": "EFFECTIVE",
                "url": {
                    "api": "https://api.arenasolutions.com/v1/items/R9TCV8TK7AT1KZNHEY9O",
                    "app": "https://app.bom.com/R9TCV8TK7AT1KZNHEY9O"
                }
            },
            "signedDateTime": "2016-09-07T23:09:58Z",
            "user": {
                "email": "jdeckard@everyroadgps.com",
                "fullName": "James Deckard",
                "guid": "YG0J2F0REHYH0J2LUKR9"
            }
        },
        {
            "dueDate": "2016-09-18T06:59:59Z",
            "guid": "J1L4N0LCZ2I0J2L4MWNG",
            "item": {
                "guid": "L3N6P2NE14NVETHB8TF2",
                "name": "SOP, Building Evacuation and Safety",
                "number": "020-00004",
                "revisionNumber": "A",
                "revisionStatus": "EFFECTIVE",
                "url": {
                    "api": "https://api.arenasolutions.com/v1/items/L3N6P2NE14NVETHB8TF2",
                    "app": "https://app.bom.com/L3N6P2NE14NVETHB8TF2"
                }
            },
            "signedDateTime": "2017-03-17T22:55:40Z",
            "user": {
                "email": "hwalker@everyroadgps.com",
                "fullName": "Heidi Walker",
                "guid": "WEYH0DYPCFWFYH0JSIPD"
            }
        },
        ...
        }
    ]
}
```
