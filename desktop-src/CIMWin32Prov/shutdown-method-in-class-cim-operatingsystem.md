---
Description: The Shutdown method requests a shutdown of the operating system.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: f2a2a98b-2f4f-4aa1-9f54-515660273c8d
ms.prod: windows-server-dev
ms.technology:
- cimwin32
- windows-management-instrumentation
ms.tgt_platform: multiple
title: Shutdown method of the CIM\_OperatingSystem class
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# Shutdown method of the CIM\_OperatingSystem class

The **Shutdown** method requests a shutdown of the operating system. The implementation or subclass of the operating system can establish dependencies between the **Shutdown** and [**Reboot**](reboot-method-in-class-cim-operatingsystem.md) methods. For example, more sophisticated capabilities can be provided, such as a scheduled shutdown and reboot.

> \[!Important\]  
> The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built. WMI currently supports only the [CIM 2.x version schemas](Http://Go.Microsoft.Com/FWLink/p/?LinkID=309367).

 

This topic uses Managed Object Format (MOF) syntax. For more information about using this method see [Calling a Method](https://msdn.microsoft.com/library/aa384832).

## Syntax


```mof
uint32 Shutdown();
```



## Parameters

This method has no parameters.

## Return value

Returns a value of 0 (zero) on success, and any other number to indicate an error.

## Remarks

This method is currently not implemented by WMI. To use this method, you must implement it in your own provider.

This documentation is derived from the CIM class descriptions published by the DMTF. Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista<br/>                                                                |
| Minimum supported server<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root\\CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## See also

<dl> <dt>

[CIM\_OperatingSystem](shutdown-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[**CIM\_OperatingSystem**](cim-operatingsystem.md)
</dt> </dl>

 

 



