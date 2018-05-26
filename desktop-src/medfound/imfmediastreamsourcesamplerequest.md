---
Description: Represents a request for a sample from a MediaStreamSource.
ms.assetid: 43617cda-84b1-405f-8a20-be793413c186
title: IMFMediaStreamSourceSampleRequest interface
ms.date: 05/31/2018
ms.topic: interface
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# IMFMediaStreamSourceSampleRequest interface

Represents a request for a sample from a MediaStreamSource.

## Members

The **IMFMediaStreamSourceSampleRequest** interface inherits from the [**IUnknown**](com.iunknown) interface. **IMFMediaStreamSourceSampleRequest** also has these types of members:

-   [Methods](#methods)

### Methods

The **IMFMediaStreamSourceSampleRequest** interface has these methods.



| Method                                                           | Description                                             |
|:-----------------------------------------------------------------|:--------------------------------------------------------|
| [**SetSample**](imfmediastreamsourcesamplerequest-setsample.md) | Sets the sample for the media stream source.<br/> |



 

## Remarks

**MFMediaStreamSourceSampleRequest** is implemented by the [**Windows.Media.Core.MediaStreamSourceSampleRequest**](w_media_core.mediastreamsourcesamplerequest) runtime class.

## Requirements



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 8.1 \[desktop apps \| UWP apps\]<br/>                                  |
| Minimum supported server<br/> | Windows Server 2012 R2 \[desktop apps \| UWP apps\]<br/>                       |
| IDL<br/>                      | <dl> <dt>Mfidl.idl</dt> </dl> |



## See also

<dl> <dt>

[Media Foundation Interfaces](media-foundation-interfaces.md)
</dt> </dl>

 

 



