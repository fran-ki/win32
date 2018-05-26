---
Description: This property sends a command to the device to search for a specified time code. The UVC device driver supports this property.
ms.assetid: 0502d59a-0a9e-4192-af9f-1553cd13a69c
title: KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH

This property sends a command to the device to search for a specified time code. The UVC device driver supports this property.



|                   |                                        |
|-------------------|----------------------------------------|
| Property Set GUID | PROPSETID\_EXT\_TRANSPORT              |
| Property ID       | KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH |
| Data Type         | **KSPROPERTY\_EXTXPORT\_S** structure  |



 

## Remarks

Fill in the **Timecode** member of the **KSPROPERTY\_EXTXPORT\_S** structure with the desired frame, second, minute, and hour. The **KSPROPERTY\_EXTXPORT\_S** structure is described in the Windows DDK.

## See also

<dl> <dt>

[External Device Transport Property Set](external-device-transport-property-set.md)
</dt> </dl>

 

 


