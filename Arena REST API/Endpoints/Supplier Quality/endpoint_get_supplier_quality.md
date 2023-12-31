# GET Supplier Quality Processes
GET /suppliers/&lt;GUID&gt;/quality

GET /suppliers/&lt;GUID&gt;/quality/&lt;GUID&gt;

Returns a collection of  Quality Process objects for a supplier with a given GUID \(all Quality Processes in which the Supplier is an affected object\). 

If the endpoint is apprended with a valid GUID, it returns a specific Quality Process and the step information where the specified Supplier has been added as an affected object.

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
Get quality processes for a supplier

GET /suppliers/&lt;GUID&gt;/quality

```
{  
   "count":1,
   "results":[  
      {  
         "guid":"3L5OTIZD0J0GZI1KTNOH",
         "notes":"Trilby fabricates the bezels. Jensen Chang is our contact there",
         "qualityProcess":{  
            "guid":"K2M5AZC4QSB7Q9SBK8IN",
            "name":"Everyroad bezels melted/burned",
            "number":"SCAR-000003",
            "step":{  
               "guid":"ASCV0P2UGI1XGZI1AYAF",
               "name":"Root Cause Analysis"
            },
            "type":"Compliance"
         }
      }
   ]
}
```
Gets a specific Quality Process \(and specific step information\) where the specified Supplier has been added as an affected object.

GET /suppliers/&lt;GUID&gt;/quality/&lt;GUID&gt;

```
{
    "guid": "YG0J2F0REHZATCVDR9KV",
    "notes": null,
    "qualityProcess": {
        "guid": "M4O7Q3OF25OK3M5OHUQ2",
        "name": "Manufacturing flaws on 175-00001 boards",
        "number": "CAR-000007",
        "step": {
            "guid": "N5P8R4PG36PL4N6PIVRR",
            "name": "Problem Description"
        },
        "type": null
    }
}
```
Request with bad GUID

```
{  
    "status":400,
    "errors":[  
        {  
            "code":3011,
            "message":"The guid \"XFWQ0GZGZDJ015J12\" is not valid."
        }
    ]
}
```
