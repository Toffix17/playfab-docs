---
author: jasonsandlin
title: "PFPlayerDataManagementClientGetUserDataAsync"
description: "Retrieves the title-specific custom data for the user which is readable and writable by the client"
ms.author: jasonsa
ms.topic: reference
ms.service: playfab
ms.date: 03/09/2023
---

# PFPlayerDataManagementClientGetUserDataAsync  

Retrieves the title-specific custom data for the user which is readable and writable by the client  

## Syntax  
  
```cpp
HRESULT PFPlayerDataManagementClientGetUserDataAsync(  
    PFEntityHandle entityHandle,  
    const PFPlayerDataManagementGetUserDataRequest* request,  
    XAsyncBlock* async  
)  
```  
  
### Parameters  
  
**`entityHandle`** &nbsp; PFEntityHandle  
  
PFTitlePlayerHandle to use for authentication.  
  
**`request`** &nbsp; [PFPlayerDataManagementGetUserDataRequest*](../../pfplayerdatamanagementtypes/structs/pfplayerdatamanagementgetuserdatarequest.md)  
  
Populated request object.  
  
**`async`** &nbsp; XAsyncBlock*  
*_Inout_*  
  
XAsyncBlock for the async operation.  
  
  
### Return value
Type: HRESULT
  
Result code for this API operation.
  
## Remarks  
  
Data is stored as JSON key-value pairs. Every time the data is updated via any source, the version counter is incremented. If the Version parameter is provided, then this call will only return data if the current version on the system is greater than the value provided. If the Keys parameter is provided, the data object returned will only contain the data specific to the indicated Keys. Otherwise, the full set of custom user data will be returned. See also ClientGetUserReadOnlyDataAsync, ClientUpdateUserDataAsync. If successful, call [PFPlayerDataManagementClientGetUserDataGetResult](pfplayerdatamanagementclientgetuserdatagetresult.md) to get the result.
  
## Requirements  
  
**Header:** PFPlayerDataManagement.h
  
## See also  
[PFPlayerDataManagement members](../pfplayerdatamanagement_members.md)  

  
  