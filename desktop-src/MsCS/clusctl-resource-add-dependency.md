---
title: CLUSCTL\_RESOURCE\_ADD\_DEPENDENCY control code
description: Internal.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: 7ae495c2-45b9-4530-b391-460c223742ad
ms.prod: windows-server-dev
ms.technology: failover-clustering
ms.tgt_platform: multiple
keywords:
- CLUSCTL_RESOURCE_ADD_DEPENDENCY control code Failover Cluster
topic_type:
- apiref
api_name:
- CLUSCTL_RESOURCE_ADD_DEPENDENCY
api_location:
- ClusAPI.h
api_type:
- HeaderDef
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# CLUSCTL\_RESOURCE\_ADD\_DEPENDENCY control code

Internal. Notifies a [resource DLL](resource-dlls.md) that a [dependency](resource-dependencies.md) being added to a [resource](resources.md) managed by the DLL. Resource DLLs receive this [control code](about-control-codes.md) as a parameter to the [**ResourceControl**](/windows/previous-versions/ResApi/nc-resapi-presource_control_routine?branch=master) callback function. Because the control code is internal, applications cannot use it in a control code function.

## Parameters

This control code has no parameters.

## Return value

This control code does not return a value.

## Remarks

ClusAPI.h defines the 32 bits of CLUSCTL\_RESOURCE\_ADD\_DEPENDENCY (0x01500012) as follows (for more information, see [Control Code Architecture](control-code-architecture.md)).



| Component                 | Bit location     | Value                                            |
|---------------------------|------------------|--------------------------------------------------|
| Object code<br/>    | 24 31<br/> | **CLUS\_OBJECT\_RESOURCE** (0x1)<br/>      |
| Global bit<br/>     | 23<br/>    | **CLUS\_NOT\_GLOBAL** (0x0)<br/>           |
| Modify bit<br/>     | 22<br/>    | **CLUS\_MODIFY** (0x1)<br/>                |
| User bit<br/>       | 21<br/>    | **CLCTL\_CLUSTER\_BASE** (0x0)<br/>        |
| Type bit<br/>       | 20<br/>    | Internal (0x1)<br/>                        |
| Operation code<br/> | 0 23<br/>  | **CLCTL\_ADD\_DEPENDENCY** (0x500012)<br/> |
| Access code<br/>    | 0 1<br/>   | **CLUS\_ACCESS\_WRITE** (0x2)<br/>         |



 

### Resource DLL Support

Optional. Support the CLUSCTL\_RESOURCE\_ADD\_DEPENDENCY control code for any resource that needs to retrieve or update properties or perform other tasks in response to the new dependency. The [Resource Monitor](resource-monitor.md) does not provide any default processing.

For more information on the [**ResourceControl**](/windows/previous-versions/ResApi/nc-resapi-presource_control_routine?branch=master) entry point function, see [Implementing ResourceControl](implementing-resourcecontrol.md).

## Requirements



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Minimum supported client<br/> | None supported<br/>                                                            |
| Minimum supported server<br/> | Windows Server 2008 Enterprise, Windows Server 2008 Datacenter<br/>            |
| Header<br/>                   | <dl> <dt>ClusAPI.h</dt> </dl> |



## See also

<dl> <dt>

[**AddClusterResourceDependency**](/windows/previous-versions/ClusAPI/nc-clusapi-pclusapi_add_cluster_resource_dependency?branch=master)
</dt> <dt>

[**ClusterResourceControl**](/windows/previous-versions/ClusAPI/nf-clusapi-clusterresourcecontrol?branch=master)
</dt> <dt>

[**ResourceControl**](/windows/previous-versions/ResApi/nc-resapi-presource_control_routine?branch=master)
</dt> </dl>

 

 




