# 4000 to 4999 - Arena API Unique Error Codes
The list below details unique API error codes from 4000 to 4999.

Error codes within the range of 4000 to 4099 focus on Changes, Requests, Training Plans, and User Group objects.


| Latest Code  | Historical Code \(Before Winter 2023\)  | Message  |
|  --- |  --- |  --- | 
| 4000  |   |  ```Only Open and Unlock Change can add the Requests.```    |
| 4001  |   |  ```Item lifecycle phase has been changed.```    |
| 4002  |   |  ```Unreleased item cannot be added to a temporary change.```    |
| 4003  |   |  ```All views must be included for unreleased items.```    |
| 4004  |   |  ```Unreleased item must be released to In Design or In Production stage.```    |
| 4005  |   |  ```The item is already in the change.```    |
| 4006  |   |  ```End revision number cannot be empty.```    |
| 4007  |   |  ```Selected view is already in another change.```    |
| 4009  |   |  ```{0}.includedInChange cannot be set to true because the {1} view of this item is already included in a change.```    |
| 4010  |   |  ```Error adding disposition attributes.```    |
| 4011  |   |  ```Invalid number format prefix.```    |
| 4012  |   |  ```The number format prefix is required.```    |
| 4013  |   |  ```The change is locked, inaccessible or invalid.```    |
| 4014  |   |  ```The default value for Effectivity Type is enforced for Changes assigned to this category and cannot be edited.```    |
| 4015  |   |  ```A new prefix cannot be selected because the default number sequence is enforced for Changes assigned to this category.```    |
| 4016  |   |  ```Default number sequence is enforced for Changes assigned to this category, but no default sequence has been specified.```    |
| 4017  |   |  ```This Change cannot be assigned to the specified category because the enforced default effectivity of the category is not allowed.```    |
| 4018  |   |  ```This Change cannot be assigned to the specified category because once created, a Change cannot move to a different number sequence.```    |
| 4019  |   |  ```Effectivity cannot be modified because once created, a Change cannot move between permanent and temporary effectivity.```    |
| 4020  |   |  ```The change cannot be updated at this lifecycle stage.```    |
| 4021  |   |  ```Item revision is automatically generated for items of this category and cannot be entered manually.```    |
| 4022  |   |  ```The category settings of this Change does not allow duplicate revision values. Please ensure that the New Revision value is unique.```    |
| 4023  |   |  ```The "retrainingRequired" attribute is only valid in a request if the Item is already released and already associated with an existing Training Plan.```    |
| 4024  |   |  ```The attribute "retrainingRequired" can only be used with Items that are already associated with an existing Open Training Plan.```    |
| 4025  |   |  ```newItemRevision must be the working revision of the item.```    |
| 4026  |   |  ```On released items, notes can only be added if {0}.includedInThisChange is true.```    |
| 4027  |   |  ```{0}.includedInThisChange must be explicitly set to true to add notes.```    |
| 4028  |   |  ```Unreleased items must have {0}.includedInThisChange set to true.```    |
| 4029  |   |  ```routings cannot be specified.```    |
| 4030  |   |  ```The request is locked, inaccessible or invalid.```    |
| 4031  |   |  ```The request evaluator group guid "{0}" is not valid.```    |
| 4032  |   |  ```The request code value "{0}" is not valid.```    |
| 4033  |   |  ```The Request cannot be deleted because it has been added as an affected object in at least one Quality Process.```    |
| 4034  |   |  ```The Request cannot be deleted because it has been added as a reference in at least one Project.```    |
| 4035  |   |  ```The Request cannot be deleted because the status is either SUBMITTED or PROMOTED.```    |
| 4036  |   |  ```The evaluator group is required.```    |
| 4037  |   |  ```The Request cannot be deleted because current user is not a Request Administrator.```    |
| 4038  |   |  ```Invalid prefix. When updating a Request number, the user can only use prefixes supported by the original Request number sequence.```    |
| 4039  |   |  ```Items can only be added to unlocked Requests.```    |
| 4040  |   |  ```The Notes field value cannot exceed {0} characters.```    |
| 4041  |   |  ```Invalid item revision guid, only the effective revision of a released item or the working revision of an unreleased item are allowed.```    |
| 4042  |   |  ```This item has already been associated to this Request.```    |
| 4043  |   |  ```Items can only be updated under unlocked Requests.```    |
| 4044  |   |  ```Only request administrators can execute this specific request lifecycle transition.```    |
| 4045  |   |  ```The attribute "{0}" can only be updated when transitioning a request into the DEFERRED lifecycle status.```    |
| 4046  |   |  ```The attribute "{0}" can only be updated when transitioning a request into the PROMOTED or CLOSED lifecycle status.```    |
| 4047  |   |  ```The deferDeadlineDateTime value within the request body must be a date and time that exists after the date and time the endpoint is submitted.```    |
| 4048  |   |  ```The deferralCode value is not a valid option within this workspace.```    |
| 4049  |   |  ```A valid "{0}" is required when transitioning a request from the "{1}" lifecycle status to the "{2}" lifecycle status.```    |
| 4050  |   |  ```The resolutionNotes attribute can only be used by users promoting or closing requests created by supplier users.```    |
| 4051  |   |  ```The attribute "status" is required and the value must not be null in the payload.```    |
| 4052  |   |  ```{0} must be smaller than {1}.```    |
| 4060  | 4002  |  ```Unreleased item {0} cannot be added to a temporary change.```    |
| 4061  | 4005  |  ```The Items you selected cannot be added due to a conflict with an existing Change.```    |
| 4062  | 4029  |  ```This Change is locked. Edits can be performed only on Open and Unlocked Changes.```    |
| 4063  | 4029  |  ```Can only be called if the change is Open and Unlocked.```    |
| 4064  | 4029  |  ```Items can be deleted only when the change is Open and Unlocked.```    |
| 4065  | 4029  |  ```Revision number could not be auto-generated and must be set manually.```    |
| 4066  | 4029  |  ```Revision number must be non-empty and can't exceed {0} characters long.```    |
| 4067  | 4043  |  ```Items can only be deleted from unlocked Requests.```    |
| 4068  | 4048  |  ```The resolutionCode value is not a valid option within this workspace.```    |
| 4071  | 4001  |  ```Item lifecycle phase has been changed.```    |
| 4072  | 4002  |  ```This request cannot be converted to an object.```    |
| 4073  | 4003  |  ```The value for the attribute "{0}" is not valid.```    |
| 4074  | 4004  |  ```The attribute "{0}" is not recognized.```    |
| 4075  | 4005  |  ```The object with guid "{0}" is deleted successfully.```    |
| 4076  | 4006  |  ```You have successfully logged out.```    |
| 4077  | 4007  |  ```The file with guid "{0}" cannot be downloaded at this time.```    |
| 4078  | 4008  |  ```The requested file with guid "{0}" does not have any content. Please make sure it is a valid file.```    |
| 4079  | 4009  |  ```API feature is not enabled in your workspace.```    |
| 4080  | 4010  | \[Currently No Message\]  |
| 4081  | 4011  |  ```Your password has either been reset by an Account Administrator or has expired. Please proceed to the browser-based Arena user interface and configure a new password.```    |
| 4082  | 4012  |  ```Access not allowed.```    |
| 4083  | 4013  |  ```Too many invalid password attempts, account disabled for five minutes.```    |
| 4084  | 4014  |  ```You have exceeded your maximum of "{0}" requests during the last 24 hours. Additional requests can be made at "{1}".```    |
| 4085  | 4015  |  ```Unexpected data access error, please contact support.```    |
| 4086  | 4016  | \[Dynamic Error Message\]  |
| 4087  | 4017  |  ```Unknown errors encountered. Please contact Arena Technical Support{0}.```    |
| 4088  | 4018  | \[Dynamic Error Message\]  |
| 4089  | 4019  |  ```Invalid token.```    |
| 4090  | 4020  |  ```The Onshape feature is not enabled in your workspace.```    |
| 4201  |   |  ```Number of question required is too small.```    |
| 4202  |   |  ```Number of correct answer required is too small.```    |
| 4203  |   |  ```Need more questions.```    |
| 4204  |   |  ```Need more answers.```    |
| 4205  |   |  ```Invalid Quiz Id.```    |
| 4206  |   |  ```Invalid Quiz Attempt Id.```    |
| 4207  |   |  ```Quiz was not found.```    |
| 4208  |   |  ```Too many questions.```    |
| 4209  |   |  ```Too many answers in a question.```    |
| 4210  |   |  ```Number of questions is too big.```    |
| 4211  |   |  ```Number of required questions is too big.```    |
| 4212  |   |  ```Invalid item id.```    |
| 4213  |   |  ```Content is too long.```    |
| 4214  |   |  ```Content cannot be empty.```    |
| 4215  |   |  ```Training is not enabled for this user.```    |
| 4216  |   |  ```Only training managers can create a training plan.```    |
| 4217  |   |  ```Only the assigned training manager for this training plan can perform this action.```    |
| 4218  |   |  ```The training plan has already in status "{0}".```    |
| 4219  |   |  ```This user has already been added to this training plan. ```    |
| 4220  |   |  ```The due date cannot be set because there is no item in this training plan.```    |
| 4221  |   |  ```This item cannot be added to this training plan. Training plans can only contain a maximum of 200 items.```    |
| 4222  |   |  ```Only the effective revision of a released item can be added to a training plan.```    |
| 4223  |   |  ```This quality process step has already been added to this training plan.```    |
| 4224  |   |  ```Disabled user cannot be added to the training plan.```    |
| 4225  |   |  ```Quality process sign-off steps cannot be added to a training plan.```    |
| 4226  |   |  ```This item has already been added to this training plan.```    |
| 4227  |   |  ```Only designated training managers can assign a training manager for a training plan.```    |
| 4228  |   |  ```Only training managers can update a training plan.```    |
| 4229  |   |  ```Only the opened training plan can perform this action.```    |
| 4330  |   |  ```Only user in training manager list can be selected as a manager.```    |
| 4301  |   |  ```No permission to get the integration and integration associated information.```    |
| 4302  |   |  ```No permission to create the integration and integration associated information.```    |
| 4303  |   |  ```You currently do not have permission to mark this object as reconciled or to be reconciled.```  ```Please contact your Account Administrator for more information.```    |
| 4310  |   |  ```This endpoint is not supported for outbound integrations with Change-Based transfer types.```    |
| 4320  |   |  ```The itemsReconciled value is null or not valid, please use: true/false.```    |
| 4321  |   |  ```The reconciled value is null or not valid, please use: true/false.```    |
| 4322  |   |  ```The specified value "{0}" is not valid for the itemsReconciled field. Currently, only the values "true", "false", or "any" can be used for the itemsReconciled field.```    |
| 4323  |   |  ```The value "{0}" is not valid for date and time fields. Please format all date and time fields in UTC/Zulu format.```    |
| 4324  | 4322  |  ```The specified value "{0}" is not valid for the resourcesReconciled field. Currently, only the values "true", "false", or "any" can be used for the resourcesReconciled field.```    |
| 4325  | 4322  |  ```The specified value "{0}" is not valid for the reconciled field. Currently, only the values "true", "false", or "any" can be used for the reconciled field.```    |
| 4326  | 4322  |  ```The creationDateTimeFrom value: "{0}" cannot be later than creationDateTimeTo value: "{1}".```    |
| 4327  | 4322  |  ```The reconciledDateTimeFrom value: "{0}" cannot be later than reconciledDateTimeTo value: "{1}".```    |
| 4328  | 4322  |  ```The offSet value: "{0}" is not valid.```    |
| 4329  | 4322  |  ```The limit value: "{0}" is not valid.```    |
| 4399  |   |  ```Server exception: {0}.```    |
| 4501  |   |  ```The Supplier Identifier "{0}" matches an existing Supplier Identifier in the workspace. Due to current workspace settings, the Supplier Identifier attribute must be unique for each Supplier.```    |
| 4701  |   |  ```Name "{0}" matches an existing User Group Name in the workspace. Names must be unique.```    |
| 4808  |   |  ```Trace Matrix maximum limit exceeded.```    |
| 4809  |   |  ```Trace Coverage maximum limit exceeded.```    |
| 4897  |   |  ```Permanent changes cannot transition to the EXPIRED lifecycle status.```    |
| 4898  |   |  ```This Change has errors that render it no longer valid.```    |
| 4899  |   |  ```Temporary changes cannot transition to the EFFECTIVE lifecycle status from the COMPLETED lifecycle status.```    |
| 4900  |   |  ```Currently, implementationStatus can only be updated when transitioning into the following change lifecycle statuses: COMPLETED, EFFECTIVE, and EXPIRED.```    |
| 4901  |   |  ```The action could not be completed because either the Change or the BOM of one or more Items contains hidden Items (Items to which you do not have access.) Please contact your Account Administrator.```    |
| 4902  |   |  ```The requested change lifecycle transition can only be performed by a change administrator.```    |
| 4991  |   |  ```Invalid change administrator guid "{0}".```    |
| 4992  |   |  ```The change requires at least one change administrator.```    |
| 4993  |   |  ```Only change administrators can execute this specific change lifecycle transition.```    |
| 4994  |   |  ```Additional change submission errors exist. Only the first twenty errors are presented here for the user's convenience.```    |
| 4995  |   |  ```This specific change lifecycle transition does not support the inclusion of a change administrator in the request body.```    |
| 4996  |   |  ```The resulting change lifecycle status (and the overall change lifecycle path) is determined by the routing method configured in workspace settings. In order to submit this change, input "SUBMITTED" for status in the request body.```    |
| 4997  |   |  ```Only a change administrator or the user who submitted the change can perform this action.```    |
| 4998  |   |  ```This change cannot transition to the COMPLETED lifecycle status due to open implementation tasks.```    |
| 4999  |   |  ```Invalid implementation status. It could be: NOT_STARTED, IN_PROGRESS, NEEDS_ATTN, DONE, BLANK.```    |

