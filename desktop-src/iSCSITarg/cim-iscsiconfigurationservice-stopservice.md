---
title: StopService method of the CIM\_iSCSIConfigurationService class
description: The StopService method places the Service in the stopped state.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: fded143b-4aa9-4606-9e71-81f89c90f1af
ms.prod: windows-server-dev
ms.technology:
- iscsi-target
- windows-management-instrumentation
ms.tgt_platform: multiple
keywords:
- StopService method iSCSI Software Target API
- StopService method iSCSI Software Target API , CIM_iSCSIConfigurationService class
- CIM_iSCSIConfigurationService class iSCSI Software Target API , StopService method
topic_type:
- apiref
api_name:
- CIM_iSCSIConfigurationService.StopService
api_location:
- SMiSCSITargetProv.dll
api_type:
- COM
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# StopService method of the CIM\_iSCSIConfigurationService class

The StopService method places the Service in the stopped state. Note that the function of this method overlaps with the RequestedState property. RequestedState was added to the model to maintain a record (such as a persisted value) of the last state request. Invoking the StopService method should set the RequestedState property appropriately. The method returns an integer value of 0 if the Service was successfully stopped, 1 if the request is not supported, and any other number to indicate an error. In a subclass, the set of possible return codes could be specified using a ValueMap qualifier on the method. The strings to which the ValueMap contents are translated can also be specified in the subclass as a Values array qualifier. Note: The semantics of this method overlap with the RequestStateChange method that is inherited from EnabledLogicalElement. This method is maintained because it has been widely implemented, and its simple "stop" semantics are convenient to use.

## Syntax


```mof
uint32 StopService();
```



## Parameters

This method has no parameters.

## Requirements



|                                     |                                                                                                  |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | None supported<br/>                                                                        |
| Minimum supported server<br/> | Windows Server 2012 R2<br/>                                                                |
| Namespace<br/>                | Root\\CIMv2\\Storage\\iScsiTarget<br/>                                                     |
| Header<br/>                   | <dl> <dt>Sdoias.h</dt> </dl>              |
| MOF<br/>                      | <dl> <dt>SmIscsiTarget.mof</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>SMiSCSITargetProv.dll</dt> </dl> |



## See also

<dl> <dt>

[**CIM\_iSCSIConfigurationService**](cim-iscsiconfigurationservice.md)
</dt> </dl>

 

 




