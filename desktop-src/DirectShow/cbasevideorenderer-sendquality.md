---
Description: The SendQuality method sends a quality message to indicate what the supplier should do about quality.
ms.assetid: 9ce11c35-958c-4eda-9130-1139c4074bf7
title: CBaseVideoRenderer.SendQuality method
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# CBaseVideoRenderer.SendQuality method

The `SendQuality` method sends a quality message to indicate what the supplier should do about quality.

## Syntax


```C++
virtual HRESULT SendQuality(
   REFERENCE_TIME trLate,
   REFERENCE_TIME trRealStream
);
```



## Parameters

<dl> <dt>

*trLate* 
</dt> <dd>

Amount of time by which the frame is late.

</dd> <dt>

*trRealStream* 
</dt> <dd>

Currentstream time.

</dd> </dl>

## Return value

Returns an **HRESULT** value.

## Remarks

This member function sends a quality control message upstream to control quality management. The nature of the quality message (that is, whether to reduce or increase the number of samples) is determined in the quality management implementation in this derived class (see [**CBaseVideoRenderer::ShouldDrawSampleNow**](cbasevideorenderer-shoulddrawsamplenow.md)).

## Requirements



|                    |                                                                                                                                                                                            |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



## See also

<dl> <dt>

[**CBaseVideoRenderer Class**](cbasevideorenderer.md)
</dt> </dl>

 

 



