---
title: ATSCComponentTypeFlags enumeration
description: Specifies a flag that identifies an AC-3 audio stream in an ATSC broadcast stream.
ms.assetid: fd4db1f7-7c32-4fcc-b95a-269a550311ef
keywords:
- ATSCComponentTypeFlags enumeration Microsoft TV Technologies
topic_type:
- apiref
api_name:
- ATSCComponentTypeFlags
api_location:
- bdatypes.h
api_type:
- HeaderDef
ms.date: 05/31/2018
ms.topic: enumeration
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# ATSCComponentTypeFlags enumeration

Specifies a flag that identifies an AC-3 audio stream in an ATSC broadcast stream.

## Syntax


```C++
typedef enum ATSCComponentTypeFlags { 
  ATSCCT_AC3  = 0x00000001
} ATSCComponentTypeFlags;
```



## Constants

<dl> <dt>

<span id="ATSCCT_AC3"></span><span id="atscct_ac3"></span>**ATSCCT\_AC3**
</dt> <dd>

Indicates that the component contains AC-3 audio.

</dd> </dl>

## Remarks

*Component* in this context means a sub-stream.

## Requirements



|                   |                                                                                       |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Bdatypes.h</dt> </dl> |



## See also

<dl> <dt>

[**IATSCComponentType Interface**](/windows/previous-versions/tuner/nn-tuner-iatsccomponenttype?branch=master)
</dt> <dt>

[Tuning Model Enumerations](tuning-model-enumerations.md)
</dt> </dl>

 

 




