# GET File Categories
/settings/files/categories

/settings/files/categories/&lt;GUID&gt;

This returns  Categories available for Files. Appending a GUID to the URL returns the category with that GUID. 

## Request Header

| Name  | Value  | Description  |
|  --- |  --- |  --- | 
| arena_session_id  |   | unique ID for session obtained from login  |
| content-type  | application/json  |   |

## Parameters

| Name  | Value  | Description  |
|  --- |  --- |  --- | 
| Path  | string  | This is used to filter out categories. The root of path for files is "file". If you want to get all the categories under the root category which start with A, you can send a request as api.arenasolutions.com/v1/settings/files/categories ?path=item\A, where "\" is the separator between parent category and child category.   |

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
Get all file categories

GET /settings/files/categories

```
{
   "count":46,
   "results":[
      {
         "activated":true,
         "assignable":true,
         "creationDateTime":"2011-01-05T00:26:30Z",
         "creator":{
            "email":"hwalker@everyroadgps.com",
            "fullName":"Heidi Walker",
            "guid":"4M6P8GPPM3K3M5O7QMJ9"
         },
         "description":"File is a system defined category",
         "guid":"I0K3MU330H0ATCVC0C11",
         "level":1,
         "name":"-uncategorized-",
         "path":"File",
         "requirements":[],
         "systemDefined":true
      },
      {
         "activated":true,
         "assignable":false,
         "creationDateTime":"2011-02-08T22:28:52Z",
         "creator":{
            "email":"hwalker@everyroadgps.com",
            "fullName":"Heidi Walker",
            "guid":"4M6P8GPPM3K3M5O7QMJ9"
         },
         "description":null,
         "guid":"9RBUDLUUR8R1K3M3R3T6",
         "level":2,
         "name":"Internal File",
         "path":"File\\Internal File",
         "requirements":[],
         "systemDefined":false
      },
      {
         "activated":true,
         "assignable":true,
         "creationDateTime":"2011-02-08T22:29:31Z",
         "creator":{
            "email":"hwalker@everyroadgps.com",
            "fullName":"Heidi Walker",
            "guid":"4M6P8GPPM3K3M5O7QMJ9"
         },
         "description":null,
         "guid":"SAUDW4DDARAK3M5MAMCT",
         "level":3,
         "name":"Artwork",
         "path":"File\\Internal File\\Artwork",
         "requirements":[],
         "systemDefined":false
      },
      {
         "activated":true,
         "assignable":true,
         "creationDateTime":"2011-02-08T22:29:55Z",
         "creator":{
            "email":"hwalker@everyroadgps.com",
            "fullName":"Heidi Walker",
            "guid":"4M6P8GPPM3K3M5O7QMJ9"
         },
         "description":null,
         "guid":"ASCVEMVVS9S2L4N4S4UK",
         "level":3,
         "name":"Assembly Specification",
         "path":"File\\Internal File\\Assembly Specification",
         "requirements":[],
         "systemDefined":false
      },
      ...
   ]
}
```
Get all file categories that begin with C

GET settings/files/categories?path=item\C

```
{  
   "count":1,
   "results":[  
      {  
         "activated":true,
         "assignable":null,
         "creationDateTime":"2008-03-05T13:55:30Z",
         "creator":{
            "email":"hwalker@everyroadgps.com",
            "fullName":"Heidi Walker",
            "guid":"4M6P8GPPM3K3M5O7QMJ9"
         },
         "description":null,
         "guid":"8F8ALDIEN3QDGOWI7V7G",
         "level":2,
         "name":"Confidential File",
         "objectType":"FILE",
         "path":"File\Confidential File",
         "requirements":[],
         "systemDefined":false
      }
   ]
}
```
Get a single file category

GET settings/files/categories/9RBUZPQQZ6PZI1DL92A2

```
{  
   "activated":true,
   "assignable":null,
   "creationDateTime":"2008-03-05T13:56:22Z",
   "creator":{
      "email":"hwalker@everyroadgps.com",
      "fullName":"Heidi Walker",
      "guid":"4M6P8GPPM3K3M5O7QMJ9"
   },
   "description":null,
   "guid":"9RBUZPQQZ6PZI1DL92A2",
   "level":3,
   "name":"CAD Data",
   "objectType":"FILE",
   "path":"File\Internal File\CAD Data",
   "requirements":[],
   "systemDefined":false
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
