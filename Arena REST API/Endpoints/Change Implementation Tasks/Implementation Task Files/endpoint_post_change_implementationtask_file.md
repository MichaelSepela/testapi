# POST Change Implementation Task File
/changes/&lt;GUID&gt;/implementationtasks/&lt;GUID&gt;/files

Adds a specific, already existing in the workspace, File to a specific implementation task. Implementation Task Management must be enabled to execute this endpoint. Not supported for Canceled or Completed Changes.

## Request Header

| Name  | Value  | Description  |
|  --- |  --- |  --- | 
| arena_session_id  |   | unique ID for session obtained from login  |
| content-type  | application/json  |   |

## Sample Request Body
Adds an existing file to an existing implementation task.

```
{
    "file": {
        "guid": "GYI1FCGITAT9SB0IJX9M"
    }
}
```
## Response Codes

| Code  | Description  |
|  --- |  --- | 
| 200  | Success  |
| 400  | Failure  |

## Response Header

| Name  | Value  | Description  |
|  --- |  --- |  --- | 
| Content-Type  | application/json  | content type of response  |
| Date  | date  | today's date and time  |
| Server  | ArenaSolutions  |   |
| X-Arena-Next-Request-Limit-Reset   | date  | the scheduled time for resetting of the count  |
| X-Arena-Requests-Remaining   | number  | how many calls left  |

## Sample Response Body
Adds a specific change implementation task file.

POST /changes/&lt;GUID&gt;/implementationtasks/&lt;GUID&gt;

```
{
    "guid": "I0K3HEIKVCT8RATCV2DU",
    "file": {
       "guid": "GYI1FCGITAT9SB0IJX9M",
       "number": "FILE-046012",
       "edition": "1",
       "name": "implementation plan.pdf",
       "storageMethodName": "FILE",
       "title": "Implementation Plan"
}
```
Request with invalid GUID

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
