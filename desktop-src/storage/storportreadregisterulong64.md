---
title: StorPortReadRegisterUlong64 routine
description: The StorPortReadRegisterUlong64 routine reads a 64-bit value from a specified 64-bit register address.
ms.assetid: 73A9E645-0B71-429F-9033-032BB83E60E4
keywords:
- StorPortReadRegisterUlong64 routine Storage Devices
topic_type:
- apiref
api_name:
- StorPortReadRegisterUlong64
api_location:
- storport.h
api_type:
- HeaderDef
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# StorPortReadRegisterUlong64 routine

The **StorPortReadRegisterUlong64** routine reads a 64-bit value from a specified 64-bit register address.

## Syntax


```C++
 VOID StorPortReadRegisterUlong64(
  _In_ PULONG64  Register
);
```



## Parameters

<dl> <dt>

*Register* \[in\]
</dt> <dd>

Pointer to the register where the data is to be read.

</dd> </dl>

## Return value

This routine does not return a value.

## Remarks

The **StorPortReadRegisterUlong64** routine is only available on the 64-bit version of Windows.

## Requirements



|                            |                                                                                                                                         |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Target platform<br/> | <dl> <dt>[Universal](http://go.microsoft.com/fwlink/p/?linkid=531356)</dt> </dl> |
| Version<br/>         | Available starting with Windows 8.<br/>                                                                                           |
| Header<br/>          | <dl> <dt>Storport.h (include Storport.h)</dt> </dl>                              |



## See also

<dl> <dt>

[**StorPortWriteRegisterUlong64**](storportwriteregisterulong64.md)
</dt> </dl>

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bstorage\storage%5D:%20StorPortReadRegisterUlong64%20routine%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")





