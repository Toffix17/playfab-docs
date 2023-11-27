---
author: jasonsandlin
title: "PFAccountManagementServerLinkServerCustomIdAsync"
description: "Links the custom server identifier, generated by the title, to the user's PlayFab account."
ms.author: jasonsa
ms.topic: reference
ms.service: playfab
ms.date: 09/25/2023
---

# PFAccountManagementServerLinkServerCustomIdAsync  

Links the custom server identifier, generated by the title, to the user's PlayFab account.  

## Syntax  
  
```cpp
HRESULT PFAccountManagementServerLinkServerCustomIdAsync(  
    PFEntityHandle titleEntityHandle,  
    const PFAccountManagementLinkServerCustomIdRequest* request,  
    XAsyncBlock* async  
)  
```  
  
### Parameters  
  
**`titleEntityHandle`** &nbsp; PFEntityHandle  
  
PFEntityHandle for a title Entity obtained using PFAuthenticationGetEntityWithSecretKeyAsync.  
  
**`request`** &nbsp; [PFAccountManagementLinkServerCustomIdRequest*](../../pfaccountmanagementtypes/structs/pfaccountmanagementlinkservercustomidrequest.md)  
  
Populated request object.  
  
**`async`** &nbsp; XAsyncBlock*  
*_Inout_*  
  
XAsyncBlock for the async operation.  
  
  
### Return value
Type: HRESULT
  
Result code for this API operation.
  
## Remarks  
  
This API is available on Win32. Call XAsyncGetStatus to get the status of the operation. If the service call is unsuccessful, the async result will be E_PF_ACCOUNT_NOT_FOUND, E_PF_LINKED_IDENTIFIER_ALREADY_CLAIMED or any of the global PlayFab Service errors. See doc page "Handling PlayFab Errors" for more details on error handling.
  
## Requirements  
  
**Header:** PFAccountManagement.h
  
## See also  
[PFAccountManagement members](../pfaccountmanagement_members.md)  

  
  