# POST Item File Create
/items/&lt;GUID&gt;/files

Creates a new File Association object and associates it with an item with a given GUID.

If you wish to create a File record with no uploaded content, construct a JSON request with a storageMethodName of PLACE_HOLDER, FTP, or WEB. When the storageMethodName is FTP or WEB, the location attribute should be the web or ftp address where the file resides.<br>

If you wish to create a File record and upload file content to the Arena servers, construct a request that is content type multipart/form-data and has a storageMethodName  of FILE. <br>

For File editions with storageMethodName FILE, the location attribute should be null.

NOTES:

* Only Item files are supported for this endpoint. Files associated with sourced Supplier Items use /supplieritems/&lt;GUID&gt;/files.

## Request Header

| Name  | Value  | Description  |
|  --- |  --- |  --- | 
| arena_session_id  |   | unique ID for session obtained from login  |
| content-type  | multipart/form-data  |   |

## Sample Request Body


* Creating a File and uploading content to Arena servers (text format):

* Text attributes:

```
file.author.fullName: Heidi Walker
file.category.guid: WEYHMCDDMTCM5O08WPWY
file.description: Assembly Instructions
file.edition: 1
file.format: txt
file.private:false
file.storageMethodName: FILE
file.title: Assembly Instructions for 324-0263
latestEditionAssociation:true
primary:true
```
* File attribute:

```
content: [physical file]
```
* Creating a File with no uploaded content (Web or FTP location/Placeholder):

```
{
    "file": {
        "location": "www.everyroadgps.com/files/300-traces.pdf",
        "category": {
            "guid ": "ZH0J2L4EXGS0NF91"
        },
        "storageMethodName": "WEB",
        "title": "traces for Everyroad 300 board",
        "edition": "1",
        "author": {
            "fullName": "Heidi Walker"
        },
        "format": "pdf"
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
| X-Arena-ItemFileAssociation-Guid  | GUID string  | GUID for new file association - only when including content  |
| X-Arena-Next-Request-Limit-Reset   | date  | the scheduled time for resetting of the count  |
| X-Arena-Requests-Remaining   | number  | how many calls left  |

## Sample Responses
* When creating a File object with uploaded content:

* No JSON Response. Please refer to the response header for file information.

* When creating a file with no uploaded content:

```
{  
   "file":{  
      "author":{  
         "fullName":"Heidi Walker"
      },
      "category":{  
         "guid":"ZH0J2L4EXGS0NF91"
      },
      "creationDateTime":"2014-02-24T22:41:19Z",
      "description":null,
      "edition":"1",
      "format":"url",
      "guid":"GYI16WW251K0J2TITQ1O",
      "hasMarkup":false,
      "lastModifiedDateTime":"2014-02-24T22:41:19Z",
      "latest":true,
      "location":"http://www.everyroadgps.com",
      "locked":false,
      "mimeType":null,
      "name":"300-traces.pdf",
      "number":"FILE-000005",
      "private":false,
      "size":null,
      "storageMethod":3,
      "storageMethodName":"WEB",
      "title":"traces for everyroad 300 board"
   },
   "guid":"ASBUDWFRATPYJAGV",
   "latestEditionAssociation":true,
   "primary":false
}
```
An error is returned if:

* The GUID is not valid.

```
{
  "status": 400,
  "errors": [
    {
      "code": 3011,
      "message": "The guid \"XFWQ0GZGZDJ015J12\" is not valid."
    }
  ]
}
```
* a required metadata attribute is missing.

```
{
  "status": 400,
  "errors": [
    {
      "code": 3001,
      "message": "The attribute \"file.edition\" is required."
    }
  ]
}
```
