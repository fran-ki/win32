---
title: FEATURE\_DATA\_VENDOR\_SPECIFIC structure
description: The FEATURE\_DATA\_VENDOR\_SPECIFIC structure holds information about a vendor-specific feature.
ms.assetid: 151e6456-4c1f-453b-9eb6-a139e0f93d6e
keywords:
- FEATURE_DATA_VENDOR_SPECIFIC structure Storage Devices
- PFEATURE_DATA_VENDOR_SPECIFIC structure pointer Storage Devices
topic_type:
- apiref
api_name:
- FEATURE_DATA_VENDOR_SPECIFIC
api_location:
- ntddmmc.h
api_type:
- HeaderDef
ms.date: 05/31/2018
ms.topic: structure
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# FEATURE\_DATA\_VENDOR\_SPECIFIC structure

The FEATURE\_DATA\_VENDOR\_SPECIFIC structure holds information about a vendor-specific feature.

## Syntax


```C++
typedef struct _FEATURE_DATA_VENDOR_SPECIFIC {
  FEATURE_HEADER Header;
  UCHAR          VendorSpecificData[];
} FEATURE_DATA_VENDOR_SPECIFIC, *PFEATURE_DATA_VENDOR_SPECIFIC;
```



## Members

<dl> <dt>

**Header**
</dt> <dd>

Contains a [**FEATURE\_HEADER**](feature-header.md) structure with header information for this feature descriptor.

</dd> <dt>

**VendorSpecificData**
</dt> <dd>

Contains an array that describes a vendor-specific feature.

</dd> </dl>

## Remarks

You can use this structure to access the data of any feature structure as though it were a simple character array.

## Requirements



|                   |                                                                                                           |
|-------------------|-----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Ntddmmc.h (include Ntddcdrm.h)</dt> </dl> |



## See also

<dl> <dt>

[**FEATURE\_HEADER**](feature-header.md)
</dt> <dt>

[**FEATURE\_NUMBER**](feature-number.md)
</dt> </dl>

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bstorage\storage%5D:%20FEATURE_DATA_VENDOR_SPECIFIC%20structure%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")





