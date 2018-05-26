---
Description: The Win32\_ProtocolBinding association WMI class relates a system-level driver, network protocol, and network adapter.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: 09b84bb2-9999-4e80-a330-88ed6b2bd5e9
ms.prod: windows-server-dev
ms.technology:
- cimwin32
- windows-management-instrumentation
ms.tgt_platform: multiple
title: Win32\_ProtocolBinding class
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# Win32\_ProtocolBinding class

The **Win32\_ProtocolBinding** association [WMI class](wmi.retrieving_a_class) relates a system-level driver, network protocol, and network adapter.

The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties. Properties and methods are in alphabetic order, not MOF order.

## Syntax

``` syntax
[Dynamic, Association, Provider("CIMWin32"), UUID("{8502C509-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ProtocolBinding
{
  Win32_NetworkProtocol REF Antecedent;
  Win32_SystemDriver    REF Dependent;
  Win32_NetworkAdapter  REF Device;
};
```

## Members

The **Win32\_ProtocolBinding** class has these types of members:

-   [Properties](#properties)

### Properties

The **Win32\_ProtocolBinding** class has these properties.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Data type: **Win32\_NetworkProtocol**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**key**](wmi.key_qualifier), [**MappingStrings**](wmi.standard_qualifiers) ("WMI\|Win32\_NetworkProtocol")
</dt> </dl>

Reference to the instance representing the protocol that is used with the system driver and on the network adapter.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Data type: **Win32\_SystemDriver**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**MappingStrings**](wmi.standard_qualifiers) ("WMI\|Win32\_SystemDriver")
</dt> </dl>

Reference to the instance representing the system driver that uses the network adapter through the network protocol of this class.

</dd> <dt>

**Device**
</dt> <dd> <dl> <dt>

Data type: **Win32\_NetworkAdapter**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**key**](wmi.key_qualifier), [**MappingStrings**](wmi.standard_qualifiers) ("WMI\|Win32\_NetworkAdapter")
</dt> </dl>

Properties of the network adapter being used on the computer system.

</dd> </dl>

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista<br/>                                                                |
| Minimum supported server<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root\\CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## See also

<dl> <dt>

[Operating System Classes](wmi.operating_system_classes)
</dt> </dl>

 

 



