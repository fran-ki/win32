---
title: HasArbitraryDataStream
description: The HasArbitraryDataStream attribute is a file-level attribute specifying whether the file contains any arbitrary data streams.
ms.assetid: 09c42ab1-7180-43ab-985a-ae6a4829376a
keywords:
- HasArbitraryDataStream windows Media Format
topic_type:
- apiref
api_name:
- HasArbitraryDataStream
api_type:
- NA
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# HasArbitraryDataStream

The **HasArbitraryDataStream** attribute is a file-level attribute specifying whether the file contains any arbitrary data streams.

## Global Constant

g\_wszWMHasArbitraryDataStream

## Data Type

**WMT\_TYPE\_BOOL**

## Remarks

This is a coded attribute.

This attribute cannot be duplicated at the file level. If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.

## See also

<dl> <dt>

[**Attribute List**](attribute-list.md)
</dt> </dl>

 

 



