---
Description: Two-pass encoding can be used for constant bit rate (CBR) and for variable bit rate (VBR) encoding with some of the Windows Media codecs.
ms.assetid: eec5085c-9441-496a-8127-cf5d2686d917
title: Using Two-Pass Encoding
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Using Two-Pass Encoding

Two-pass encoding can be used for constant bit rate (CBR) and for variable bit rate (VBR) encoding with some of the Windows Media codecs. You can find the maximum number of encoding passes supported by a codec by retrieving the [MFPKEY\_PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md) property. None of the codecs supports more than two passes. Configure the DMO to use two passes by setting the [MFPKEY\_PASSESUSED](mfpkey-passesusedproperty.md) property to 2.

Deliver the samples to the encoder DMO one at a time, as you would in a one-pass mode. When you process the input samples for your preprocessing pass, the calls to [**IMediaObject::ProcessInput**](dshow.imediaobject_processinput) or [**IMFTransform::ProcessInput**](/windows/win32/mftransform/nf-mftransform-imftransform-processinput?branch=master) will return **S\_FALSE**, to indicate that no output is produced.

At the end of the first pass (after the last input is processed for the first time), you then must set the [MFPKEY\_ENDOFPASS](mfpkey-endofpassproperty.md) property to notify the codec that the next input processed is the first input of the second pass. No value is required for this property, so you should use an empty **VARIANT** structure.

## Related topics

<dl> <dt>

[Windows Media Codecs](windows-media-codecs.md)
</dt> </dl>

 

 


