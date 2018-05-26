---
Description: The CheckReady method queries whether a state transition is complete.
ms.assetid: dfa669ed-a5ab-498e-9fc2-ff15d6ddbc13
title: CBaseRenderer.CheckReady method
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# CBaseRenderer.CheckReady method

The `CheckReady` method queries whether a state transition is complete.

## Syntax


```C++
BOOL CheckReady();
```



## Parameters

This method has no parameters.

## Return value

Returns **TRUE** if the state transition is complete, or **FALSE** if the filter is still transitioning to a new state.

## Requirements



|                    |                                                                                                                                                                                            |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



## See also

<dl> <dt>

[**CBaseRenderer Class**](cbaserenderer.md)
</dt> <dt>

[**CBaseRenderer::NotReady**](cbaserenderer-notready.md)
</dt> <dt>

[**CBaseRenderer::Ready**](cbaserenderer-ready.md)
</dt> </dl>

 

 



