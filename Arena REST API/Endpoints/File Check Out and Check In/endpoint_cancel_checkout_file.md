# POST Cancel File Check Out
POST /files/checkoutstatuschanges

Cancels the check out process for a checked out File. Note that only the user who checked out the File or an Account administrator can cancel a File Check Out

Users must have a Full license to perform a File Check Out. Users must have access to an Edit File Policy rule.

Users must also have full access and have access to the file category.

## Request Header

| Name  | Value  | Description  |
|  --- |  --- |  --- | 
| arena_session_id  |   | unique ID for session obtained from login  |
| content-type  | application/json  |   |

## Sample Request Body


```
{  
  "checkedOut": false,
  "newEdition": null,
  "comment": "Cancelling File Check Out",
  " file": { 
       "guid": "K2M501MD03M2L47YKQ5B"
  }
}
```
## Response Codes

| Code  | Description  |
|  --- |  --- | 
| 201  | Success  |
| 400  | Failure  |

## Response Header

| Name  | Value  | Description  |
|  --- |  --- |  --- | 
| Content-Length  | number  | number of characters in response  |
| Content-Type  | determined by file type  | content type of file  |
| Date  | date  | today's date and time  |
| Server  | ArenaSolutions  |   |
| X-Arena-FileGuid  | GUID string  | GUID for new file - only when including content  |
| X-Arena-Next-Request-Limit-Reset   | date  | the scheduled time for resetting of the count  |
| X-Arena-Requests-Remaining   | number  | how many calls left  |

## Sample Responses
* Cancel the File Checkout:

```
{  
   "checkedOut": false,
   "comment": "Test Cancel Checkout",
   "file": {
       "author": {
           "fullName": "George C Lewis"
       },
       "category": {
           "guid": "3L507K5WJM5FYHW334R7"
       },
       "checkedOut": false,
       "corrected": false,
       "creationDateTime": "2011-06-02T19:30:28Z",
       "description": null,
       "edition": "1",
       "format": "pdf",
       "guid": "K2M501MD03M2L47YKQ5B",
       "hasMarkup": false,
       "lastModifiedDateTime": "2011-06-02T19:30:28Z",
       "latest": true,
       "location": null
       "locked": true,
       "mimeType": application/pdf
       "name": USB Cable A-A Datasheet.pdf",
       "number": "FILE-000867",
       "private": false,
       "size": 12326,
       "storageMethod": 0,
       "storageMethodName": "FILE",
       "title": "USB CABLE A-A Datasheet"
   }       
}
```
An error is returned if a user attempts to cancel a Check Out is already Checked In.

```
{  
   "status":400,
   "errors":[  
      {  
         "code":3132,
         "message":"\"This action cannot be completed. Cancelling a check out can only be performed on checked out Files.\""
      }
   ]
}
```
