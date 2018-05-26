---
Description: The Set method sets the media type from another media type.
ms.assetid: b3cf65c2-48db-4ee0-9a74-c1652f017eed
title: CMediaType.Set method
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# CMediaType.Set method

The `Set` method sets the media type from another media type.

## Syntax


```C++
HRESULT Set(
  [ref] const AM_MEDIA_TYPE &amp;mtype
);
```



## Parameters

<dl> <dt>

*mtype* \[ref\]
</dt> <dd>

Reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/strmif/ns-strmif-_ammediatype?branch=master) structure.

</dd> </dl>

## Return value

Returns S\_OK or E\_OUTOFMEMORY.

## Remarks

This method copies the entire media type from *mtype*.

## Requirements



|                    |                                                                                                                                                                                            |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype.h (include Streams.h)</dt> </dl>                                                                                     |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



## See also

<dl> <dt>

[**CMediaType Class**](cmediatype.md)
</dt> </dl>

 

 



