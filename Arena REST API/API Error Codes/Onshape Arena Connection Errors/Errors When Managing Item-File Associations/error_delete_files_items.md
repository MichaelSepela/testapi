# Errors When Removing Files from an Item
DELETE /items/&lt;GUID&gt;/files/&lt;GUID&gt;

This endpoint is used to remove a file from an existing Item through the Items World.  The file object still exist in the Files World but no longer be associated with the Item.  This endpoint requires that the Authorize User must have a Full License, Item Read & Write and File Read & Edit Access Policy Rules in Arena. This endpoint will return the following error information under the following scenarios:  


| Status Code  | Error Code  | Message  | Explanation  |
|  --- |  --- |  --- |  --- | 
| 400  | 3024  |  ```Either you do not have privileges to access the requested data or it does not exist.```    | The file is attempted to be removed by a user that does not have the appropriate access polices. The user does not have Item Read & Write nor File Read & Write Access Polices in Arena. <br> The use can attempt to remove a file from an item though the Arena Application. <br> Otherwise, the Arena Administrator can check the user’s access polices.<br>   |
| 400  | 3034  |  ```The item is locked.```    | The working revision of the unreleased item is assigned to a submitted change so the file cannot be removed from the item.Within the Files view of the Item, lock icons appear within the work area.<br>   |
| 400  | 3066  |  ```The working revision of the item is locked by inclusion in at least one change. ```    | The working revision of the Item has been assigned to a Change that is submitted for approval or has been approved and is waiting to be made effective.Within the Files view of the Item, lock icons appear within the work area.<br>   |

