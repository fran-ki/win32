---
title: IVMHostInfo DVDDrives property
description: The DVDDrives property contains an array of drive letters associated with host CD-ROM or DVD-ROM devices.
ms.assetid: 0ee2136e-1b1e-46a9-bfad-9d9103d33d9c
keywords:
- DVDDrives property Virtual Server
- DVDDrives property Virtual Server , IVMHostInfo interface
- IVMHostInfo interface Virtual Server , DVDDrives property
- DVDDrives property Virtual Server , VMHostInfo interface
- VMHostInfo interface Virtual Server , DVDDrives property
topic_type:
- apiref
api_name:
- IVMHostInfo.DVDDrives
- IVMHostInfo.get_DVDDrives
- VMHostInfo.DVDDrives
api_location:
- VsComInterfaces.h
api_type:
- COM
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# IVMHostInfo::DVDDrives property

The **DVDDrives** property contains an array of drive letters associated with host CD-ROM or DVD-ROM devices.

This property is read-only.

## Syntax


```C++
HRESULT get_DVDDrives(
  [out] VARIANT *DVDDrives
);
```

<span codelanguage="VisualBasic"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>VMHostInfo.DVDDrives( _
  ByRef DVDDrives _
)</code></pre></td>
</tr>
</tbody>
</table>



## Property value

Contains an array of drive letters associated with host CD-ROM or DVD-ROM devices.

This property value is read-only.

## Error codes



| Name                                                                                          | Meaning                                        |
|-----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt> S\_OK</dt> </dl>             | The operation was successful.<br/>       |
| <dl> <dt>E\_POINTER</dt> </dl>         | The outgoing parameter is **NULL**.<br/> |
| <dl> <dt>DISP\_E\_EXCEPTION</dt> </dl> | An unexpected error occurred.<br/>       |



## Requirements



|                     |                                                                                                   |
|---------------------|---------------------------------------------------------------------------------------------------|
| Product<br/>  | Microsoft Virtual Server 2005 onWindows Server 2003<br/>                                    |
| Download<br/> | Microsoft Virtual Server 2005 R2 SP1 Update onWindows Server 2008orWindows Server 2003<br/> |
| Header<br/>   | <dl> <dt>VsComInterfaces.h</dt> </dl>      |



## See also

<dl> <dt>

[**IVMHostInfo**](ivmhostinfo.md)
</dt> </dl>

 

 




