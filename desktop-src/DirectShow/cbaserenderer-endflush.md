---
Description: The EndFlush method ends a flush operation.
ms.assetid: 4c30abbf-7351-4eee-af9a-9330f6d1aa08
title: CBaseRenderer.EndFlush method
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# CBaseRenderer.EndFlush method

The `EndFlush` method ends a flush operation.

## Syntax


```C++
virtual HRESULT EndFlush();
```



## Parameters

This method has no parameters.

## Return value

Returns S\_OK.

## Remarks

The filter's input pin calls this method when it receives a call to the [**IPin::EndFlush**](/windows/win32/Strmif/nf-strmif-ipin-endflush?branch=master) method.

## Requirements



|                    |                                                                                                                                                                                            |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



## See also

<dl> <dt>

[**CBaseRenderer Class**](cbaserenderer.md)
</dt> </dl>

 

 



