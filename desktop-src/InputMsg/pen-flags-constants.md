---
title: Pen Flags
description: Values that can appear in the penFlags field of the POINTER\_PEN\_INFO structure.
ms.assetid: BC3CE568-4090-4451-B780-18530C988305
topic_type:
- apiref
api_name:
- PEN_FLAG_NONE
- PEN_FLAG_BARREL
- PEN_FLAG_INVERTED
- PEN_FLAG_ERASER
api_location:
- winuser.h
api_type:
- HeaderDef
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Pen Flags

Values that can appear in the **penFlags** field of the [**POINTER\_PEN\_INFO**](/windows/win32/Winuser/ns-rimext-tagpointer_pen_info?branch=master) structure.

<dl> <dt>

<span id="PEN_FLAG_NONE"></span><span id="pen_flag_none"></span>**PEN\_FLAG\_NONE**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



There is no pen flag. This is the default.


</dt> </dl> </dd> <dt>

<span id="PEN_FLAG_BARREL"></span><span id="pen_flag_barrel"></span>**PEN\_FLAG\_BARREL**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



The barrel button is pressed.


</dt> </dl> </dd> <dt>

<span id="PEN_FLAG_INVERTED"></span><span id="pen_flag_inverted"></span>**PEN\_FLAG\_INVERTED**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



The pen is inverted.


</dt> </dl> </dd> <dt>

<span id="PEN_FLAG_ERASER"></span><span id="pen_flag_eraser"></span>**PEN\_FLAG\_ERASER**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



The eraser button is pressed.


</dt> </dl> </dd> </dl>

## Requirements



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 8 \[desktop apps only\]<br/>                                           |
| Minimum supported server<br/> | Windows Server 2012 \[desktop apps only\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



## See also

<dl> <dt>

[Constants](constants.md)
</dt> <dt>

[**POINTER\_INFO**](/windows/win32/Winuser/ns-rimext-tagpointer_info?branch=master)
</dt> </dl>

 

 




