---
Description: The PeekAllocator method returns a pointer to the pins allocator. The method does not increment the reference count on the interface.
ms.assetid: 67f1b872-4ae2-4fbe-9240-801ef8ae1e5b
title: CTransInPlaceInputPin.PeekAllocator method
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# CTransInPlaceInputPin.PeekAllocator method

The `PeekAllocator` method returns a pointer to the pin's allocator. The method does not increment the reference count on the interface.

## Syntax


```C++
IMemAllocator* PeekAllocator();
```



## Parameters

This method has no parameters.

## Return value

Returns the [**CBaseInputPin::m\_pAllocator**](cbaseinputpin-m-pallocator.md) member variable.

## Requirements



|                    |                                                                                                                                                                                            |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



## See also

<dl> <dt>

[**CTransInPlaceInputPin Class**](ctransinplaceinputpin.md)
</dt> </dl>

 

 



