# GET File Attributes
/settings/files/attributes

Returns  Attributes available for Files. 

## Request Header

| Name  | Value  | Description  |
|  --- |  --- |  --- | 
| arena_session_id  |   | unique ID for session obtained from login  |
| content-type  | application/json  |   |

## Parameters

| Name  | Value  | Description  |
|  --- |  --- |  --- | 
| includePossibleValues  | true or false  | If this is set to true, it returns all the possible values for Drop Down List attributes. The default value is false.  |
| creatableOnly  | true or false  | If this is set to true, it returns only creatable attributes, which are settable during creation of a file.If this is set to false, it returns only non-creatable attributes.<br>   |
| editableOnly  | true or false  | If this is set to true, it returns only editable attributes, which are settable during update of a file. The default value is false.  |
| searchableOnly  | true or false  | If this is set to true, it returns only searchable attributes, which are searchable when getting files.  |

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
Get all file attributes with possible values included

GET /settings/files/attributes?includePossibleValues=true

```
{  
   "count":38,
   "results":[  
      {  
         "allowsExplicitNullValue":false,
         "apiName":"author",
         "creatable":true,
         "editable":true,
         "fieldType":"OBJECT",
         "inViews":[  
            "ITEM_FILES",
            "FILE_SUMMARY",
            "SI_FILES"
         ],
         "required":true,
         "searchable":true
      },
      {  
         "allowsExplicitNullValue":false,
         "apiName":"category",
         "creatable":true,
         "editable":true,
         "fieldType":"OBJECT",
         "inViews":[  
            "ITEM_FILES",
            "FILE_SUMMARY",
            "SI_FILES"
         ],
         "required":true,
         "searchable":true
      },
      {  
         "allowsExplicitNullValue":false,
         "apiName":"creationDateTime",
         "creatable":false,
         "editable":false,
         "fieldType":"DATETIME",
         "inViews":[  
            "ITEM_FILES",
            "FILE_SUMMARY",
            "SI_FILES"
         ],
         "searchable":true
      },
      {  
         "allowsExplicitNullValue":false,
         "apiName":"description",
         "creatable":true,
         "editable":true,
         "fieldType":"SINGLE_LINE_TEXT",
         "inViews":[  
            "ITEM_FILES",
            "FILE_SUMMARY",
            "SI_FILES"
         ],
         "maxLength":4000,
         "required":false,
         "searchable":true
      },
      {  
         "allowsExplicitNullValue":false,
         "apiName":"format",
         "creatable":true,
         "editable":true,
         "fieldType":"DROP_DOWN",
         "inViews":[  
            "ITEM_FILES",
            "FILE_SUMMARY",
            "SI_FILES"
         ],
         "maxLength":100,
         "required":false,
         "searchable":true
      },
      {  
         "allowsExplicitNullValue":false,
         "apiName":"guid",
         "creatable":false,
         "editable":false,
         "fieldType":"GUID",
         "inViews":[  
            "ITEM_FILES",
            "FILE_SUMMARY",
            "SI_FILES"
         ],
         "searchable":false
      },
      {  
         "allowsExplicitNullValue":false,
         "apiName":"storageMethod",
         "creatable":true,
         "deprecated":true,
         "developerNotes":"This attribute is deprecated and storageMethodName must be used instead",
         "editable":false,
         "fieldType":"INTEGER",
         "inViews":[  
            "ITEM_FILES",
            "FILE_SUMMARY",
            "SI_FILES"
         ],
         "required":true,
         "searchable":false
      },
      {  
         "allowsExplicitNullValue":false,
         "apiName":"storageMethodName",
         "creatable":true,
         "editable":false,
         "fieldType":"FIXED_DROP_DOWN",
         "inViews":[  
            "ITEM_FILES",
            "FILE_SUMMARY",
            "SI_FILES"
         ],
         "required":true,
         "searchable":false
      },
      …
   ]
}
```
