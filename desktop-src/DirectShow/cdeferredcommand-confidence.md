---
Description: This method is not currently implemented and returns E\_NOTIMPL.
ms.assetid: 1004d7e1-d1e9-4217-bbbb-a25f46c7112f
title: CDeferredCommand.Confidence method
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# CDeferredCommand.Confidence method

This method is not currently implemented and returns E\_NOTIMPL.

## Syntax


```C++
HRESULT Confidence(
   LONG *pConfidence
);
```



## Parameters

<dl> <dt>

*pConfidence* 
</dt> <dd>

Pointer to the confidence level.

</dd> </dl>

## Return value

Returns E\_NOTIMPL.

## Remarks

For information about implementing this method, see [**IDeferredCommand::Confidence**](/windows/win32/Control/nf-control-ideferredcommand-confidence?branch=master).

## Requirements



|                    |                                                                                                                                                                                            |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



## See also

<dl> <dt>

[**CDeferredCommand Class**](cdeferredcommand.md)
</dt> </dl>

 

 



